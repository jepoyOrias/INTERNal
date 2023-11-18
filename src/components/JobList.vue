<template>
    <div class="job-list">
        <ul>
            <li>
                <div class="d-flex justify-content-between">
                    Ordered by {{ order }}
                    <JobOrderBy @showOrderBy="handleFilter"/>
                </div>
               
            </li>
            <li v-for="(job, index) in orderedJobs" :key="job.id" @click="showJob(index,job.id)" :class="{ 'active': index === activeIndex }">
                <h2>{{ job.title }} in {{ job.location }}</h2>
                <div class="salary">
                    <p>php {{ job.salary }} </p>
                </div>
                <div class="description">
                    <p>Lorem ipsum dolor sit amet,</p>
                </div>
            </li>
        </ul>
        <JobListContent :job="job" />   
    </div>
</template>

<script lang="ts">
import { defineComponent, onMounted, PropType, ref,computed } from 'vue'
import JobListContent from './JobListContent.vue';
import JobOrderBy from './JobOrderBy.vue';
import Job from '@/types/Job';
import OrderBy from '@/types/OrderBy';

export default defineComponent({
    components: {JobListContent,JobOrderBy},
    props: {
        jobs: {
            required: true,
            type: Array as PropType<Job[]>
        },
    },
    setup(props) {
        const job = ref<Job>(props.jobs[0]);
        const order = ref<OrderBy>('title'); // Define the order here
        const activeIndex = ref<number>(0);

        const showJob = (index: number, jobId: string | number) => {
            activeIndex.value = index;
            const matchingJobs = [...props.jobs].filter(job => job.id == jobId);
            if (matchingJobs.length > 0) {
                job.value = matchingJobs[0];
                // You can do something with job.value
            } else {
                return
            }
        }
        
        const orderedJobs = computed(()=>{
            if (order.value) {
                return [...props.jobs].sort((a: Job, b: Job) => {
                return a[order.value].toString().toLocaleLowerCase() > b[order.value].toString().toLocaleLowerCase() ? 1 : -1;
                });
            }
            // Return the original order if no order is specified
            return props.jobs;
        
        });


        const handleFilter = (term: OrderBy): void =>{
            order.value = term; 
        }
        onMounted(()=>{
            showJob(0,"1")
        })
        return { job, showJob,orderedJobs ,handleFilter,order,activeIndex}
    },

})
</script>

<style scoped>
.job-list {
    max-width: 1600px;
    width: 100%;
    display: flex;
    justify-content: center;
    padding: 0 100px;
    margin: 0 auto;
}

.job-list ul {
    max-width: 35%;
    width: 100%;
    list-style-type: none;
    max-height: 95vh;
    overflow-y: scroll;
    padding: 0 10px;
    display: grid;
    gap: 20px;
}

.job-list ul li {
    box-shadow: -8px 10px 15px -3px rgba(0, 0, 0, 0.1);
    background-color: #fff;
    padding: 10px 20px;

}
.job-list ul li.active{
    border: 2px solid #000044 !important;
    border-radius: 5px;
    background-color: #fca311;
}
.job-list ul li.active .salary { 
    color: #fff;
}
.job-list ul li h2 {
    color: #000044;
}

.job-list ul li .salary {
    color: #fca311;
}
</style>
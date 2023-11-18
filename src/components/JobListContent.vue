<template>
    <div class="job-content">
        {{ job }}
    </div>
</template>

<script lang="ts">
import { defineComponent, PropType } from 'vue'
import Job from '@/types/Job'
export default defineComponent({
    props: {
            job:{
                required: true,
                type: Object as PropType<Job>
            }
    },
    setup () {
       return{}
    }
})
</script>

<style scoped>
.job-content{
    width: 100%;
    box-shadow: -8px 10px 15px -3px rgba(0, 0, 0, 0.1);
    background-color: #fff;
    padding: 10px;
    margin: 0 30px;
}
</style>
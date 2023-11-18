<template>
    <div class="dropdown">
    <button class="btn btn-transparent outline-none " type="button"  data-bs-toggle="dropdown" aria-expanded="false">
       Order by <i class="fa-solid fa-arrow-up-short-wide"></i>
    </button>
    <ul class="dropdown-menu">
        <li  v-for="(term , index ) in terms" :key="index">
            <button class="dropdown-item"  :class="{ 'active': index === activeIndex }" type="button" @click="handleFilter(index,term)">Order by {{ term }}</button>
        </li>
    </ul>
    </div>
</template>

<script lang="ts">
import { defineComponent,ref} from 'vue'
import OrderBy from '@/types/OrderBy';

export default defineComponent({
    emits: ['showOrderBy'], // Define emitted events here
   
    setup (_,{emit}) {
        const activeIndex = ref<number>(0);
        const terms = ref<OrderBy[]>(['title','location','salary']);
        const handleFilter = (index : number,term: OrderBy)=>{
            activeIndex.value = index;
            emit('showOrderBy', term)
        }

        return {handleFilter,terms,activeIndex }
    }
})
</script>

<style scoped>
.dropdown-item.active{
    background-color: #000044;
}
</style>
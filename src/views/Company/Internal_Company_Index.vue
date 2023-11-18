<template>
    <div>
        <Internal_Company_TopCompaniesVue :companies="companies" />
    </div>
</template>

<script lang="ts">
import { defineComponent , ref} from 'vue'
import Company from '@/types/Company';
import Internal_Company_TopCompaniesVue from '@/components/Company/Internal_Company_TopCompanies.vue';
export default defineComponent({
    components:{
        Internal_Company_TopCompaniesVue,
    },
    setup () {
        const companies = ref<Company[]>([
        {name: 'St. Luke`s Medical Center', headquarter: 'Manila', size: 1000, industry: 'Healthcare',founded: new Date(), id: '1', image: null},
        {name: 'G-Cash', headquarter: 'Makati', size: 800, industry: 'Information Technology (IT)',founded: new Date(),id: '2', image: null},
        {name: 'Toyota', headquarter: 'BGC', size: 15000, industry: 'Automotive',founded: new Date(),id: '3', image: null},
        {name: 'Ayala Corporation', headquarter: 'Pasig', size: 600, industry: 'Finance and Banking',founded: new Date(),id: '4', image: null},
        {name: 'SM Investments Corporation', headquarter: 'SM Mega mall', size: 2000, industry: 'Retail',founded: new Date(),id: '5', image: null},
        

   ]); 

        return {companies}
    }
})
</script>

<style scoped>

</style>
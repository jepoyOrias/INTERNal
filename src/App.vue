<template>
  <div class="app bg-light">
    <NavBar/>
    <HeroSection />
    <AdvanceInternship />
    <JobsNearMe />
    <IgniteYourCareer/>
    <InternalWhoWeAre/>
    <FooterComponent/>
   <!-- <JobList :jobs="jobs" /> -->
  </div>
 
</template>

<script lang="ts">

import { defineComponent, ref } from 'vue';
// import JobList from './components/JobList.vue';
import HeroSection from './components/HeroSection.vue';

import Job from './types/Job';
import NavBar from './components/NavBar.vue';
import FooterComponent from './components/FooterComponent.vue';
import AdvanceInternship from './views/Internal_AdvanceInternship.vue';
import JobsNearMe from './views/Internal_JobsNearMe.vue';
import IgniteYourCareer from './views/Internal_IgniteYourCareer.vue';
import InternalWhoWeAre from './views/Internal_WhoWeAre.vue';

export default defineComponent({
  name: 'App',
  components: {  HeroSection, NavBar, AdvanceInternship,JobsNearMe,IgniteYourCareer,InternalWhoWeAre,FooterComponent,},
  setup() {
      const jobs = ref<Job[]>([
        {title: 'Job 1', location: 'Manila', salary: 25000, id: '1'},
        {title: 'Job 2', location: 'Makati', salary: 32000, id: '2'},
        {title: 'Job 3', location: 'BGC', salary: 22000, id: '3'},
        {title: 'Job 4', location: 'Pasig', salary: 15000, id: '4'},
        {title: 'Job 5', location: 'SM Mega mall', salary: 52000, id: '5'},
        {title: 'Job 6', location: 'Manila', salary: 16000, id: '6'},
        {title: 'Job 7', location: 'Bulacan', salary: 17000, id: '7'},
        {title: 'Job 8', location: 'QC', salary: 12000, id: '8'},
        {title: 'Job 9', location: 'Fairview', salary: 11000, id: '9'}

   ]); 

   return {jobs}
  }
});
</script>

<style>
</style>

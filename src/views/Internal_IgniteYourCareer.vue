<template>
    <div class="bg-light">
            <div class="container col-xxl-8 px-md-4 py-xl-5 py-3">
        <div class="row flex-row-reverse align-items-start g-5 py-5">
          <div class="col-12">
            <h1 class="display-5 fw-bold text-dark lh-1 mb-3 text-center">Ignite Your Career</h1>
          </div>
          <div class="col-12">
            <div class="row gy-3">
                <div class="col-12 col-md-6 col-lg-4">
                    <div class="card py-2 border-0 shadow-lg h-100">
                        <div class="card-header border-0 fw-bold text-dark bg-white  fs-5 text-center">
                           Recommended Jobs For You
                        </div>
                        <div class="card-body">
                           <p class="text-center">Based on your skills and experience, we recommend the following jobs that align with your qualifications and career aspirations.</p>
                           <Internal_Company_Index />
                           <div class="d-grid gap-2 d-md-flex justify-content-md-center">
                                <button type="button" class="btn btn-outline-primary rounded-pill px-3 me-md-2">View More Recommended Jobs</button>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-12 col-md-6 col-lg-4">
                    <div class="card py-2 border-0 shadow-lg h-100">
                        <div class="card-header border-0 fw-bold text-primary bg-white fs-5 text-center">
                            Top Companies
                        </div>
                        <div class="card-body">
                            <p class="text-center">
                                Top companies consistently redefine industry standards, setting the benchmark for innovation, quality, and success.
                            </p>
                            <Internal_Company_Index />
                            <div class="d-grid gap-2 d-md-flex justify-content-md-center">
                                <button type="button" class="btn btn-outline-primary rounded-pill px-3 me-md-2">View More Companies</button>
                            </div>
                        </div>
                    </div>
                </div>
                <div class="col-12 col-md-6 col-lg-4">
                    <div class="card py-2 border-0 shadow-lg h-100">
                        <div class="card-header border-0 fw-bold text-secondary bg-white  fs-5 text-center">
                            Recent Job Postings
                        </div>
                        <div class="card-body">
                             <p class="text-center">Explore our recent job postings to discover exciting opportunities that match your expertise and career goals.</p>
                             <Internal_Company_Index />
                             <div class="d-grid gap-2 d-md-flex justify-content-md-center">
                                <button type="button" class="btn btn-outline-primary rounded-pill px-3 me-md-2">View More Jobs</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
           
           
          </div>
        </div>
        </div>
        </div>
    </template>
    
    <script lang="ts">
    import { defineComponent } from 'vue'
    import Internal_Company_Index from './Company/Internal_Company_Index.vue';
  
    export default defineComponent({
        components: {Internal_Company_Index},
        setup () {
            
    
            return {}
        }
    })
    </script>
    
    <style scoped>
    
    .card-header > span{
        width: 50px !important;
        height:50px !important;
        border-radius: 100%;
        
    }
    .card-header > span::before{
        display: flex;
        justify-content: center;
        align-items: center;
        font-size: 20px;
    }
    </style>
<template>
 <div class="bg-white">
            <div class="container col-xxl-8 px-md-4 py-xl-5 py-3">
        <div class="row flex-row-reverse align-items-start g-5 py-5">
          <div class="col-12">
            <h1 class="display-5 fw-bold text-dark lh-1 mb-3 text-center">Meet Our Team</h1>
          </div>
          <div class="col-12">
            <div class="box digonal-right">

</div>
            <div class="row gy-3">
                <div class="col-12 col-md-6 col-lg-4">
                  
                    <div class="team-member-card bg-change card  border-0 shadow-lg h-100">
                        <div class="card-header border-0 fw-bold text-white align-items-center  py-2 d-flex gap-3 h-100">
                           <div class="internal_avatar">
                                <img src="../assets/images/image.png" class="rounded-circle" alt="Jefffrey_Orias"/>
                           </div>
                           <div class="d-grid gap-1">
                                <h2 class="pb-0 mb-0">Jeffrey Orias</h2>
                                <div class="text-light">Full Stack Developer</div>
                                <div class="fw-bold text-dark rounded-pill w-100 d-flex gap-4 fs-4 mt-2">
                                    <a href="https://github.com/jepoyOrias" class="text-decoration-none fa-brands fa-github text-light"></a>
                                    <a href="www.linkedin.com/in/jeffrey-orias-34a978198" class="text-decoration-none fa-brands fa-linkedin text-light"></a>
                                    <a href="https://www.facebook.com/jepoy.jepoy.jepoy14" class="text-decoration-none fa-brands fa-facebook text-light"></a>
                                </div>
                           </div>
                          
                        </div>
                    </div>
                </div>
                <div class="col-12 col-md-6 col-lg-4">
                    <div class="card py-2 border-0 shadow-lg h-100">
                        <div class="card-header border-0 fw-bold text-primary bg-white ">
                            <span class="fa-solid fa-person me-3 "></span>
                            Mentorship and Guidance
                        </div>
                        <div class="card-body">
                            Receive personalized mentorship from seasoned professionals who are dedicated to helping you navigate your career path and overcome challenges.
                        </div>
                    </div>
                </div>
                <div class="col-12 col-md-6 col-lg-4">
                    <div class="card py-2 border-0 shadow-lg h-100">
                        <div class="card-header border-0 fw-bold text-info bg-white">
                            <span class="fa-solid fa-globe me-3 "></span>
                            Real-World Impact
                        </div>
                        <div class="card-body">
                            Contribute to projects that have a real-world impact, making a difference in the organization and the community, and leaving a lasting mark on your internship experience.
                        </div>
                    </div>
                </div>
                <div class="col-12 col-md-6 col-lg-4">
                    <div class="card py-2 border-0 shadow-lg h-100">
                        <div class="card-header border-0 fw-bold text-success bg-white">
                            <span class="fa-solid fa-rotate me-3 "></span>
                            Continuous Learning
                        </div>
                        <div class="card-body">
                            Immerse yourself in a culture that values continuous learning, providing opportunities for ongoing education and growth throughout your internship.
                        </div>
                    </div>
                </div>
                <div class="col-12 col-md-6 col-lg-4">
                    <div class="card py-2 border-0 shadow-lg h-100">
                        <div class="card-header border-0 fw-bold text-success bg-white">
                            <span class="fa-solid fa-rotate me-3 "></span>
                            Continuous Learning
                        </div>
                        <div class="card-body">
                            Immerse yourself in a culture that values continuous learning, providing opportunities for ongoing education and growth throughout your internship.
                        </div>
                    </div>
                </div>
                <div class="col-12 col-md-6 col-lg-4">
                    <div class="card py-2 border-0 shadow-lg h-100">
                        <div class="card-header border-0 fw-bold text-success bg-white">
                            <span class="fa-solid fa-rotate me-3 "></span>
                            Continuous Learning
                        </div>
                        <div class="card-body">
                            Immerse yourself in a culture that values continuous learning, providing opportunities for ongoing education and growth throughout your internship.
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

export default defineComponent({
    setup () {
        

        return {}
    }
})
</script>

<style scoped>
.internal_avatar {
    width: 100px;
    height: 100px;
}
.internal_avatar img{
    width: 100%;
    height: 100%;
}
.card-header   a:hover{
    color: var(--bs-white ) !important;
}

.team-member-card {
  position: relative;
  cursor: pointer;
 
}
.team-member-card .card-header{
    z-index: 3;
}
.team-member-card::after {
  content: "";
  position: absolute;
  transition: 1s;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: radial-gradient(farthest-side, var(--bs-success)  50%, transparent 50%) no-repeat, var(--bs-secondary);
  background-size: 400% 400%;
  background-position: bottom right !important;
}

.team-member-card:hover::after {
  background-position: center !important;
}


/* Apply styles to text elements within the card on hover */

</style>
<script setup lang='ts'>
import image from '../public/images/background/landing-about.png'
</script>
<template>

    <OtherLanding active="/about"  :image="image" bread="About Us" title="About Our Hospital"/>
    <About/>
    <section class="features">
        <div class="page">
            <div class="info">
                <div class="left">
                    <span>Why Choose Anand</span>
                    <h3>We Ready For 24 Hours</h3>
                    <p>we offer a wide range of comprehensive healthcare services to address all aspects of your health. </p>
                </div>
                <div class="right">
                    <div class="card-holder">
                        <div class="card">
                            <div class="icon">
                                <img src="../public/images/icons/child-care-icon.png" alt="child care">
                            </div>
                            <h4>Child Care</h4>
                            <p>State of the Art Operation Theatre for all Pediatric & Neonatal Surgeries. </p>
                            <NuxtLink to="#">Read More</NuxtLink>
                        </div>

                        <div class="card">
                            <div class="icon" style="background-color: hsla(77, 59%, 54%, 0.2);">
                                <img src="../public/images/icons/clinic-icon.png" alt="clinic">
                            </div>
                            <h4>Modern Clinic</h4>
                            <p>State of the Art Operation Theatre for all Pediatric & Neonatal Surgeries.  </p>
                            <NuxtLink to="#">Read More</NuxtLink>
                        </div>
                    </div>
                </div>
            </div>

            <div class="progress-holder">
                <div class="card" v-for="item in 3">
                    <div class="heading">
                        <h4>Environmental Testing</h4>
                        <span>90%</span>
                    </div>
                    <div class="progress">
                        <div class="fill"></div>
                    </div>
                    <p>From preventive care and health screenings to specialized treatments and chronic disease management.</p>
                </div>
            </div>
        </div>
    </section>
    
<!-- 
    <About/>
    <HomeFacility/>
    <Counter/>
    <Emergency/>
    <Testimonail/>
    <Blogs/> -->
    <Footer></Footer>

</template>
<style scoped>

.features{
    margin-top: 210px;
    min-height: 615px;
    background-color: black;
    padding-top: 110px;
    padding-bottom: 110px;
}


.features .info{
    display: grid;
    grid-template-columns: 1fr 1.3fr;
    gap: 45px;
}


.features .right{
    position: relative;
}

.features .right .card-holder{
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 32px;
    position: absolute;
    top: -210px;
}


/* left */
.features .info .left span{
    color: var(--color-primary);
}

.features .info .left h3{
    color: white;
    margin: 0;
    margin-top: 18px;
    margin-bottom: 24px;
}

.features .info .left p{
    color: #E6E6E6;
    max-width: calc(100% - 20px);
}
/* right card */
.features .right .card{
    background-color: white;
    min-height: 340px;
    border-radius: 30px;
    padding: 40px;
    box-shadow: 0px -3px 57px 0px rgba(0, 0, 0, 0.11);
}

.features .right .card .icon{
    width: 92px;
    height: 92px;
    border-radius: 50%;
    background-color: hsla(198, 100%, 43%, 0.2);
    display: flex;
    align-items: center;
    justify-content: center;
}

.features .right .card h4{
    margin-top: 23px;
    margin-bottom: 13px;
}

.features .right .card a{
    color: var(--color-primary);
}




/* ---- progress holder -------- */

.features .progress-holder{
    margin-top: 98px;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 70px;
}

.features .progress-holder .heading{
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.features .progress-holder .heading h4{
    font-family: 'Outfit';
    font-weight: normal;
    color: white;
    margin: 0;
}

.features .progress-holder .heading span{
    color: white;
}

.features .progress-holder p{
    color: #BFBFBF;
    font-size: 18px;
    margin-right: 20px;
}

.features .progress-holder .progress{
    width: 100%;
    border-radius: 20px;
    height: 7px;
    background-color: hsla(0, 0%, 25%, 0.7);
    margin-top: 20px;
    margin-bottom: 24px;
}

.features .progress-holder .progress .fill{
    width: 90%;
    height: 100%;
    background: linear-gradient(270deg, #0098DA 0%, rgba(142, 183, 38, 0.73) 100%);
    border-radius: 20px;
}


</style>
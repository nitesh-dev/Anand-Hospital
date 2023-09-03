<script setup lang='ts'>
import image from '../public/images/background/landing-appointment.png'


const data = ['Search Nearest Clinic Of Bootamins', 'Select Your Services Option', 'Fill Out The Appointment Form', 'Meet With Doctor At Bootamins Clinic']



</script>
<template>
    <OtherLanding active="/appointment" :image="image" bread="Appointment" title="Appointment" />

    <Booking />

    <div class="page shadow">
        <div></div>
    </div>

    <section class="steps">
        <div class="page">
            <div class="first">
                <div>
                    <span>Appointment Steps</span>
                    <h3>Easy Step To Booking Appointment</h3>
                </div>
                <p>Anand Children Hospital is one of the largest Pediatric Super Specialty Hospital of South Gujarat located
                    at the center of the Surat City. It is the 1st Pediatric Hospital in Gujarat to get Level III (A) NNF
                    (National Neonatology Forum) accreditation.</p>
            </div>
            <div class="last">
                <div class="card" v-for="item, index in data">
                    <div class="numbering">
                        <span>{{ index + 1 }}</span>
                        <hr>
                    </div>
                    <h4>{{ item }}</h4>
                    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut lab.</p>
                </div>
            </div>
        </div>
    </section>

    <Emergency style="margin-top: 110px; margin-bottom: 110px;" />

    <Question />
    <Footer></Footer>
</template>



<style scoped>


.steps{
    margin-top: 110px;
    margin-bottom: 110px;
}

.steps .first{
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 24px;
}

.steps .first span{
    color: var(--color-primary);
}

.steps .first p{
    margin: 0;
}

.steps .first h3{
    margin-top: 17px;
    max-width: 450px;
}


.steps .last{
    margin-top: 90px;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    gap: 24px;
}

.steps .card .numbering{
    display: grid;
    grid-template-columns: max-content 1fr;
    align-items: center;
    gap: 24px;
}

.steps .card .numbering hr{
    width: 100%;
    border: none;
    border-bottom: 1px dashed #BFBFBF;
}

.steps .card:last-child hr{
    border: none;
}

.steps .card .numbering span{
    position: relative;
    width: 60px;
    height: 60px;
    display: flex;
    align-items: center;
    justify-content: center;
    border-radius: 50%;
    background-color: white;
    font-size: 32px;
    color: var(--color-on-surface);
}


.steps .card .numbering span::after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  z-index: -1;
  margin: -2px;
  border-radius: inherit;
  background-image: linear-gradient(319deg, #0098DA 4.91%, #A8CF45 90.27%)
}

.steps .card h4{
    margin-top: 27px;
    margin-bottom: 11px;
    max-width: 200px;
}

.steps .card p{
    margin: 0;
}






/* extra */

.page.shadow {
    position: relative;
}

.page.shadow div {
    position: absolute;
    width: 360px;
    height: 360px;
    right: 0;
    background-color: var(--color-primary);
    transform: translateY(-50%);
    filter: blur(315px);
    z-index: -1;
}
</style>
<script setup lang='ts'>
import image from '../public/images/background/landing-about.png'
import profile1 from '../public/images/profile/specialist1.png'
import profile2 from '../public/images/profile/specialist2.png'
import profile3 from '../public/images/profile/specialist3.png'
import profile4 from '../public/images/profile/specialist4.png'

const data = Array<{
    name: string,
    role: string,
    rating: number,
    consultantCount: number,
    image: string
}>()


data.push({
    name: 'Dr. Chetan B. Shah',
    role: 'Neonatologist',
    rating: 4.7,
    consultantCount: 1324,
    image: profile1
})

data.push({
    name: 'Dr. Sachin A. Shah',
    role: 'Neonatologist',
    rating: 4.7,
    consultantCount: 1324,
    image: profile2
})

data.push({
    name: 'Dr Neeta C. Shah',
    role: 'Neonatologist',
    rating: 4.7,
    consultantCount: 1324,
    image: profile3
})

data.push({
    name: 'Dr. Charul J. Bhutwala',
    role: 'Neonatologist',
    rating: 4.7,
    consultantCount: 1324,
    image: profile4
})



</script>
<template>
    <OtherLanding active="/about" :image="image" bread="About Us" title="About Our Hospital" />
    <About />

    <!-- features -->
    <section class="features">
        <div class="page">
            <div class="info">
                <div class="left">
                    <span>Why Choose Anand</span>
                    <h3>We Ready For 24 Hours</h3>
                    <p>we offer a wide range of comprehensive healthcare services to address all aspects of your health.
                    </p>
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
                            <p>State of the Art Operation Theatre for all Pediatric & Neonatal Surgeries. </p>
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
                    <p>From preventive care and health screenings to specialized treatments and chronic disease management.
                    </p>
                </div>
            </div>
        </div>
    </section>


    <!-- specialist -->
    <section class="specialist">
        <div class="page">
            <span>Emergency Situation</span>
            <h3>Meet Our Specialists</h3>
            <p>A Big & Dedicated Team of Experienced Pediatricians to provide Quality Healthcare.</p>
            <div class="card-holder">
                <div class="card" v-for="item in data">
                    <img :src="item.image" :alt="item.name">
                    <div class="heading">
                        <h5>{{ item.name }}</h5>
                        <span>{{ item.role }}</span>
                    </div>
                    <div class="done">
                        <svg xmlns="http://www.w3.org/2000/svg" width="17" height="17" viewBox="0 0 17 17" fill="none">
                            <path
                                d="M8.33333 0C3.74167 0 0 3.74167 0 8.33333C0 12.925 3.74167 16.6667 8.33333 16.6667C12.925 16.6667 16.6667 12.925 16.6667 8.33333C16.6667 3.74167 12.925 0 8.33333 0ZM12.3167 6.41667L7.59167 11.1417C7.475 11.2583 7.31667 11.325 7.15 11.325C6.98333 11.325 6.825 11.2583 6.70833 11.1417L4.35 8.78333C4.10833 8.54167 4.10833 8.14166 4.35 7.9C4.59167 7.65833 4.99167 7.65833 5.23333 7.9L7.15 9.81666L11.4333 5.53333C11.675 5.29167 12.075 5.29167 12.3167 5.53333C12.5583 5.775 12.5583 6.16667 12.3167 6.41667Z"
                                fill="#A8CF45" />
                        </svg>
                        <p>{{ item.consultantCount }} Consultation Done</p>
                    </div>

                    <div class="rating">
                        <span>{{ item.rating }}</span>
                        <div>
                            <img v-for="item in 5" src="../public/images/icons/star.png" alt="star">
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </section>

    <!-- about2 -->

    <section class="about2">
        <div class="page">
            <span>Caring For The Health Of You And Your Family.</span>
            <h3>We Provide All Aspects Of Medical Practice For Your Whole Family!</h3>
            <div class="container">
                <div class="left">
                    <h5>Welcome to ANAND, where we offer comprehensive medical care tailored to every member of your family.
                    </h5>
                    <p>Our dedicated team of healthcare professionals is committed to providing you and your loved ones with
                        personalized and compassionate healthcare services. We understand the importance of family health.
                    </p>
                    <div class="list">
                        <div
                            v-for="item in ['Family-Centered Care', 'Preventive Services', 'Vaccinations and Immunizations']">
                            <svg xmlns="http://www.w3.org/2000/svg" width="17" height="17" viewBox="0 0 17 17" fill="none">
                                <path
                                    d="M8.33333 0C3.74167 0 0 3.74167 0 8.33333C0 12.925 3.74167 16.6667 8.33333 16.6667C12.925 16.6667 16.6667 12.925 16.6667 8.33333C16.6667 3.74167 12.925 0 8.33333 0ZM12.3167 6.41667L7.59167 11.1417C7.475 11.2583 7.31667 11.325 7.15 11.325C6.98333 11.325 6.825 11.2583 6.70833 11.1417L4.35 8.78333C4.10833 8.54167 4.10833 8.14166 4.35 7.9C4.59167 7.65833 4.99167 7.65833 5.23333 7.9L7.15 9.81666L11.4333 5.53333C11.675 5.29167 12.075 5.29167 12.3167 5.53333C12.5583 5.775 12.5583 6.16667 12.3167 6.41667Z"
                                    fill="#A8CF45" />
                            </svg>
                            <span>{{ item }}</span>
                        </div>
                    </div>
                    <WidgetButton><span>More About Us..</span></WidgetButton>

                </div>
                <div class="right">
                    <img src="../public/images/background/background1.png" class="top">
                    <img src="../public/images/background/background2.png" class="center">
                    <img src="../public/images/background/background3.png" class="bottom">

                    <div class="outline">
                        <img src="../public/images/outline/star.png" class="star">
                        <img src="../public/images/outline/circle.png" class="circle">
                    </div>

                </div>


            </div>
        </div>
    </section>

    <Question />
    <Footer></Footer>
</template>


<!-- Family-Centered Care
Preventive Services
Vaccinations and Immunizations -->


<style scoped>
.about2 {
    min-height: 515px;
    margin-top: 110px;
    margin-bottom: 110px;

}

.about2 .page>span {
    color: var(--color-primary);
    margin-top: 0;
}

.about2 h3 {
    margin-top: 17px;
    max-width: 780px;
    width: 100%;
    margin-bottom: 0;
}

.about2 .container {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
}


.about2 .right {
    min-height: 402px;
    position: relative;
}

.about2 .right>img {
    display: block;
    height: 118px;
    object-fit: cover;
    border-radius: 30px;
    box-shadow: 0px 4px 44px 0px rgba(0, 0, 0, 0.19);
}

.about2 .right .top {
    margin-right: auto;
    width: 272px;
}

.about2 .right .center {
    margin-left: auto;
    width: 345px;
    margin-right: 20px;
    margin-top: 24px;
    margin-bottom: 24px;
}

.about2 .right .bottom {
    margin-left: 80px;
    width: 304px;

}


.about2 h5 {
    font-size: 18px;
    font-weight: 500;
    font-family: 'Outfit';
    margin: 0;
    margin-bottom: 15px;
    margin-top: 70px;
    color: black;
}


.about2 button {
    margin-top: 32px;
}


/* list */
.about2 .list {
    margin-left: 15px;
    margin-top: 28px;
}

.about2 .list div {
    display: flex;
    align-items: center;
    gap: 11px;
}


/* outline */
.about2 .outline .star {
    position: absolute;
    z-index: -1;
    right: 136px;
    top: 40px;
}

.about2 .outline .circle {
    position: absolute;
    z-index: -1;
    left: 80px;
    bottom: 78px;

}




/* ----------------- features section ----------- */
.features {
    margin-top: 210px;
    min-height: 615px;
    background-color: black;
    padding-top: 110px;
    padding-bottom: 110px;
}


.features .info {
    display: grid;
    grid-template-columns: 1fr 1.3fr;
    gap: 45px;
}


.features .right {
    position: relative;
}

.features .right .card-holder {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 32px;
    position: absolute;
    top: -210px;
}


/* left */
.features .info .left span {
    color: var(--color-primary);
}

.features .info .left h3 {
    color: white;
    margin: 0;
    margin-top: 18px;
    margin-bottom: 24px;
}

.features .info .left p {
    color: #E6E6E6;
    max-width: calc(100% - 20px);
}

/* right card */
.features .right .card {
    background-color: white;
    min-height: 340px;
    border-radius: 30px;
    padding: 40px;
    box-shadow: 0px -3px 57px 0px rgba(0, 0, 0, 0.11);
}

.features .right .card .icon {
    width: 92px;
    height: 92px;
    border-radius: 50%;
    background-color: hsla(198, 100%, 43%, 0.2);
    display: flex;
    align-items: center;
    justify-content: center;
}

.features .right .card h4 {
    margin-top: 23px;
    margin-bottom: 13px;
}

.features .right .card a {
    color: var(--color-primary);
}




/* ---- progress holder -------- */

.features .progress-holder {
    margin-top: 98px;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 70px;
}

.features .progress-holder .heading {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.features .progress-holder .heading h4 {
    font-family: 'Outfit';
    font-weight: normal;
    color: white;
    margin: 0;
}

.features .progress-holder .heading span {
    color: white;
}

.features .progress-holder p {
    color: #BFBFBF;
    font-size: 18px;
    margin-right: 20px;
}

.features .progress-holder .progress {
    width: 100%;
    border-radius: 20px;
    height: 7px;
    background-color: hsla(0, 0%, 25%, 0.7);
    margin-top: 20px;
    margin-bottom: 24px;
}

.features .progress-holder .progress .fill {
    width: 90%;
    height: 100%;
    background: linear-gradient(270deg, #0098DA 0%, rgba(142, 183, 38, 0.73) 100%);
    border-radius: 20px;
}





/* --------------------- specialist section -------------- */

.specialist {
    margin-top: 110px;
}

.specialist .page>span {
    text-align: center;
    display: block;
    color: var(--color-primary);
}

.specialist h3 {
    text-align: center;
    margin: 0;
    margin-top: 18px;
    margin-bottom: 32px;
}

.specialist .page>p {
    text-align: center;
}

.specialist .card-holder {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    gap: 32px;
    margin-top: 62px;
}

.specialist .card {
    box-shadow: 0px 0px 42px 0px rgba(0, 0, 0, 0.10);
    padding: 24px;
    border-radius: 30px;
}



/* heading */

.specialist .card>img {
    width: 100%;
    border-radius: 30px;
}

.specialist .heading {
    height: 77px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: calc(100% - 20px);
    margin: auto;
    background: linear-gradient(319deg, #0098DA 0%, #A8CF45 100%);
    border-radius: 30px;
    transform: translateY(-50%);
}

.specialist .heading h5,
.specialist .heading span {
    color: white;
    font-weight: normal;
}

.specialist .heading span {
    opacity: 0.8;
}

.specialist .heading h5 {
    margin: 0;
    font-size: 18px;
    text-align: center;
}

.specialist .heading span {
    display: block;
    font-size: 14px;
    text-align: center;
}


/* done */
.specialist .done {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 9px;
    transform: translateY(-15px);
}

.specialist .done p {
    margin: 0;
}

/* rating */
.specialist .rating {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 9px;
}







@media only screen and (max-width: 1200px) {
    .specialist .card-holder {
        grid-template-columns: 1fr 1fr 1fr;
    }
}


@media only screen and (max-width: 1000px) {
    .features .info {
        grid-template-columns: 100%;
    }

    .features .right .card-holder {
        position: static;
    }

    .features .progress-holder {
        grid-template-columns: 1fr 1fr;
    }

    .features {
        margin-top: 110PX;
    }

    .about2 .container {
        grid-template-columns: 100%;
    }

}

@media only screen and (max-width: 900px) {
    .specialist .card-holder {
        grid-template-columns: 1fr 1fr;
        gap: 24px;
    }
}

@media only screen and (max-width: 700px) {
    .features .right .card-holder {
        grid-template-columns: 100%;
    }

    .features .progress-holder {
        grid-template-columns: 100%;
    }

    .specialist .card-holder {
        grid-template-columns: 100%;
    }
}


@media only screen and (max-width: 500px) {
    .about2 .right .top {
        width: 70%;
        border-radius: 17px;

    }

    .about2 .right .center {
        width: 90%;
        margin-right: 0;
        border-radius: 17px;
    }

    .about2 .right .bottom {
        margin-left: 0;
        width: 80%;
        border-radius: 17px;

    }
}
</style>
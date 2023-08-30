<script setup lang='ts'>
import image from '../public/images/background/landing-service.png'




</script>
<template>
    <OtherLanding active="/services" :image="image" bread="Services" title="Services Our Hospital" />

    <Question/>
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


.about2 button{
    margin-top: 32px;
}


/* list */
.about2 .list{
    margin-left: 15px;
    margin-top: 28px;
}

.about2 .list div{
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




/* ---------------------------  */</style>
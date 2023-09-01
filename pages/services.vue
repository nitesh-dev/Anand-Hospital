<script setup lang='ts'>
import image from '../public/images/background/landing-service.png'




</script>
<template>
    <OtherLanding active="/services" :image="image" bread="Services" title="Services Our Hospital" />

    <section class="facilities">
        <div class="page">
            <span>Our Facilities</span>
            <h3>Latest Technologies for Your Health</h3>

            <div class="holder">
                <div class="left">
                    <img src="../public/images/background/doctor3.png">
                    <p>As a tertiary referral ICU to provide state of the art care with the help of very good professionals
                        and infrastructure.</p>
                </div>
                <div class="right">
                    <div class="top">
                        <div class="content">
                            <h4>laboratory Analytics</h4>
                            <p>Anand Children Hospital is one of the largest Pediatric Super Specialty Hospital of South
                                Gujarat located at the center of the Surat City.</p>
                            <p>Our mission is "Towards Playful Health & Intact Survival with Humane Touch" for all.</p>
                            <WidgetButton><span>More About Us..</span></WidgetButton>
                        </div>
                        <img src="../public/images/background/background4.png">
                    </div>
                    <hr>
                    <div class="bottom">
                        <div class="item">
                            <div class="image-holder">
                                <img src="../public/images/background/mini-background4.png">
                                <div>
                                    <h5>Load More</h5>
                                    <svg xmlns="http://www.w3.org/2000/svg" width="16" height="12" viewBox="0 0 16 12"
                                        fill="none">
                                        <path
                                            d="M15.5303 6.53033C15.8232 6.23744 15.8232 5.76256 15.5303 5.46967L10.7574 0.696699C10.4645 0.403806 9.98959 0.403806 9.6967 0.696699C9.40381 0.989593 9.40381 1.46447 9.6967 1.75736L13.9393 6L9.6967 10.2426C9.40381 10.5355 9.40381 11.0104 9.6967 11.3033C9.98959 11.5962 10.4645 11.5962 10.7574 11.3033L15.5303 6.53033ZM0 6.75H15V5.25H0V6.75Z"
                                            fill="black" />
                                    </svg>
                                </div>
                            </div>
                            <p>Operation Theatre</p>
                        </div>

                        <div class="item">
                            <img src="../public/images/background/mini-background1.png">
                            <p>Laboratory Department</p>
                        </div>

                        <div class="item">
                            <img src="../public/images/background/mini-background2.png">
                            <p>NICU / PICU</p>
                        </div>

                        <div class="item">
                            <img src="../public/images/background/mini-background3.png">
                            <p>OPD & Ward</p>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </section>
    <Booking/>

    <Question />
    <Footer></Footer>
</template>



<style scoped>
.facilities {
    margin-top: 110px;
}

.facilities .page>span {
    text-align: center;
    display: block;
    color: var(--color-primary);
}

.facilities h3 {
    text-align: center;
    margin: 0;
    margin-top: 18px;
    margin-bottom: 70px;

}

.facilities .holder {
    display: grid;
    grid-template-columns: max-content 1fr;
    gap: 32px;
}

/* left */
.facilities .left {
    position: relative;
    widows: 372px;
}

.facilities .left img {
    height: 100%;
    border-radius: 30px;
    object-fit: cover;
}

.facilities .left p {
    position: absolute;
    margin: 0;
    left: 24px;
    right: 24px;
    bottom: 24px;
    background-color: black;
    border-radius: 30px;
    color: white;
    padding: 25px;
    text-align: center;
}


/* right */
.facilities .right h4 {
    margin: 15px 0;
}


.facilities .right .top {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 60px;
}

.facilities .right .top img{
    width: 100%;
    border-bottom: 30px;
    object-fit: cover;
}


.facilities hr{
    border: none;
    border-top: 1px solid #E6E6E6;
    margin: 37px 0;
}



/* bottom */
.facilities .bottom {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr 1fr;
    gap: 32px;
}

.facilities .bottom .item p{
    margin: 17px 0;
    text-align: center;
    color: var(--color-on-surface);
    font-weight: 500;
}

.facilities .bottom img{
    width: 100%;
    aspect-ratio: 1/1;
}

.facilities .bottom .item .image-holder{
    position: relative;
}

.facilities .bottom .item .image-holder h5{
    font-size: 18px;
}

.facilities .bottom .image-holder div{
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    display: flex;
    align-items: center;
    gap: 12px;
    justify-content: center;
}
</style>
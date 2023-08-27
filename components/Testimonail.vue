<script setup lang='ts'>

import profile1 from '../public/images/profile/profile-test1.png'

const data = Array<{
    image: string,
    message: string,
    name: string,
    role: string
}>()


data.push({
    image: profile1,
    message: '“Dr Sachin and his team gave wonderful treatment to my daughter. It is the best hospital I ever visited.”',
    name: '-Alex Thomas',
    role: "NICU"
})

data.push({
    image: profile1,
    message: '“Dr Sachin and his team gave wonderful treatment to my daughter. It is the best hospital I ever visited.”',
    name: '-Alex Thomas',
    role: "NICU"
})

data.push({
    image: profile1,
    message: '“Dr Sachin and his team gave wonderful treatment to my daughter. It is the best hospital I ever visited.”',
    name: '-Alex Thomas',
    role: "NICU"
})

data.push({
    image: profile1,
    message: '“Dr Sachin and his team gave wonderful treatment to my daughter. It is the best hospital I ever visited.”',
    name: '-Alex Thomas',
    role: "NICU"
})

data.push({
    image: profile1,
    message: '“Dr Sachin and his team gave wonderful treatment to my daughter. It is the best hospital I ever visited.”',
    name: '-Alex Thomas',
    role: "NICU"
})


const deskData = Array<{
    image: string,
    message: string,
    name: string,
    role: string
}[]>()



for (let index = 0; index < data.length; index++) {
    const element = data[index];

    if (index == 0 || index % 4 == 0) {
        const array = Array<{
            image: string,
            message: string,
            name: string,
            role: string
        }>()
        deskData.push(array)
    }
    deskData[deskData.length - 1].push(element)

}


console.table(deskData)




const autoPlay = {
    delay: 10000,
    disableOnInteraction: false,
}


const navigation = {
    nextEl: '.swiper-button-next',
    prevEl: '.swiper-button-prev',
}


const effect = {
    prev: {
        shadow: false,
        translate: ['-100%', 0, -1],
    },
    next: {
        translate: ['100%', 0, 0],
    },
}

</script>
<template>
    <section>
        <div class="page">
            <span>Emergency Situation</span>
            <h3>What Our Patients Say About Us</h3>
            <p>Our clients send us bunch of healthy smilies with our services and we love them</p>

            <div class="testimonial desktop">
                <Swiper :modules="[SwiperAutoplay, SwiperEffectCreative, SwiperNavigation]" :slides-per-view="1"
                    :loop="true" :effect="'creative'" :autoplay="autoPlay" :navigation="navigation"
                    :creative-effect="effect">
                    <SwiperSlide v-for="slide, index in deskData" :key="index">
                        <div class="testi-content">

                            <div class="card" v-if="slide.length > 0">
                                <img :src="slide[0].image">
                                <p>"{{ slide[0].message }}"</p>
                                <span class="name">{{ slide[0].name }} / </span>
                                <span>{{ slide[0].role }}</span>
                            </div>
                            <div class="space"></div>

                            <div class="card" v-if="slide.length > 1">
                                <img :src="slide[1].image">
                                <p>"{{ slide[1].message }}"</p>
                                <span class="name">{{ slide[1].name }} / </span>
                                <span>{{ slide[1].role }}</span>
                            </div>


                            <div class="card small" v-if="slide.length > 2" style="margin-left: auto;">
                                <img :src="slide[2].image">
                                <p>"{{ slide[2].message }}"</p>
                                <span class="name">{{ slide[2].name }} / </span>
                                <span>{{ slide[2].role }}</span>
                            </div>

                            <div class="space"></div>

                            <div class="card small" v-if="slide.length > 3" style="margin-right: auto;">
                                <img :src="slide[3].image">
                                <p>"{{ slide[3].message }}"</p>
                                <span class="name">{{ slide[3].name }} / </span>
                                <span>{{ slide[3].role }}</span>
                            </div>

                        </div>
                    </SwiperSlide>
                </Swiper>

                <div class="button-holder">
                    <div class="button swiper-button-prev">
                        <svg xmlns="http://www.w3.org/2000/svg" width="34" height="34" viewBox="0 0 34 34" fill="none">
                            <g clip-path="url(#clip0_140_217)">
                                <path
                                    d="M10.2838 10.991L4.94233 16.3339L4.86667 16.4294L4.81859 16.5057L4.76909 16.6033L4.73445 16.6945L4.71465 16.7652L4.7005 16.8388L4.69061 16.9194L4.68707 17.005L4.69768 17.1499L4.72525 17.2779L4.76768 17.3967L4.81718 17.4957L4.85183 17.553L4.88294 17.5968L4.97981 17.7092L10.2859 23.0154C10.4664 23.1954 10.7087 23.2997 10.9635 23.3071C11.2183 23.3144 11.4662 23.2242 11.6567 23.0548C11.8472 22.8854 11.9658 22.6497 11.9883 22.3959C12.0109 22.142 11.9356 21.8891 11.7779 21.6888L11.7002 21.5997L8.10098 18.0006L28.3129 18.0006C28.5564 18.0005 28.7916 17.9117 28.9742 17.7506C29.1569 17.5896 29.2745 17.3675 29.305 17.1259L29.3128 17.0007C29.3129 16.7572 29.2243 16.522 29.0634 16.3392C28.9024 16.1564 28.6804 16.0386 28.4388 16.0079L28.3122 16.0002L8.10239 16.0009L11.698 12.4052C11.8712 12.232 11.9748 12.0013 11.9891 11.7567C12.0035 11.5122 11.9276 11.271 11.7758 11.0787L11.698 10.991C11.5105 10.8035 11.2561 10.6981 10.9909 10.6981C10.7257 10.6981 10.4714 10.8035 10.2838 10.991Z"
                                    fill="white" />
                            </g>
                            <defs>
                                <clipPath id="clip0_140_217">
                                    <rect width="24" height="24" fill="white"
                                        transform="translate(0.0292969 17) rotate(-45)" />
                                </clipPath>
                            </defs>
                        </svg>
                    </div>
                    <div class="button swiper-button-next">
                        <svg xmlns="http://www.w3.org/2000/svg" width="34" height="34" viewBox="0 0 34 34" fill="none">
                            <g clip-path="url(#clip0_140_217)">
                                <path
                                    d="M23.7159 23.009L29.0574 17.6661L29.1331 17.5706L29.1812 17.4943L29.2307 17.3967L29.2653 17.3055L29.2851 17.2348L29.2993 17.1612L29.3092 17.0806L29.3127 16.9951L29.3021 16.8501L29.2745 16.7221L29.2321 16.6033L29.1826 16.5043L29.1479 16.447L29.1168 16.4032L29.0199 16.2908L23.7138 10.9846C23.5334 10.8046 23.291 10.7003 23.0363 10.693C22.7815 10.6856 22.5335 10.7759 22.343 10.9452C22.1526 11.1146 22.0339 11.3503 22.0114 11.6041C21.9889 11.858 22.0641 12.1109 22.2218 12.3112L22.2996 12.4003L25.8988 15.9994L5.68684 15.9994C5.44333 15.9995 5.2082 16.0883 5.02555 16.2494C4.8429 16.4104 4.72528 16.6326 4.69477 16.8741L4.68699 16.9993C4.68681 17.2428 4.77549 17.478 4.9364 17.6608C5.09731 17.8436 5.31939 17.9614 5.56097 17.9921L5.68755 17.9999L25.8974 17.9991L22.3017 21.5948C22.1286 21.768 22.025 21.9987 22.0106 22.2433C21.9963 22.4878 22.0722 22.729 22.2239 22.9213L22.3017 23.009C22.4893 23.1965 22.7436 23.3019 23.0088 23.3019C23.274 23.3019 23.5284 23.1965 23.7159 23.009Z"
                                    fill="white" />
                            </g>
                            <defs>
                                <clipPath id="clip0_140_217">
                                    <rect width="24" height="24" fill="white"
                                        transform="translate(33.9705 17) rotate(135)" />
                                </clipPath>
                            </defs>
                        </svg>
                    </div>
                </div>
            </div>
        </div>
    </section>
</template>
<style scoped>
section {
    margin-top: 100px;
    width: 100%;
    min-height: 1020px;
    background-image: url('../public/images/background/testimonials.png');
    background-position: center;
    background-size: cover;
    background-repeat: no-repeat;
}

section .page {
    padding-top: 100px;
    padding-bottom: 80px;
}

section .page>span {
    color: var(--color-primary);
    display: block;
    text-align: center;
    margin-bottom: 18px;
}

section h3 {
    text-align: center;
    color: white;
    margin: 0;
}

section .page>p {
    text-align: center;
    color: #E6E6E6;
}


section .testimonial {
    position: relative;
}



.testimonial .card {
    background-color: white;
    padding: 36px;
    border-radius: 30px;
    position: relative;
    width: 100%;
}

.testimonial .card.small {
    width: calc(100% - 60px);
}

.testimonial .card img {
    position: absolute;
    top: 0;
    transform: translateY(-50%);
    z-index: 1;
    border: 2px solid white;
    border-radius: 50%;
    box-shadow: 0px 13px 23px 0px rgba(0, 0, 0, 0.15);

}

.testimonial .card .name {
    color: var(--color-primary);
}

.testimonial .testi-content {
    display: grid;
    grid-template-columns: 1fr 0 1fr;
    gap: 143px;
    padding-top: 100px;
}



/* button */
.button-holder {
    display: flex;
    justify-content: center;
    margin-top: 100px;
    gap: 30px;
}

.swiper-button-prev::after,
.swiper-button-next::after {
    content: '';
}

.button-holder .button svg {
    fill: white;
}


.button-holder .button {
    position: static;

}</style>
<script setup lang='ts'>

const data = Array<{
    title: string,
    content: string,
    url: string
}>()

data.push({
    title: 'Operation Theatre',
    content: 'State of the Art Operation Theatre for all Pediatric & Neonatal Surgeries.',
    url: ''
})

data.push({
    title: 'Laboratory Department',
    content: 'State of the Art Operation Theatre for all Pediatric & Neonatal Surgeries.',
    url: ''
})

data.push({
    title: 'OPD & Ward',
    content: 'State of the Art Operation Theatre for all Pediatric & Neonatal Surgeries.',
    url: ''
})

data.push({
    title: 'NICU / PICU',
    content: 'State of the Art Operation Theatre for all Pediatric & Neonatal Surgeries.',
    url: ''
})

</script>
<template>
    <section>
        <div class="page">
            <div class="content">
                <div>
                    <span>Our Facilities</span>
                    <h3>Latest Technologies for Your Health</h3>
                </div>
                <div>
                    <p>Anand Children Hospital is one of the largest Pediatric Super Specialty Hospital of South Gujarat
                        located at the center of the Surat City.</p>
                    <p>Our mission is "Towards Playful Health & Intact Survival with Humane Touch" for all.</p>
                </div>
            </div>
            <div class="detail">
                <img src="../public/images/background/doctor.png">
                <div class="card-holder">
                    <div class="card" v-for="item, index in data" :class="{'variant': index == 1 || index == 2}">
                        <div class="svg-holder">
                            <img v-if="index == 0" src="../public/images/icons/bed.png">
                            <img v-else-if="index == 1" src="../public/images/icons/microscope.png">
                            <img v-else-if="index == 2" src="../public/images/icons/opd.png">
                            <img v-else-if="index == 3" src="../public/images/icons/nicu.png">
                        </div>
                        <h4>{{ item.title }}</h4>
                        <p>{{ item.content }}</p>
                        <a href="#">Learn More
                            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="9" viewBox="0 0 16 9" fill="none">
                                <path
                                    d="M15.3536 4.85355C15.5488 4.65829 15.5488 4.34171 15.3536 4.14645L12.1716 0.964466C11.9763 0.769204 11.6597 0.769204 11.4645 0.964466C11.2692 1.15973 11.2692 1.47631 11.4645 1.67157L14.2929 4.5L11.4645 7.32843C11.2692 7.52369 11.2692 7.84027 11.4645 8.03553C11.6597 8.2308 11.9763 8.2308 12.1716 8.03553L15.3536 4.85355ZM0 5H15V4H0V5Z"
                                    fill="black" />
                            </svg>
                        </a>
                    </div>
                </div>
            </div>
        </div>
        <div class="outline"></div>
    </section>
</template>
<style scoped>
section {
    margin-top: 110px;
    position: relative;
}

.content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
}

.content span {
    color: var(--color-primary);
    margin: 16px 0;
    margin-top: 0;
    display: block;
}

section h3 {
    margin: 0;
    line-height: 125%;
    max-width: 350px;
}

.outline {
    position: absolute;
    top: -8px;
    left: 0;
    height: 187px;
    width: calc(max(0px, ((100% - var(--max-page-width)) * 0.5) - var(--page-gap) * 2) + 235px);
    border-radius: 0px 100px 100px 0px;
    opacity: 0.1;
    background: linear-gradient(319deg, #0098DA 0%, #A8CF45 100%);
}


/* detail */

.detail {
    margin-top: 5rem;
    display: grid;
    grid-template-columns: 1fr 1.2fr;
    gap: 32px;
}

.detail>img {
    border-radius: 30px;
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.detail .card-holder {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 32px;
}

.detail .card {
    border-radius: 30px;
    background-color: hsla(198, 100%, 43%, 0.11);
    padding: 24px;
}

.detail .card.variant{
    background-color:hsla(77, 59%, 54%, 0.1);
}

.detail .card.variant .svg-holder{
    background-color:hsla(77, 59%, 54%, 0.2);
}

.detail .svg-holder {
    margin-left: auto;
    width: 77px;
    height: 77px;
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: hsla(198, 100%, 43%, 0.2);
    border-radius: 50%;
}

.detail h4 {
    margin: 0;
    margin-top: 18px;
}

.detail .svg-holder img {
    width: 42px;
}

.detail a {
    color: #404040;
}


</style>
<script setup lang='ts'>

const data = Array<{
    title: string,
    content: string
}>()

data.push({
    title: 'Why is Webflow the best nocode tool?',
    content: 'Ut enim ad minim veniam quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat aute irure dolor'
})

data.push({
    title: 'When did Webflow was founded?',
    content: 'Ut enim ad minim veniam quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat aute irure dolor'
})

data.push({
    title: 'Is NoCode the future of the web?',
    content: 'Ut enim ad minim veniam quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat aute irure dolor'
})


const activeIndex = ref(0)

function changeActiveQuestion(index: number) {
    activeIndex.value = index
}


</script>
<template>
    <section>
        <div class="page">
            <span>Clients Questions</span>
            <h3>Clients Questions</h3>
            <p>A Big & Dedicated Team of Experienced Pediatricians to provide Quality Healthcare.</p>
            <div class="holder">
                <div class="left">
                    <template v-for="item, index in data">
                        <div class="card" :class="{ 'active': index == activeIndex }" @click="changeActiveQuestion(index)">
                            <div class="heading">
                                <h4>{{ item.title }}</h4>

                                <!-- in active svg -->
                                <svg v-if="index != activeIndex" xmlns="http://www.w3.org/2000/svg" width="43" height="43"
                                    viewBox="0 0 43 43" fill="none">
                                    <rect x="0.969238" y="0.385254" width="42" height="42" rx="8" fill="#F7F7FF" />
                                    <path
                                        d="M20.9985 13.1353C20.9985 12.583 21.4463 12.1353 21.9985 12.1353H22.0268C22.5791 12.1353 23.0268 12.583 23.0268 13.1353V29.1353C23.0268 29.6875 22.5791 30.1353 22.0268 30.1353H21.9985C21.4463 30.1353 20.9985 29.6875 20.9985 29.1353V13.1353Z"
                                        fill="#0098DA" />
                                    <path
                                        d="M12.8853 21.1353C12.8853 20.583 13.333 20.1353 13.8853 20.1353H30.1397C30.692 20.1353 31.1397 20.583 31.1397 21.1353C31.1397 21.6875 30.692 22.1353 30.1397 22.1353H13.8853C13.333 22.1353 12.8853 21.6875 12.8853 21.1353Z"
                                        fill="#0098DA" />
                                </svg>

                                <!-- active svg -->
                                <svg v-else xmlns="http://www.w3.org/2000/svg" width="43" height="42" viewBox="0 0 43 42"
                                    fill="none">
                                    <rect x="0.117188" width="42" height="42" rx="8" fill="url(#paint0_linear_151_54)" />
                                    <path
                                        d="M29.4019 22.25C30.0922 22.25 30.6519 21.6904 30.6519 21C30.6519 20.3096 30.0922 19.75 29.4019 19.75H13.1475C12.4571 19.75 11.8975 20.3096 11.8975 21C11.8975 21.6904 12.4571 22.25 13.1475 22.25H29.4019Z"
                                        fill="white" stroke="white" stroke-width="0.5" stroke-linecap="round" />
                                    <defs>
                                        <linearGradient id="paint0_linear_151_54" x1="37.7072" y1="42" x2="4.31719"
                                            y2="3.99" gradientUnits="userSpaceOnUse">
                                            <stop stop-color="#0098DA" />
                                            <stop offset="1" stop-color="#A8CF45" />
                                        </linearGradient>
                                    </defs>
                                </svg>

                            </div>
                            <p v-if="index == activeIndex">{{ item.content }}</p>
                        </div>
                    </template>

                </div>
                <img src="../public/images/background/question.png">

                <!-- outline -->

                <svg class="star" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none">
                    <g opacity="0.6">
                        <path opacity="0.6"
                            d="M6.38997 7.98322L0 11.5723L6.38996 15.1613L9.97899 21.5513L13.568 15.1613L19.958 11.5723L13.568 7.98322L9.979 1.59326L6.38997 7.98322Z"
                            fill="#0098DA" />
                    </g>
                </svg>

            </div>
        </div>
    </section>
</template>
<style scoped>
.page>span {
    text-align: center;
    display: block;
    color: var(--color-primary);
}

h3 {
    text-align: center;
    margin: 0;
    margin-top: 18px;
    margin-bottom: 32px;
}

.page>p {
    text-align: center;
}


.holder {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 133px;
    margin-top: 62px;
    align-items: center;
    position: relative;
}

.holder .left {
    display: flex;
    flex-direction: column;
    gap: 26px;
}

.holder img {
    width: 100%;
}


.holder .card {
    padding: 32px;
    min-height: 122px;
    background-color: hsla(198, 100%, 43%, 0.2);
    border-radius: 30px;
}

.holder .card.active {
    background-color: hsla(77, 59%, 54%, 0.2);
}

.holder .card h4 {
    margin: 0;
}

.holder .card p {
    margin-top: 4px;
    margin-bottom: 10px;
    max-width: 400px;
}



.holder .card .heading {
    display: flex;
    align-items: center;
    justify-content: space-between;
    margin-top: 8px;
}


/* outline */
.holder .star{
    position: absolute;
    z-index: -1;
    top: 100px;
    right: 50%;
}
</style>
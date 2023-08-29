<script setup lang='ts'>
defineProps<{
    active: string,
    image: string,
    bread: string,
    title: string
}>()
</script>
<template>
    <section class="landing">
        <div class="page">
            <Header :active="active" :is-outline="true"></Header>
            <div class="content">
                <div class="left">
                    <div class="bread">
                        <span>Home</span>
                        <span>></span>
                        <span>{{ bread }}</span>
                    </div>
                    <h2>{{ title }}</h2>
                    <p>Good health is a state of mental, physical and social well being and it does not just mean the absence diseanse!</p>
                </div>

                <img :src="image">
            </div>

        </div>

        <div class="background">
            <img src="../public/images/background/landing-background.png" >
            <div class="layer"></div>
        </div>
    </section>
</template>
<style scoped>
.landing {
    min-height: 597px;
    position: relative;
    margin-bottom: 110px;
}

.landing .page {
    position: relative;
    overflow: auto;
}



.landing .background{
    position: absolute;
    width: 100%;
    height: 100%;
    left: 0;
    top: 0;
    z-index: -5;
}

.landing .background img{
    width: 100%;
    height: 100%;
    object-fit: cover;
}


.landing .background .layer{
    position: absolute;
    z-index: -4;
    right: 0;
    top: 0;
    height: 100%;
    background-color: hsla(198, 100%, 43%, 0.3);
    width: calc((100% - var(--max-page-width)) * 0.5 + 355px);
    
}


/* content */
.landing .content {
    margin-top: 144px;
    display: grid;
    grid-template-columns: max-content 1fr;
    gap: 1rem;
    align-items: center;
}

.landing .content .left{
    max-width: 480px;
    width: 100%;
}

.landing .content img{
    display: block;
    margin-left: auto;
    margin-right: 160px;
}

.landing h2{
    margin: 0;
    margin-top: 4px;
    margin-bottom: 16px;
}

.landing .bread{
    display: flex;
    align-items: center;
    gap: 12px;
    color: var(--color-primary);
}

.landing .bread span{
    font-size: 18px;
}

.landing .content p{
    color: var(--color-on-surface);
}
</style>
<script setup lang='ts'>
import blog1 from '../public/images/blog/blog1.png'
</script>
<template>
    <section>
        <div class="page">
            <span>Our Blogs</span>
            <h3>Don't Wait Until It's Too Late, Read Our Blog Today!</h3>
            <p>A Big & Dedicated Team of Experienced Pediatricians to provide Quality Healthcare.</p>

            <div class="card-holder hide-scroll">
                <div class="card" v-for="item  in 10">
                    <img :src="blog1">
                    <div class="content">
                        <span>· June 14, 2017</span>
                        <p>6 Tips For Maintaining Children's Mental Health When Sick</p>
                        <NuxtLink to="#">Read More..</NuxtLink>
                    </div>
                </div>
            </div>

            <WidgetButton><span>See More..</span></WidgetButton>
        </div>

        <div class="outline"></div>
    </section>
</template>
<style scoped>


section{
    margin-top: 110px;
    position: relative;
}

section .outline{
    width: 211px;
    height: 211px;
    border-radius: 50%;
    position: absolute;
    z-index: -1;
    top: 200px;
    left: calc(max(0px, ((100% - var(--max-page-width)) * 0.5) - var(--page-gap) * 2));
    background-image: linear-gradient(319deg, #007baf 0%, #A8CF45 100%);
    filter: blur(200px);
}

section .page>span {
    color: var(--color-primary);
    display: block;
    text-align: center;
    margin-bottom: 18px;
}

section h3 {
    text-align: center;
    margin: 0;
}

section .page>p {
    text-align: center;
    margin: 32px 0;
}


.card-holder{
    width: 100%;
    overflow: auto;
    display: flex;
    align-items: center;
    gap: 24px;
    margin: 0;
    padding: 0 var(--page-gap);
    margin-top: 50px;
}

.card-holder .card{
    background-color: hsla(198, 100%, 43%, 0.07);
    min-width: 335px;
    padding: 16px;
    min-height: 380px;
    border-radius: 30px;
    margin: 24px 0;

}


.card img{
    width: 100%;
    height: 164px;
    border-radius: 30px;
}

.card-holder .card:hover{
    background-color: white;
    box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
}


.card span{
    margin-top: 30px;
    display: block;
    color: var(--color-secondary);
}

.card p{
    font-size: 18px;
    color: var(--color-on-surface);
    margin: 0.5em 0;
}

.card a{
    color: var(--color-primary);
    font-weight: 500;
}

button{
    margin: auto;
    margin-top: 20px;
}
</style>
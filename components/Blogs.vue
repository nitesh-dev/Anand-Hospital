<script setup lang='ts'>
import blog1 from '../public/images/blog/blog1.png'
import blog2 from '../public/images/blog/blog2.png'
import blog3 from '../public/images/blog/blog3.png'
import blog4 from '../public/images/blog/blog4.png'

const data = Array<{
    image: string,
    date: string,
    title: string,
    link: string
}>()


data.push({
    image: blog1,
    date: '· June 14, 2017',
    title: 'Very important immunizations for children at the age of 12',
    link: '#'
})

data.push({
    image: blog2,
    date: '· June 14, 2017',
    title: 'Adapting to the development of children’s needs',
    link: '#'
})

data.push({
    image: blog3,
    date: '· June 14, 2017',
    title: '6 Tips For Maintaining Children’s Mental Health When Sick',
    link: '#'
})

data.push({
    image: blog4,
    date: '· June 14, 2017',
    title: 'Very important immunizations for children at the age of 12',
    link: '#'
})





</script>
<template>
    <section>
        <div class="page">
            <span>Our Blogs</span>
            <h3>Don't Wait Until It's Too Late, Read Our Blog Today!</h3>
            <p>A Big & Dedicated Team of Experienced Pediatricians to provide Quality Healthcare.</p>

            <div class="card-holder hide-scroll">
                <div class="card" v-for="item  in data">
                    <img :src="item.image">
                    <div class="content">
                        <span>{{ item.date }}</span>
                        <p>{{ item.title }}</p>
                        <NuxtLink :to="item.link">Read More..</NuxtLink>
                    </div>
                </div>
            </div>

            <WidgetButton><span>See More..</span></WidgetButton>
        </div>

        <div class="outline"></div>
    </section>
</template>
<style scoped>
section {
    margin-top: 110px;
    position: relative;
}

section .outline {
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
    margin-top: 0;
    margin-bottom: 0;
}

section .page>p {
    text-align: center;
    margin-top: 32px;
    margin-bottom: 32px;
}


.card-holder {
    width: 100%;
    overflow: auto;
    display: flex;
    align-items: center;
    gap: 24px;
    margin: 0;
    padding: 0 var(--page-gap);
    margin-top: 50px;
}

.card-holder .card {
    background-color: hsla(198, 100%, 43%, 0.07);
    min-width: 335px;
    padding: 16px;
    min-height: 380px;
    border-radius: 30px;
    margin: 24px 0;

}


.card img {
    width: 100%;
    height: 164px;
    border-radius: 30px;
}

.card-holder .card:hover {
    background-color: white;
    box-shadow: rgba(149, 157, 165, 0.2) 0px 8px 24px;
}


.card span {
    margin-top: 30px;
    display: block;
    color: var(--color-secondary);
}

.card p {
    font-size: 18px;
    color: var(--color-on-surface);
    margin: 0.5em 0;
}

.card a {
    color: var(--color-primary);
    font-weight: 500;
}

button {
    margin: auto;
    margin-top: 20px;
}
</style>
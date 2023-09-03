<script setup lang='ts'>
import slugify from 'slugify'

import image from '~/public/images/background/landing-about.png'

const readMoreUrl = '/blogs/readmore/' + slugify("Some Of The Most Common Children's Diseases")

</script>
<template>
    <OtherLanding active="/blogs" :image="image" bread="Blogs" title="Our Blogs" />

    <section class="blogs">
        <div class="page">
            <span>Our Blogs</span>
            <h3>Don't Wait Until It's Too Late, Read Our Blog Today!</h3>
            <p>A Big & Dedicated Team of Experienced Pediatricians to provide Quality Healthcare.</p>

            <div class="contents">

                <!-- first  col-->
                <div class="inner-content">
                    <div class="card">
                        <img src="~/public/images/blog/blog-small1.png">
                        <div>
                            <span>Some Of The Most Common Children's Diseases</span>
                            <p>A Big & Dedicated Team of Experienced Pediatricians ..</p>
                            <NuxtLink :to="readMoreUrl">Read More...</NuxtLink>
                        </div>
                    </div>
                    <div class="card">
                        <img src="~/public/images/blog/blog-small3.png">
                        <div>
                            <span>Some Of The Most Common Children's Diseases</span>
                            <p>A Big & Dedicated Team of Experienced Pediatricians ..</p>
                            <NuxtLink :to="readMoreUrl">Read More...</NuxtLink>
                        </div>
                    </div>
                </div>

                <!-- second  col-->
                <div class="inner-content">
                    <div class="card">
                        <img src="~/public/images/blog/blog-small2.png">
                        <div>
                            <span>Some Of The Most Common Children's Diseases</span>
                            <p>A Big & Dedicated Team of Experienced Pediatricians ..</p>
                            <NuxtLink :to="readMoreUrl">Read More...</NuxtLink>
                        </div>
                    </div>
                    <div class="card">
                        <img src="~/public/images/blog/blog-small4.png">
                        <div>
                            <span>Some Of The Most Common Children's Diseases</span>
                            <p>A Big & Dedicated Team of Experienced Pediatricians ..</p>
                            <NuxtLink :to="readMoreUrl">Read More...</NuxtLink>
                        </div>
                    </div>
                </div>

                <!-- third col -->
                <div class="image-card">
                    <div>
                        <h4>Some Of The Most Common Children's Diseases</h4>
                        <p>A Big & Dedicated Team of Experienced Pediatricians ..</p>
                        <NuxtLink :to="readMoreUrl">Read More...</NuxtLink>
                    </div>
                    <img src="~/public/images/blog/blog-big1.png">
                </div>

            </div>

            <div class="contents">

                <!-- first col -->
                <div class="image-card">
                    <div>
                        <h4>Some Of The Most Common Children's Diseases</h4>
                        <p>A Big & Dedicated Team of Experienced Pediatricians ..</p>
                        <NuxtLink :to="readMoreUrl">Read More...</NuxtLink>
                    </div>
                    <img src="~/public/images/blog/blog-big2.png">
                </div>

                <!-- second  col-->
                <div class="inner-content">
                    <div class="card">
                        <img src="~/public/images/blog/blog-small5.png">
                        <div>
                            <span>Some Of The Most Common Children's Diseases</span>
                            <p>A Big & Dedicated Team of Experienced Pediatricians ..</p>
                            <NuxtLink :to="readMoreUrl">Read More...</NuxtLink>
                        </div>
                    </div>
                    <div class="card">
                        <img src="~/public/images/blog/blog-small7.png">
                        <div>
                            <span>Some Of The Most Common Children's Diseases</span>
                            <p>A Big & Dedicated Team of Experienced Pediatricians ..</p>
                            <NuxtLink :to="readMoreUrl">Read More...</NuxtLink>
                        </div>
                    </div>
                </div>

                <!-- third  col-->
                <div class="inner-content">
                    <div class="card">
                        <img src="~/public/images/blog/blog-small6.png">
                        <div>
                            <span>Some Of The Most Common Children's Diseases</span>
                            <p>A Big & Dedicated Team of Experienced Pediatricians ..</p>
                            <NuxtLink :to="readMoreUrl">Read More...</NuxtLink>
                        </div>
                    </div>
                    <div class="card">
                        <img src="~/public/images/blog/blog-small8.png">
                        <div>
                            <span>Some Of The Most Common Children's Diseases</span>
                            <p>A Big & Dedicated Team of Experienced Pediatricians ..</p>
                            <NuxtLink :to="readMoreUrl">Read More...</NuxtLink>
                        </div>
                    </div>
                </div>

            </div>
        </div>
    </section>

    <Footer></Footer>
</template>



<style scoped>
.blogs {
    margin-top: 110px;
}

.blogs .page>span {
    text-align: center;
    display: block;
    color: var(--color-primary);
}

.blogs h3 {
    text-align: center;
    margin: 0;
    margin-top: 18px;
    margin-bottom: 32px;
}

.blogs .page>p {
    text-align: center;
    margin-bottom: 72px;
}


.blogs .contents {
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 32px;
    margin-bottom: 60px;
}

.blogs .inner-content {
    display: flex;
    flex-direction: column;
    gap: 32px;
}



/* card */
.blogs .card {
    min-height: 215px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 32px;
    align-items: center;
}

.blogs .card img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 30px;
}

.blogs .card span {
    display: block;
    color: var(--color-on-surface);
    line-height: normal;
    font-weight: 500;
}

.blogs .card p {
    margin: 14px 0;
}

.blogs .card a {
    display: block;
    color: var(--color-primary);
}



/* image-card */

.blogs .image-card {
    position: relative;
    height: 100%;
    display: flex;
    align-items: end;
}

.blogs .image-card img {
    position: absolute;
    z-index: -1;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
    border-radius: 30px;
}

.blogs .image-card div {
    margin: 24px;

}

.blogs .image-card h4 {
    font-size: 24px;
    color: white;
    line-height: 151.8%;
    margin: 0;
}

.blogs .image-card p {
    color: white;
    margin-top: 8px;
}

.blogs .image-card a {
    color: white;
    display: block;
}
</style>
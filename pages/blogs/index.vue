<script setup lang='ts'>
import slugify from 'slugify'

import image from '~/public/images/background/landing-blogs.png'

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

    <section class="facility">
        <div class="page">
            <div class="heading">
                <div>
                    <span>Our Facilities</span>
                    <h3>Latest Technologies for Your Health</h3>
                </div>
                <p>Anand Children Hospital is one of the largest Pediatric Super Specialty Hospital of South Gujarat located
                    at the center of the Surat City. </p>
            </div>

            <div class="image-holder">
                <img src="~/public/images/blog/blog5.png">
                <div>
                    <span> · June 14, 2017</span>
                    <h4>6 Tips For Maintaining Children's Mental Health When Sick</h4>
                    <p>Anand Children Hospital is one of the largest Pediatric Super Specialty Hospital of South Gujarat
                        located at the center of the Surat City. sit amet, consectetur</p>
                    <p>Our mission is "Towards Playful Health & Intact Survival with Humane Touch" for all.sit amet,
                        consectetur adipisicing elisit amet, consectetur adipisicing eli</p>
                    <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod tempor incididunt ut labore
                        et dolore magna aliqua.</p>

                    <NuxtLink :to="readMoreUrl">Read More...</NuxtLink>
                </div>
            </div>
        </div>
    </section>

    <Footer></Footer>
</template>



<style scoped>
.facility {
    margin-top: 110px;
}

.facility .heading {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 32px;
}

.facility .heading span {
    display: block;
    color: var(--color-primary);
}

.facility .heading h3 {
    margin-top: 17px;
    max-width: 354px;
}

.facility .heading p {
    margin: 0;
    max-width: 480px;
    margin-top: 30px;
}


.facility .image-holder {
    margin-top: 90px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 32px;
    align-items: center;
}

.facility .image-holder img {
    width: 100%;
    min-height: 372px;
    object-fit: cover;
    border-radius: 30px;
    display: block;
}


.facility .image-holder span {
    color: var(--color-secondary);
    display: block;
}

.facility .image-holder h4 {
    font-size: 18px;
    margin-top: 8px;
    margin-bottom: 22px;
}

.facility .image-holder p {
    margin: 8px 0;
}

.facility .image-holder a {
    margin-top: 30px;
    display: block;
    color: var(--color-primary);
}






/* ---------------- blogs section -------------- */
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




@media only screen and (max-width: 1100px) {
    .blogs .contents {
        grid-template-columns: 100%;
        gap: 32px;
        margin-bottom: 40px;
    }

    .blogs .inner-content {
        flex-direction: row;
        gap: 32px;
    }

    .blogs .image-card {
        min-height: 417px;
    }
}

@media only screen and (max-width: 800px) {

    .blogs .contents {
        gap: 24px;
    }

    .blogs .inner-content {
        flex-direction: column;
        gap: 24px;
    }

    .blogs .card {
        gap: 24px;
    }

}


@media only screen and (max-width: 700px) {
    .facility .heading {
        grid-template-columns: 100%;
        gap: 0px;
    }

    .facility .heading h3 {
        margin-bottom: 0;
    }

    .facility .image-holder {
        margin-top: 24px;
        grid-template-columns: 100%;
        gap: 24px;
    }

}
</style>
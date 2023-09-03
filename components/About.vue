<script setup lang='ts'>
</script>
<template>
    <section>
        <div class="page">
            <div class="grid">
                <div class="left">

                    <span>About ANAND Hospital</span>
                    <h3>We Are Always Ensure Best Treatment Your Child</h3>
                    <p>Anand Children Hospital is one of the largest Pediatric Super Specialty Hospital of South Gujarat
                        located at the center of the Surat City. It is the 1st Pediatric Hospital in Gujarat </p>

                    <WidgetButton>
                        <span>More About Us..</span>
                    </WidgetButton>

                    <div class="profile">
                        <img src="../public/images/profile/profile.png">
                        <div class="content">
                            <p>"<b>Healthy Child</b> is the Best Promise to the Future"</p>
                            <span>- Dr. Chetan B. Shah</span>
                        </div>
                    </div>
                </div>
                <div class="right">
                    <div class="image-holder">
                        <img class="top" src="../public/images/background/image1.png">
                        <div class="holder">
                            <img class="label" src="../public/images/outline/care.png">
                            <svg xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 16 16" fill="none">
                                <path
                                    d="M1.52637 7.63086C4.91194 7.63086 7.65649 4.21441 7.65649 0C7.65649 4.21441 10.401 7.63086 13.7866 7.63086C10.401 7.63086 7.65649 11.0473 7.65649 15.2617C7.65649 11.0473 4.91194 7.63086 1.52637 7.63086Z"
                                    fill="#113C4E" />
                            </svg>
                        </div>
                    </div>
                    <img class="bottom" src="../public/images/background/image2.png">

                </div>
            </div>
        </div>
    </section>
</template>
<style scoped>
section .grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 160px;
    align-items: center;
}

section .left>span {
    color: var(--color-primary);
    margin: 16px 0;
    margin-top: 0;
    display: block;
}

section h3 {
    margin: 0;
    line-height: 125%
}

section .left>p {
    margin-bottom: 40px;
}




/* profile */
section .profile {
    border: 1px solid var(--black-10, #E6E6E6);
    border-radius: 30px;
    display: grid;
    grid-template-columns: max-content 1fr;
    padding: 32px 23px;
    align-items: center;
    gap: 12px;
    margin-top: 41px;
}

.profile img {
    display: block;
    width: 65px;
    height: 65px;
    border: 2px solid white;
    border-radius: 50%;
    box-shadow: 0px 13px 23px 0px rgba(0, 0, 0, 0.15);
}

.profile p {
    margin: 0;
}

.profile span {
    background: var(--gradiant, linear-gradient(319deg, var(--color-primary) 0%, var(--color-secondary) 100%));
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin: 0;
    font-weight: 500px;
    display: block;
}

.profile p b {
    color: var(--color-on-surface);
}



/* right */

.right {
    position: relative;
    padding-left: 30px;
}

.right img {
    display: block;
}

.right .image-holder {
    position: relative;
    margin-bottom: 40px;
}

.right .holder {
    position: absolute;
    bottom: 0;
    left: 0;
    transform: translate(-40%, 40%);
    backdrop-filter: blur(10px);
    border-radius: 50%;
    background-color: rgba(226, 223, 223, 0.42);
}

.right .holder svg {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
}

.right .bottom {
    margin-left: auto;
    margin-right: 12px;
}





@media only screen and (max-width: 1100px) {
    section .grid {
        gap: 40px;

    }
}


@media only screen and (max-width: 900px) {
    section .grid {
        grid-template-columns: 100%
    }
}

@media only screen and (max-width: 600px) {

    .right .top {
        width: 60%;
    }

    .right{
        padding-left: 0;
    }

    .right .bottom {
        margin-left: auto;
        width: 90%;
    }

    .right .image-holder{
        margin-bottom: 25px;
    }

    .right .holder {
        display: none;
    }


}
</style>
<script setup lang='ts'>
</script>
<template>
    <section>
        <div class="page">
            <span>Emergency Situation</span>
            <h3>Meet Our Specialists</h3>
            <p>A Big & Dedicated Team of Experienced Pediatricians to provide Quality Healthcare.</p>
            <div class="profile-holder desktop">
                <div class="profile" style="top: 100px; left: 0;">
                    <img src="../public/images/profile/profile1.png">
                    <h4>Dr. Kashmira Solanki</h4>
                    <p>Neonatologist</p>
                </div>

                <div class="profile" style="top: 220px; right: 30%;">
                    <img src="../public/images/profile/profile2.png">
                    <h4>Dr. Pratik Shah</h4>
                    <p>Pediatric Intensivist</p>
                </div>

                <div class="profile" style="right: 50%; top: 0;">
                    <img src="../public/images/profile/profile3.png">
                    <h4>Dr. Sachin A. Shah</h4>
                    <p>Neonatologist</p>
                </div>

                <div class="profile" style="top: 200px; right: 0;">
                    <img src="../public/images/profile/profile4.png">
                    <h4>Dr Neeta C. Shah</h4>
                    <p>Chief Pathologist</p>
                </div>

                <div class="profile" >
                    <img src="../public/images/profile/profile5.png">
                    <h4>Dr Silky Modi</h4>
                    <p>Child Specialist</p>
                </div>

                <div class="profile" style="left: 50px; bottom: 50px;">
                    <img src="../public/images/profile/profile6.png">
                    <h4>Dr. Devarshi Patel</h4>
                    <p>Child Specialist</p>
                </div>

                <div class="profile" style="left: 40%; bottom: 0;">
                    <img src="../public/images/profile/profile7.png">
                    <h4>Dr. Chetan B. Shah</h4>
                    <p>MD (Pediatrics), DCH</p>
                </div>

                <div class="profile" style="right: 20px; bottom: 50px;">
                    <img src="../public/images/profile/profile8.png">
                    <h4>Dr. Charul J. Bhutwala</h4>
                    <p>Child Specialist</p>
                </div>
            </div>
        </div>

        <!-- outline -->
        <img src="../public/images/outline/shadow.png">
    </section>
</template>
<style scoped>
section{
    margin-top: 110px;
    position: relative;
}

.page>span{
    text-align: center;
    display: block;
    color: var(--color-primary);
}

section h3{
    text-align: center;
    margin: 0;
    margin-top: 18px;
    margin-bottom: 32px;
}

section .page>p{
    text-align: center;
}

section>img{
    position: absolute;
    z-index: -1;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;

}


/* profile */

.profile-holder.desktop{
    height: 800px;
    width: 100%;
    position: relative;
}

.desktop .profile{
    position: absolute;
    display: flex;
    flex-direction: column;
}
</style>
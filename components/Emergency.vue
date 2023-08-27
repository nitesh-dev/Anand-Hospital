<script setup lang='ts'>
</script>
<template>
    <section>
        <div class="page">
            <div class="grid">
                <div class="left">
                    <img src="../public/images/background/doctor2.png" alt="doctor">

                    <div class="service">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="25" viewBox="0 0 24 25" fill="none">
                            <path
                                d="M11.9008 2.64453C6.43629 2.64453 1.9834 7.09742 1.9834 12.5619C1.9834 18.0263 6.43629 22.4792 11.9008 22.4792C17.3652 22.4792 21.8181 18.0263 21.8181 12.5619C21.8181 7.09742 17.3652 2.64453 11.9008 2.64453ZM16.6412 10.2809L11.0181 15.904C10.8793 16.0429 10.6908 16.1222 10.4925 16.1222C10.2941 16.1222 10.1057 16.0429 9.96687 15.904L7.16026 13.0974C6.87265 12.8098 6.87265 12.3338 7.16026 12.0462C7.44786 11.7586 7.92389 11.7586 8.2115 12.0462L10.4925 14.3272L15.59 9.22965C15.8776 8.94205 16.3536 8.94205 16.6412 9.22965C16.9289 9.51726 16.9289 9.98337 16.6412 10.2809Z"
                                fill="#A8CF45" />
                        </svg>
                        <span>24 Hours Service</span>
                    </div>

                    <img class="pill" src="../public/images/icons/pill.png" alt="pill">
                </div>
                <div class="right">
                    <span>Emergency Situation</span>
                    <h3>Doctor's Schedule Day</h3>
                    <p>Anand Children Hospital is one of the largest Pediatric Super Specialty Hospital of South Gujarat
                        located at the center of the Surat City. It is the 1st Pediatric Hospital in Gujarat </p>

                    <div class="schedule">
                        <div>
                            <span>08.00 AM - 12.00 PM</span>
                            <span>Dr. Sachin A. Shah</span>
                        </div>
                        <div>
                            <span>12.00 PM - 03.00 PM</span>
                            <span>Dr. Sachin A. Shah</span>
                        </div>
                        <div>
                            <span>03.00 PM - 07.00 PM</span>
                            <span>Dr. Pratik Shah</span>
                        </div>
                        <div>
                            <span>07.00 PM - 11.00 PM</span>
                            <span>Dr. Neeta C. Shah</span>
                        </div>
                    </div>

                    <WidgetButton>
                        <span>Chat with doctor..</span>
                    </WidgetButton>
                </div>
            </div>
        </div>


        <!-- outline -->

        <img class="full-outline" src="../public/images/outline/lines.png">
    </section>
</template>
<style scoped>
section {
    position: relative;
}

.grid {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 135px;
    align-items: center;
}

.grid .left{
    position: relative;
}

.grid img {
    width: 100%;
}

section .right>span {
    color: var(--color-primary);
    display: block;
    margin-bottom: 10px;
}

section h3 {
    margin: 0;
    line-height: 125%
}


section p {
    margin: 32px 0;
}


section .schedule{
    margin-bottom: 38px;
}
section .schedule div {
    display: grid;
    grid-template-columns: 1fr 1fr;
    margin-bottom: 24px;
}

section .schedule div span:first-child {
    background: linear-gradient(319deg, #0098DA 0%, #A8CF45 100%);
    background-clip: text;
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    font-weight: 500;
}

/* service */
.left .service{
    position: absolute;
    right: 0;
    top: 150px;
    height: 57px;
    display: flex;
    align-items: center;
    border-radius: 50px;
    padding: 0 16px;
    background-color: white;
    z-index: 3;
    transform: translateX(40%);
    box-shadow: 0px 23px 34px 0px rgba(211, 211, 211, 0.60);
    gap: 8px;
}

.service svg{
    box-shadow: 0px 5px 11px 0px rgba(215, 237, 156, 0.56);
    border-radius: 50%;
}

.service span{
    display: block;
    color: var(--color-primary);
    font-weight: 500;

}


/* outline */
.full-outline {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
}

.left .pill{
    position: absolute;
    right: 0;
    bottom: 100px;
    z-index: 2;
    width: 71px;
    transform: translateX(60%);
}
</style>
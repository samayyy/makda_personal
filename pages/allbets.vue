<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div class="flexx1">
        <NuxtLink to="/home">
            <div class="back-icon" icon="akar-icons:arrow-left"></div>
        </NuxtLink>
    </div>
    <div class="head1">Open Bets</div>
    <div class="open">
        <div v-for="(value, index) in  card" :key="index" :data-index="index" class="card">
            <div class="d-flex justify-content-between ">
                <div class="name">{{value.name}}</div>
                <div class="time">{{value.startTime}}</div>
            </div>
            <div class="d-flex justify-content-end">
                <NuxtLink to="/games"><button class="button"><span class="btntext">View Bets</span></button></NuxtLink>
            </div>
            <div class="d-flex">
                <div class="text1 p">Open Sheet</div>
                <div class="text1 p"> Janatari</div>
                <div class="text1"> Harf</div>
            </div>
        </div>
    </div>
    <div v-if="isEmpty === 1">
        <p class="open card card2"><span class="text-center">You have not placed any bet yet</span></p>
    </div>
</div>
</template>

<script>
export default {
    name: 'Home4',
    data() {
        return {
            // card: {}
            card: [{
                    value: '',
                    name: 'Royal Rajasthan',
                    startTime: '07:30',
                    endTime: '08:30',
                    resultTime: '08:45',
                    status: 'live',
                },
                {
                    value: '',
                    name: 'Amravati Gold',
                    startTime: '08:30',
                    endTime: '09:30',
                    resultTime: '09:45',
                    status: 'live',

                },
                {
                    value: '',
                    name: 'Royal Rajasthan',
                    startTime: '05:30',
                    endTime: '07:15',
                    resultTime: '07:30',
                    status: 'expired',

                },
                {
                    value: '',
                    name: 'Amravati Gold',
                    startTime: '05:30',
                    endTime: '06:15',
                    resultTime: '06:30',
                    status: 'expired',

                },
                {
                    value: '',
                    name: 'Kashipur',
                    startTime: '05:30',
                    endTime: '06:15',
                    resultTime: '06:30',
                    status: 'expired',

                },

            ],

        }
    },
    computed: {
        isEmpty() {
            let count = 0;
            if (Object.keys(this.card).length === 0) {
                count = 1;
            }
            return count;
        }
    }
}
</script>

<style scoped>
.head1 {
    top: 40px;
    position: absolute;
    width: 108px;
    left: 0;
    right: 0;
    margin: auto;
    transform: translateY(-50%);
    text-align: center;
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 20px;
    line-height: 42px;
}

.open {
    position: absolute;
    top: 75px;
    left: 0;
    right: 0;
    margin: auto;
}

.card {
    max-width: 310px;
    width: 84vw;
    height: 104px;
    left: 0;
    right: 0;
    margin: auto;
    background: #FFFFFF;
    box-shadow: 0px 2px 12px rgba(0, 0, 0, 0.12);
    border-radius: 12px;
    padding: 10px 15px;
    margin-bottom: 15px;
}

.card2 {
    display: flex;
    justify-content: center !important;
}

.name {
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 27px;
    display: flex;
    align-items: center;
    color: #000000;
}

.time {
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 21px;
    display: flex;
    align-items: center;
    /* text-align: end; */
    color: #8E8E8E;
    padding-right: 5px;

}

.button {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 8px;
    width: 95px;
    height: 37px;
    background: #006CA9;
    border-radius: 20px;
    color: white !important;
    text-decoration: none !important;
}

.btntext {
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 21px;
    display: flex;
    align-items: center;
    color: #FFFFFF;
}

.text1 {
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 21px;
    display: flex;
    align-items: center;
    color: #767676;
}

.p {
    padding-right: 15px;
}

.button2 {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 8px;
    position: absolute;
    top: 820px;
    width: 304px;
    height: 37px;
    background: #006CA9;
    border-radius: 20px;
    margin-left: 15px;
    max-width: 400px;
    width: 84vw;
    /* left: 0;
    right: 0;
    margin: auto; */
}

.btntext2 {
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 21px;
    display: flex;
    align-items: center;
    color: #FFFFFF;
}
</style>

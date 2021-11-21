<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div class="align2">
        <div class="align">
            <div class="head1">Open Bets</div>
        </div>
    </div>

    <div v-if="isEmpty === 0">
        <div class="open">
            <div v-for="(value, index) in  1" :key="index" :data-index="index" class="card">
                <div class="d-flex justify-content-between">
                    <div class="name justify-self-start">{{card[index].name}}</div>
                    <div class="time justify-self-center">{{card[index].startTime}}</div>
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
        <div class="open">
            <NuxtLink to="/allbets"><button class="button2"><span class="btntext2">View All Bets</span></button></NuxtLink>
        </div>
    </div>
    <div v-if="isEmpty === 1">
        <div class="open">
        <p class="card card2"><span class="text-center">You have not placed any bet yet</span></p>
        </div>
        <button class="button2" type="button" disabled><NuxtLink to="/allbets"><span class="btntext2">View All Bets</span><NuxtLink to="/allbets"></button><NuxtLink to="/allbets">
    </div>

</div>
</template>

<script>
export default {
    name: 'Home4',
    data() {
        return {
            card: {}
            // card: [{
            //         value: '',
            //         name: 'Royal Rajasthan',
            //         startTime: '07:30',
            //         endTime: '08:30',
            //         resultTime: '08:45',
            //         status: 'live',
            //     },
            //     {
            //         value: '',
            //         name: 'Amravati Gold',
            //         startTime: '08:30',
            //         endTime: '09:30',
            //         resultTime: '09:45',
            //         status: 'live',

            //     },
            //     {
            //         value: '',
            //         name: 'Royal Rajasthan',
            //         startTime: '05:30',
            //         endTime: '07:15',
            //         resultTime: '07:30',
            //         status: 'expired',

            //     },
            //     {
            //         value: '',
            //         name: 'Amravati Gold',
            //         startTime: '05:30',
            //         endTime: '06:15',
            //         resultTime: '06:30',
            //         status: 'expired',

            //     },
            //     {
            //         value: '',
            //         name: 'Kashipur',
            //         startTime: '05:30',
            //         endTime: '06:15',
            //         resultTime: '06:30',
            //         status: 'expired',

            //     },

            // ],

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
.open {
    display: flex;
    justify-content: center;
    margin-left: -24px;
}

.head1 {
    padding-left: 12px;
    padding-top: 20px;
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 20px;
    line-height: 30px;
    display: flex;
    align-items: center;
    color: #000000;
}

.card {
    max-width: 400px;
    width: 84vw;
    height: 104px;
    margin-left: 12px;
    margin-top: 10px;
    background: #FFFFFF;
    box-shadow: 0px 2px 12px rgba(0, 0, 0, 0.12);
    border-radius: 12px;
    padding: 10px 15px;
}

.card2 {
    display: flex;
    justify-content: center !important;
}

.align2 {
    display: flex;
    justify-content: center;
    margin-left: -24px;

}

.align {
    max-width: 600px;
    width: 84vw;
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
    padding-right: 5px;
    color: #8E8E8E;

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

p {
    margin-bottom: 0 !important;
}

.button2 {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 8px;
    /* position: absolute; */
    margin-top: 25px;
    width: 304px;
    height: 37px;
    background: #006CA9;
    border-radius: 20px;
    margin-left: 15px;
    max-width: 400px;
    width: 84vw;
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

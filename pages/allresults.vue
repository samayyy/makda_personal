<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div class="flexx1">
        <NuxtLink to="/home">
            <div class="back-icon" icon="akar-icons:arrow-left"></div>
        </NuxtLink>
    </div>
    <div class="head1">All Results</div>
    <div class="results">
        <div v-for="(value, index) in  card.filter(card => card.date === '17/11/2021')" :key="index" :data-index="index" class="card">
            <div class="card-text">
                <div class="d-flex justify-content-around align-items-center">
                    <div class="inner">
                        <div class="name">{{value.city}}</div>
                        <div class="d-flex justify-content-between pt-1">
                            <div class="date">{{value.date}}</div>
                            <div class="time ">{{value.startTime}} to {{value.endTime}}</div>
                        </div>
                    </div>
                    <div class="circle" :class="{bg0: index%1==0, bg1: index%2==0, bg2: index%3 == 0,bg3: index%4==0}">{{value.number}}</div>
                </div>
            </div>
        </div>
    </div>
    <div v-if="isEmpty === 1">
        <p class="results card"><span class="text-center">No data found</span></p>
    </div>

    <NuxtLink to="/pastresults"><button :class="{button: isEmpty===0, button2: isEmpty===1}"><span class="btntext">VIew Past Results</span></button></NuxtLink>

</div>
</template>

<script>
export default {
    name: 'Allbets',
    data() {
        return {
            // card: []
            card: [{
                    value: '',
                    city: 'Bikaner',
                    number: '82',
                    startTime: '07:30',
                    endTime: '09:30',
                    date: '16/11/2021',

                },
                {
                    value: '',
                    city: 'Dishawar',
                    number: '42',
                    startTime: '12:30',
                    endTime: '2:30',
                    date: '17/11/2021',
                },
                {
                    value: '',
                    city: 'Haryana',
                    number: '17',
                    startTime: '4:30',
                    endTime: '6:30',
                    date: '17/11/2021',
                },
                {
                    value: '',
                    city: 'Mumbai',
                    number: '05',
                    startTime: '1:30',
                    endTime: '3:30',
                    date: '17/11/2021',
                },
                {
                    value: '',
                    city: 'Ahemdabad',
                    number: '26',
                    startTime: '9:00',
                    endTime: '11:00',
                    date: '16/11/2021',
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

.circle {
    width: 15vw;
    height: 15vw;
    max-width: 70px;
    max-height: 70px;
    min-width: 40px;
    min-height: 40px;
    font-family: Poppins;
    font-style: normal;
    font-weight: bold;
    font-size: 24px;
    line-height: 36px;
    display: flex;
    align-items: center;
    border-radius: 50%;
    color: black;
    text-align: center;
    justify-content: center;
}

.results {
    position: absolute;
    top: 75px;
    left: 0;
    right: 0;
    margin: auto;
}

.card {
    max-width: 400px;
    width: 84vw;
    height: 84px;
    left: 0;
    right: 0;
    margin: auto;
    background: #FFFFFF;
    box-shadow: 0px 2px 12px rgba(0, 0, 0, 0.12);
    border-radius: 12px;
    padding: 7px 10px;
    margin-bottom: 10px;
    justify-content: center !important;
}

.name {
    width: 76px;
    height: 27px;
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 27px;
    display: flex;
    align-items: center;
    color: #000000;
}

.date {
    /* width: 59px; */
    height: 18px;
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 12px;
    line-height: 18px;
    display: flex;
    align-items: center;
    color: #000000;
}

.time {
    width: 125px;
    height: 18px;
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 12px;
    line-height: 18px;
    display: flex;
    align-items: center;
    color: #000000;
    justify-content: flex-end;
}

.bg0 {
    background: #FF8585;
}

.bg1 {
    background: #FFE485;
}

.bg2 {
    background: #85DAFF;
}

.bg3 {
    background: #DF85FF;
}

.button {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 8px;
    position: absolute;
    left: 0;
    right: 0;
    margin: auto;
    width: 304px;
    height: 37px;
    top: 370px;
    background: #006CA9;
    border-radius: 20px;
}

.button2 {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 8px;
    position: absolute;
    left: 0;
    right: 0;
    margin: auto;
    width: 304px;
    height: 37px;
    top: 190px;
    background: #006CA9;
    border-radius: 20px;
}

.btntext {
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 21px;
    /* identical to box height */

    display: flex;
    align-items: center;

    color: #FFFFFF;
}

@media only screen and (max-width: 310px) {
    .circle {
        font-size: 20px;
    }
}
</style>

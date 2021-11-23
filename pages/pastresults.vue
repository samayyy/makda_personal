<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div class="flexx1">
        <NuxtLink to="/allresults">
            <div class="back-icon"></div>
        </NuxtLink>
    </div>
    <div class="head1">Past Results</div>
    <functional-calendar v-model="calendarData" :is-date-picker='true' :date-format="'dd/mm/yyyy'" class="calendar"></functional-calendar>
    <div class="results">

        <div v-for="(value, index) in  card.filter(card => card.date === calendarData.selectedDate)" :key="index" :data-index="index" class="card">
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
        <div v-if="isEmpty === 0">
            <p class="upcoming card"><span class="text-center">OOPS! No Game Found</span></p>
        </div>
    </div>
</div>
</template>

<script>
import {
    FunctionalCalendar
} from 'vue-functional-calendar';
export default {
    name: 'Pastresults',
    components: {
        FunctionalCalendar
    },
    data() {
        return {
            calendarData: {},
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
                    date: '18/11/2021',
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
            let count=0;
            if (Object.keys(this.calendarData).length === 0) {
                    count = 1;
                } 
            
            for (const i of this.card) {
                if (this.calendarData.selectedDate === i.date) {
                    count = count + 1;
                } 
                
            }
            return count;

        },
    }
}
</script>

<style scoped>
.head1 {
    padding-top: 60px;
    width: 200px;
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

.calendar {

    left: 0;
    right: 0;
    margin: auto;
    width: 90vw !important;
    max-width: 400px !important;
    border: 1px solid #27397D;
    box-sizing: border-box;
}

.vfc-week .vfc-day span.vfc-span-day.vfc-today {
    background-color: #006CA9 !important;
}

.vfc-week .vfc-day span.vfc-span-day.vfc-hover:hover,
.vfc-week .vfc-day span.vfc-span-day.vfc-hovered {
    background-color: #006CA9 !important;
    z-index: 100;
}

.vfc-week .vfc-day span.vfc-span-day.vfc-hover:hover {
    background-color: #006CA9 !important;
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
    padding-top: 25px;
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
/* 
.results2 {
    position: absolute;
    top: 600px;
} */
</style>

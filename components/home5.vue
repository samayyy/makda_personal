<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div class="align2">
        <div class="align">
            <div class="head2">Timed Out Games</div>
        </div>
    </div>
    <div class="justify">
        <div class="timed-out">
            <div v-for="(value, index) in  card.filter(card => card.status === 'expired')" :key="index" :data-index="index" class="card1">
                <div class="text-disabled">
                    <div class="d-flex justify-content-between">
                        <div class="name1 justify-self-start">{{value.name}}</div>
                        <div class="resultTime">{{value.resultTime}}</div>

                    </div>
                    <div class="time1 justify-self-end"> {{value.startTime}} to {{value.endTime}}</div>
                    <hr>
                </div>
                <br>
            </div>
            <div v-if="isEmpty2 === 0">
                <p class="n"><span class="text-center">No data found</span></p>
            </div>
        </div>
    </div>

</div>
</template>

<script>
export default {
    name: 'Home3',
    data() {
        return {
            card: [{
                    value: '',
                    name: 'Royal Rajasthan',
                    startTime: '07:30',
                    endTime: '08:30',
                    resultTime: '08:45',
                    status: 'expired',
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
                    status: 'live',

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
                    status: 'live',

                },

            ],

        }
    },
    computed: {
        isEmpty() {
            let count = 0;
            for (const i of this.card) {
                if (i.status === 'live') {
                    count = count + 1;
                }
            }
            return count;
        },
        isEmpty2() {
            let count = 0;
            for (const i of this.card) {
                if (i.status === 'expired') {
                    count = count + 1;
                }
            }
            return count;
        },
    }
}
</script>

<style scoped>
.head2 {
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

.timed-out {
    padding-left: 12px;
    padding-top: 10px;
    display: flex;
    justify-content: center;
    flex-direction: column;
}

.name1 {
    /* width: 148px; */
    height: 27px;
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 21px;
    line-height: 27px;
    display: flex;
    align-items: center;
    color: #ABABAB;
    padding-right: 24vw;
}

.n {
    height: 27px;
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-weight: 500;
    font-size: 21px;
    line-height: 27px;
    display: flex;
    align-items: center;
    color: #ABABAB;
}

.resultTime {
    /* width: 53px; */
    height: 21px;
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 18px;
    line-height: 21px;
    display: flex;
    align-items: center;
    color: #CACACA;
}

.time1 {
    width: 122px;
    height: 21px;
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 21px;
    display: flex;
    align-items: center;
    color: #ABABAB;
    padding-top: 15px;
}

.justify {
    display: flex;
    justify-content: center;
    left: 0;
    right: 0;
    margin: auto;
    margin-left: -24px;
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
</style>

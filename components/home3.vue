<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div class="align2">
        <div class="align">
            <div class="head1">Upcoimg Games</div>
        </div>
    </div>
    <div class="upcoming">
        <div class="scrolling-wrapper">

            <div v-for="(value, index) in  card.filter(card => card.status === 'live')" :key="index" :data-index="index" class="card">
                <div class="card-text">
                    <div class="starttime">{{value.startTime}}</div>
                    <div class="name">{{value.name}}</div>
                    <div class="time">{{value.startTime}}-{{value.endTime}}</div>
                    <NuxtLink to="/games"><button class="button"><span class="btntext">Play</span></button></NuxtLink>
                </div>
            </div>

        </div>
        <div v-if="isEmpty === 0">
            <p class="card2"><span class="text-center">No live games at the moment. Come back later!</span></p>
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
.scrolling-wrapper {
    padding-top: 10px;
    overflow-x: scroll;
    overflow-y: hidden;
    white-space: nowrap;
}

.scrolling-wrapper .card {
    display: inline-block;
    margin-right: 10px;
}

.scrolling-wrapper::-webkit-scrollbar {
    display: none;
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

.upcoming {
    padding-left: 12px;
    display: flex;
    justify-content: center;
}

.card {
    max-width: 160px;
    max-height: 160px;
    width: 42vw;
    height: 40vw;
    background: #FFFFFF;
    box-shadow: 0px 2px 12px rgba(0, 0, 0, 0.12);
    border-radius: 20px;
    margin-right: 5px;
}

.starttime {
    width: 53px;
    height: 21px;
    padding-top: 20px;
    padding-left: 10px;
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 21px;
    display: flex;
    align-items: center;
    color: #000000;
}

.name {
    width: 148px;
    height: 27px;
    padding-left: 10px;
    padding-top: 20px;
    font-weight: 500;
    font-size: 16px;
    line-height: 27px;
    display: flex;
    align-items: center;
    color: #000000;
}

.time {
    width: 160px;
    height: 21px;
    padding-top: 20px;
    font-family: Poppins;
    font-style: normal;
    font-weight: normal;
    font-size: 14px;
    line-height: 21px;
    display: flex;
    align-items: center;
    color: #737373;
    justify-content: center;
}

.button {
    width: 120px;
    height: 40px;
    background: #006CA9;
    border-radius: 20px;
    margin-top: 20px;
    display: flex;
    align-items: center;
    color: white;
    justify-content: center;
    margin-left: 20px;
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

@media only screen and (max-width: 400px) {
    .starttime {
        width: 53px;
        height: 21px;
        padding-top: 10px;
        padding-left: 10px;
        font-weight: 500;
        font-size: 14px;
        line-height: 21px;
    }

    .name {
        width: 148px;
        height: 27px;
        padding-left: 10px;
        padding-top: 10px;
        font-size: 16px;
        line-height: 27px;
    }

    .time {
        width: 40vw;
        height: 21px;
        padding-top: 10px;
        font-size: 14px;
        line-height: 21px;
    }

    .button {
        width: 30vw;
        height: 10vw;
        margin-top: 10px;
        margin-left: 5vw;
    }
}

@media only screen and (max-width: 320px) {
    .name {
        font-size: 12px;
    }
}

.justify {
    display: flex;
    justify-content: center;
    left: 0;
    right: 0;
    margin: auto;
    margin-left: -24px;
}

.card2 {
    max-width: 400px;
    max-height: 160px;
    width: 84vw;
    height: 35vw;
    background: #FFFFFF;
    box-shadow: 0px 2px 12px rgba(0, 0, 0, 0.12);
    border-radius: 20px;
    margin-right: 5px;
    display: flex;
    justify-content: center;
    align-items: center;
    margin-top: 10px;
    margin-bottom: 0 !important;
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

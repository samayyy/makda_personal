<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div class="head1">Upcoimg Games</div>
    <div class="upcoming d-flex">
        <div v-for="(value, index) in  card.filter(card => card.status === 'live')"  :key="index" :data-index="index" class="card">
            <div class="card-text">
                <div class="starttime">{{value.startTime}}</div>
                <div class="name">{{value.name}}</div>
                <div class="time">{{value.startTime}}-{{value.endTime}}</div>
                <NuxtLink to="/games"><button class="button"><span class="btntext">Play</span></button></NuxtLink>
            </div>
        </div>
    </div>
    <div class="head2">Timed Out Games</div>
    <div class="timed-out d-flex">
        <div v-for="(value, index) in  card.filter(card => card.status === 'expired')"  :key="index" :data-index="index" class="card1">
        <div class="card-text">
                <div class="starttime1">{{value.startTime}}</div>
                <div class="name2">{{value.name}}</div>
                <div class="time2">{{value.startTime}}-{{value.endTime}}</div>
                <NuxtLink to="/games"><button class="button1"><span class="btntext">Play</span></button></NuxtLink>
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
                    status: 'live',
                },
                {
                    value: '',
                    name: 'Amravati Gold',
                    number: '42',
                    startTime: '08:30',
                    endTime: '09:30',
                    status: 'live',

                },
                {
                    value: '',
                    name: 'Royal Rajasthan',
                    startTime: '07:30',
                    endTime: '08:30',
                    status: 'expired',

                },
                {
                    value: '',
                    name: 'Amravati Gold',
                    number: '42',
                    startTime: '08:30',
                    endTime: '09:30',
                    status: 'expired',

                },

            ],

        }
    },
    // computed: {
    //     card: function () {
    //         return this.info.filter(i => i.status === 'live')
    //     },
    // }
}
</script>

<style scoped>
.head1 {
    position: absolute;
    height: 30px;
    padding-left: 12px;
    top: 445px;
    height: 30px;
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 20px;
    line-height: 30px;
    display: flex;
    align-items: center;
    color: #000000;
}
.head2 {
    position: absolute;
    height: 30px;
    padding-left: 12px;
    top: 680px;
    height: 30px;
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
    position: absolute;
    padding-left: 12px;
    top: 491px;
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
    /* padding-left: 10px; */
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










.timed-out {
    position: absolute;
    padding-left: 12px;
    top: 730px;
}

.card1 {
    max-width: 160px;
    max-height: 160px;
    width: 42vw;
    height: 40vw;
    background: #FFFFFF;
    box-shadow: 0px 2px 12px rgba(0, 0, 0, 0.12);
    border-radius: 20px;
    margin-right: 5px;
}

.starttime1 {
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

.name1 {
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

.time1 {
    width: 160px;
    height: 21px;
    /* padding-left: 10px; */
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

.button1 {
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

@media only screen and (max-width: 400px) {
    .starttime1 {
        width: 53px;
        height: 21px;
        padding-top: 10px;
        padding-left: 10px;
        font-weight: 500;
        font-size: 14px;
        line-height: 21px;
    }

    .name1 {
        width: 148px;
        height: 27px;
        padding-left: 10px;
        padding-top: 10px;
        font-size: 16px;
        line-height: 27px;
    }

    .time1 {
        width: 40vw;
        height: 21px;
        padding-top: 10px;
        font-size: 14px;
        line-height: 21px;
    }

    .button1 {
        width: 30vw;
        height: 10vw;
        margin-top: 10px;
        margin-left: 5vw;
    }
}

</style>

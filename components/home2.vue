<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div class="pos1">
        <div class="scrolling-wrapper">
            <div v-for="(value, index) in  card" :key="index" :data-index="index" class="card" :class="{bg0: index%1==0, bg1: index%2==0, bg2: index%3 == 0,bg3: index%4==0}">
                <div class="card-text number">{{value.number}}</div>
                <div class="card-text city">{{value.city}}</div>
                <div class="card-text time">{{value.startTime}} - {{value.endTime}}</div>

            </div>
        </div>

    </div>
</div>
</template>

<script>
export default {
    name: 'Home',
    data() {
        return {
            card: [{
                    value: '',
                    city: 'Bikaner',
                    number: '82',
                    startTime: '07:30',
                    endTime: '09:30',
                },
                {
                    value: '',
                    city: 'Dishawar',
                    number: '42',
                    startTime: '12:30',
                    endTime: '2:30',
                },
                {
                    value: '',
                    city: 'Haryana',
                    number: '17',
                    startTime: '4:30',
                    endTime: '6:30',
                },
                {
                    value: '',
                    city: 'Mumbai',
                    number: '05',
                    startTime: '1:30',
                    endTime: '3:30',
                },
                {
                    value: '',
                    city: 'Ahemdabad',
                    number: '26',
                    startTime: '9:00',
                    endTime: '11:00',

                },

            ],
            
        }
    }
}
</script>

<style scoped>
.scrolling-wrapper {
    padding-top: 50px;
    overflow-x: scroll;
    overflow-y: hidden;
    white-space: nowrap;
}

.scrolling-wrapper .card {
    display: inline-block;
    margin-right: 10px;
}

.bg0 {
    width: 100px;
    height: 120px;
    background: #FF8585;
    box-shadow: 0px 2px 12px rgba(0, 0, 0, 0.12);
    border-radius: 10px;
}

.bg1 {
    width: 100px;
    height: 120px;
    background: #FFE485;
    box-shadow: 0px 2px 12px rgba(0, 0, 0, 0.12);
    border-radius: 10px;
}

.bg2 {
    width: 100px;
    height: 120px;
    background: #85DAFF;
    box-shadow: 0px 2px 12px rgba(0, 0, 0, 0.12);
    border-radius: 10px;
}

.bg3 {
    width: 100px;
    height: 120px;
    background: #DF85FF;
    box-shadow: 0px 2px 12px rgba(0, 0, 0, 0.12);
    border-radius: 10px;
}

.card {
    width: 100px;
    height: 120px;
    box-shadow: 0px 2px 12px rgba(0, 0, 0, 0.12);
    border-radius: 10px;
}

.scrolling-wrapper::-webkit-scrollbar {
    display: none;
}

.number {
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 24px;
    line-height: 36px;
    justify-content: center;
    padding-top: 20px;
    display: flex;
    align-items: center;
    color: #3F3F3F;
}

.city {
    font-family: Poppins;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 24px;
    justify-content: center;
    padding-top: 5px;
    display: flex;
    align-items: center;
    color: #3F3F3F;
}

.time {
    padding-top: 5px;
    font-family: Poppins;
    font-style: normal;
    font-weight: normal;
    font-size: 12px;
    line-height: 18px;
    display: flex;
    align-items: center;
    color: #3F3F3F;
    justify-content: center;
}
</style>

<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div class="flexx1">
        <NuxtLink to="/home">
            <Icon class="back-icon" icon="akar-icons:arrow-left" />
        </NuxtLink>
    </div>
    <div class="head1">Past Results</div>
    <functional-calendar v-model="calendarData"  :is-date-picker='true' :date-format="'dd/mm/yyyy'" class="calendar"></functional-calendar>
</div>
</template>

<script>
import {
    Icon
} from '@iconify/vue2';
import {
    FunctionalCalendar
} from 'vue-functional-calendar';
export default {
    name: 'Pastresults',
    components: {
        Icon,
        FunctionalCalendar
    },
    data() {
        return {
            calendarData: {}
        }
    }
}
</script>

<style scoped>
.back-icon {
    position: absolute;
    width: 25px;
    height: 25px;
    left: 27px;
    top: 30px;
}

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

.calendar {
    position: absolute;
    top: 75px;
    left: 0;
    right: 0;
    margin: auto;
    width: 90vw !important;
}
</style>

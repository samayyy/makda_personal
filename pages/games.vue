<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div class="d-flex justify-content-between align-items-center pos">
        <NuxtLink to="/home">
            <Icon class="back-icon" icon="akar-icons:arrow-left" />
        </NuxtLink>
    <div class="head1">Game</div>
            <Icon class="back-icon" icon="akar-icons:arrow-left" color="white"/>
    </div>
        <v-tabs v-model="tab" slider-size="5" class="d-flex justify-content-center pos1">
            <v-tabs-slider color="#006CA9"></v-tabs-slider>
            <!-- <v-tab > Open SHeet</v-tab>
            <v-tab >Jantari</v-tab>
            <v-tab >Harf</v-tab> -->
            <v-tab v-for="item in items" :key="item">
                {{ item }}
            </v-tab>
        </v-tabs>
        <v-tabs-items v-model="tab" light>
            <v-tab-item  v-for="item in items" :key="item">
                <div v-if="item==='Open Sheet'">
                <opensheet />
                </div>
                <div v-if="item==='Harf'">
                    <harf />
                </div>
                <div v-if="item==='Jantari'">
                    <jantari />
                </div>
            </v-tab-item>
        </v-tabs-items>

</div>
</template>

<script>
import {
    Icon
} from '@iconify/vue2';
import harf from '../components/harf'
import opensheet from '../components/opensheet'
import jantari from '../components/jantari'
export default {
    name: 'Games',
    components: {
        Icon,
        harf,opensheet,jantari
    },
    data() {
        return {
            tab: null,
            items: [
                'Open Sheet', 'Jantari', 'Harf'
            ],

        }
    },
}
</script>

<style scoped>

.back-icon {
    width: 25px;
    height: 25px;

}

.head1 {
    text-align: center;
    margin-left: -12px;
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 20px;
    line-height: 42px;
}

.v-slide-group__content {
    display: flex;
    flex: 1 0 auto;
    position: relative;
    transition: 0.3s cubic-bezier(0.25, 0.8, 0.5, 1);
    white-space: nowrap;
    font-family: Nunito Sans;
    font-style: normal;
    font-weight: bold;
    font-size: 16px;
    line-height: 22px;
    color: #0E0E0E;
}
.pos{
    padding-top: 15px;
    padding-left: 12px;
}
.pos1{
    margin-top: 20px;
}
</style>

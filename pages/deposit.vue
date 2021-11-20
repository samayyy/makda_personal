<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div class="d-flex justify-content-between align-items-center pos">
        <NuxtLink to="/home">
            <div class="back-icon2" icon="akar-icons:arrow-left"></div>
        </NuxtLink>
        <div class="head1">Wallet</div>
        <div class="back-icon3" icon="akar-icons:arrow-left"></div>
    </div>
    <v-tabs v-model="tab" slider-size="5" class="d-flex justify-content-center pos1">
        <v-tabs-slider color="#006CA9"></v-tabs-slider>
        <v-tab v-for="item in items" :key="item">
            {{ item }}
        </v-tab>
    </v-tabs>
    <v-tabs-items v-model="tab" light>
        <v-tab-item v-for="item in items" :key="item">
            <div v-if="item==='Bank Transfer'">
                <banktransfer />
            </div>
            <div v-if="item==='Payment Gateway'">
                <paymentgateway />
            </div>
        </v-tab-item>
    </v-tabs-items>
</div>
</template>

<script>
export default {
    name: 'Withdraw',
    data() {
        return {
            tab: null,
            items: [
                'Bank Transfer', 'Payment Gateway'
            ],

        }
    },
}
</script>

<style scoped>
.head1 {
    text-align: center;
    margin-left: -12px;
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 20px;
    line-height: 42px;
}

.back-icon3 {
    width: 25px;
    height: 25px;
    background: url('data:image/svg+xml,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20xmlns%3Axlink%3D%22http%3A%2F%2Fwww.w3.org%2F1999%2Fxlink%22%20width%3D%221em%22%20height%3D%221em%22%20preserveAspectRatio%3D%22xMidYMid%20meet%22%20viewBox%3D%220%200%2024%2024%22%3E%3Cpath%20fill%3D%22white%22%20d%3D%22M19%2011H7.14l3.63-4.36a1%201%200%201%200-1.54-1.28l-5%206a1.19%201.19%200%200%200-.09.15c0%20.05%200%20.08-.07.13A1%201%200%200%200%204%2012a1%201%200%200%200%20.07.36c0%20.05%200%20.08.07.13a1.19%201.19%200%200%200%20.09.15l5%206A1%201%200%200%200%2010%2019a1%201%200%200%200%20.64-.23a1%201%200%200%200%20.13-1.41L7.14%2013H19a1%201%200%200%200%200-2z%22%2F%3E%3C%2Fsvg%3E');
    background-repeat: no-repeat;
    background-size: 100%;
}

.pos {
    padding-top: 15px;
    padding-left: 12px;
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

.pos1 {
    margin-top: 20px;
}
</style>

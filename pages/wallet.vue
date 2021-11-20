<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div class="d-flex justify-content-between align-items-center pos">
        <NuxtLink to="/home">
            <div class="back-icon2" icon="akar-icons:arrow-left"></div>
        </NuxtLink>
        <div class="head1">Wallet</div>
        <div class="back-icon3" icon="akar-icons:arrow-left" color="white"></div>
    </div>
    <div class="section1">
        <div class="d-flex justify-content-center align-items-center">
            <div class="icon"></div>
            <div class="amount">$14000.00</div>
        </div>
        <div class="availablefunds">Available funds</div>
    </div>
    <div class="section2">
        <div class="d-flex justify-content-center">
            <NuxtLink to="/deposit"><button class="button">
                <div class="bg"></div><span class="btntext">Deposit</span>
            </button></NuxtLink>
            <NuxtLink to="/withdraw"><button class="button2">
                <div class="bg2"></div><span class="btntext2">Withdraw</span>
            </button></NuxtLink>
        </div>

    </div>
</div>
</template>

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

.icon {
    width: 53px;
    height: 53px;
    background: url('data:image/svg+xml,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20xmlns%3Axlink%3D%22http%3A%2F%2Fwww.w3.org%2F1999%2Fxlink%22%20width%3D%2253%22%20height%3D%2253%22%20preserveAspectRatio%3D%22xMidYMid%20meet%22%20viewBox%3D%220%200%2024%2024%22%3E%3Cg%20fill%3D%22none%22%3E%3Cpath%20d%3D%22M3%205v12.75A3.25%203.25%200%200%200%206.25%2021h12a3.25%203.25%200%200%200%203.25-3.25v-8.5A3.251%203.251%200%200%200%2019%206.087V5.25A2.25%202.25%200%200%200%2016.75%203H5.25a2.25%202.25%200%200%200-2.236%202H3zm2.25%201a.75.75%200%200%201%200-1.5h11.5a.75.75%200%200%201%20.75.75V6H5.25zm11%207h2a.75.75%200%200%201%200%201.5h-2a.75.75%200%200%201%200-1.5z%22%20fill%3D%22%23006ca9%22%2F%3E%3C%2Fg%3E%3C%2Fsvg%3E');
    background-repeat: no-repeat;
    background-size: 100%;
}

.amount {
    width: 183px;
    height: 54px;
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 30px;
    line-height: 54px;
    color: #303030;
    text-align: center;
}

.section1 {
    margin-top: 25px;
}

.availablefunds {
    padding-top: 20px;
    width: 158px;
    height: 30px;
    font-family: Poppins;
    font-style: normal;
    font-weight: normal;
    font-size: 20px;
    line-height: 30px;
    color: #111111;
    display: flex;
    justify-content: center;
    left: 0;
    right: 0;
    margin: auto;
}

.section2 {
    padding-top: 25px;
    margin-left: 5px;
}

.button {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    width: 148px;
    height: 46px;
    background: #006CA9;
    border-radius: 20px;
    left: 0;
    right: 0;
    margin: auto;
    margin-top: 40px;
    margin-right: 5px;

}

.btntext {
    /* width: 69px; */
    height: 27px;
    font-family: Nunito;
    font-style: normal;
    font-weight: 600;
    font-size: 18px;
    line-height: 27px;
    color: #FFFFFF;
    padding-left: 5px;

}

.bg {
    width: 25px;
    height: 25px;
    background: url('data:image/svg+xml,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20xmlns%3Axlink%3D%22http%3A%2F%2Fwww.w3.org%2F1999%2Fxlink%22%20width%3D%2225%22%20height%3D%2225%22%20preserveAspectRatio%3D%22xMidYMid%20meet%22%20viewBox%3D%220%200%2024%2024%22%3E%3Cg%20fill%3D%22none%22%3E%3Cpath%20d%3D%22M12%208v4m0%200v4m0-4h4m-4%200H8%22%20stroke%3D%22white%22%20stroke-width%3D%222%22%20stroke-linecap%3D%22round%22%2F%3E%3Ccircle%20cx%3D%2212%22%20cy%3D%2212%22%20r%3D%2210%22%20stroke%3D%22white%22%20stroke-width%3D%222%22%2F%3E%3C%2Fg%3E%3C%2Fsvg%3E');
    background-size: 100%;
    background-repeat: no-repeat;
}

.bg2 {
    width: 25px;
    height: 25px;
    background: url('data:image/svg+xml,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20xmlns%3Axlink%3D%22http%3A%2F%2Fwww.w3.org%2F1999%2Fxlink%22%20width%3D%2253%22%20height%3D%2253%22%20preserveAspectRatio%3D%22xMidYMid%20meet%22%20viewBox%3D%220%200%2024%2024%22%3E%3Cg%20fill%3D%22none%22%3E%3Cpath%20d%3D%22M16%2012H8%22%20stroke%3D%22%23006ca9%22%20stroke-width%3D%222%22%20stroke-linecap%3D%22round%22%2F%3E%3Ccircle%20cx%3D%2212%22%20cy%3D%2212%22%20r%3D%2210%22%20stroke%3D%22%23006ca9%22%20stroke-width%3D%222%22%2F%3E%3C%2Fg%3E%3C%2Fsvg%3E');
    background-size: 100%;
    background-repeat: no-repeat;
}

.button2 {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    width: 148px;
    height: 46px;
    background: white;
    border: 1px solid #006CA9;
    border-radius: 20px;
    left: 0;
    right: 0;
    margin: auto;
    margin-top: 40px;
}

.btntext2 {
    /* width: 85px; */
    height: 27px;
    font-family: Nunito;
    font-style: normal;
    font-weight: 600;
    font-size: 18px;
    line-height: 27px;
    color: #006CA9;

    padding-left: 5px;

}
</style>

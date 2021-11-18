<template>
<div>
    <div class="jantari">
        <div class="text1">Andar</div>
        <div class="d-flex justify-content-around">
            <div class="num">00</div>
            <div class="num">01</div>
            <div class="num">02</div>
            <div class="num">03</div>
            <div class="num">04</div>

        </div>
        <div class="d-flex justify-content-around ">
            <div v-for="index in 5" :key="index">
                <input class="input" />
            </div>

        </div>
        <div class="d-flex justify-content-around p">
            <div class="num">05</div>
            <div class="num">06</div>
            <div class="num">07</div>
            <div class="num">08</div>
            <div class="num">09</div>
        </div>
        <div class="d-flex justify-content-around ">
            <div v-for="index in 5" :key="index">
                <input class="input" />
            </div>
        </div>
    </div>
    <div class="jantari">
        <div class="text1 ">Bahar</div>
        <div class="d-flex justify-content-around">
            <div class="num">00</div>
            <div class="num">01</div>
            <div class="num">02</div>
            <div class="num">03</div>
            <div class="num">04</div>

        </div>
        <div class="d-flex justify-content-around ">
            <div v-for="index in 5" :key="index">
                <input class="input" />
            </div>

        </div>
        <div class="d-flex justify-content-around p">
            <div class="num">05</div>
            <div class="num">06</div>
            <div class="num">07</div>
            <div class="num">08</div>
            <div class="num">09</div>
        </div>
        <div class="d-flex justify-content-around ">
            <div v-for="index in 5" :key="index">
                <input class="input" />
            </div>
        </div>
        <div class="bottom">
            <div class="text2"><span>TOTAL: 0</span></div>
            <NuxtLink to=/games><button class="button"><span class="btntext">Submit</span></button></NuxtLink>
        </div>
    </div>
</div>
</template>

<style scoped>
.jantari {
    padding-top: 25px;
    left: 0;
    right: 0;
    margin: auto;
    margin-left: 12px;
    margin-right: 12px;
}

.text1 {
    width: 58px;
    height: 27px;
    margin-left: 12px;
    font-family: Nunito;
    font-style: normal;
    font-weight: bold;
    font-size: 20px;
    line-height: 27px;
    color: #000000;
    margin-bottom: 25px;
}

.num {
    width: 25px;
    height: 22px;
    font-family: Nunito;
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 22px;
    color: #000000;
    display: flex;
    justify-content: center;
}

.input {
    width: 25px;
    height: 22px;
    border-bottom: 1px solid black !important;
    display: flex;
    justify-content: center;
}

input {
    font-family: Nunito;
    font-style: normal;
    font-weight: 600;
    font-size: 16px !important;
    line-height: 22px;
    color: #000000;
    text-align: center;
}

textarea:focus,
input:focus {
    outline: none;
}

.p {
    padding-top: 22px;
}

.bottom {
    padding-top: 25px;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
}

.text2 {
    height: 27px;
    font-family: Nunito;
    font-style: normal;
    font-weight: bold;
    font-size: 20px;
    line-height: 27px;
    color: #000000;
}

.button {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 8px;
    width: 90vw;
    max-width: 330px;
    height: 40px;
    background: #006CA9;
    border-radius: 20px;
    color: white !important;
    text-decoration: none !important;
    margin-top: 20px;
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
</style>

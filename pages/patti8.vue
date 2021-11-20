<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div class="d-flex justify-content-between align-items-center pos">
        <NuxtLink to="/home">
            <div class="back-icon2" icon="akar-icons:arrow-left"></div>
        </NuxtLink>
        <div class="head1">Game</div>
        <div class="back-icon3" icon="akar-icons:arrow-left" color="white"></div>
    </div>
    <div class="head2">8 PATTI</div>
    <div class="patti8">
        <div class="d-flex justify-content-center p">
            <div v-for="(items,i) in patti8.slice(0, 4)" :key="i">
                <div class="num">{{items.num}}</div>
            </div>
        </div>
        <div class="d-flex justify-content-center ">
            <div v-for="(items,index) in patti8.slice(0, 4)" :key="index">
                <input v-model="items.value" type="number" class="input" />
            </div>
        </div>
        <div class="d-flex justify-content-center p">
            <div v-for="(items,i) in patti8.slice(4,8)" :key="i">
                <div class="num">{{items.num}}</div>
            </div>
        </div>
        <div class="d-flex justify-content-center ">
            <div v-for="(items,index) in patti8.slice(4, 8)" :key="index">
                <input v-model="items.value" type="number" class="input" />
            </div>
        </div>
    </div>
    <div class="bottom">
        <div class="text2"><span>TOTAL:  &#8377;{{total}}</span></div>
        <button class="button" @click="func"><span class="btntext">Submit</span></button>
    </div>
    <div v-if="total>0">
    <div v-show="modal_1" class="c-modal flexxx">
        <div class="modalhead">Congratulations</div>
        <div class="modaltext">Your bet has been placed</div>
        <button type="submit" class="button3" @click="func2();"><span class="btntext3">Continue</span></button>

    </div>
    <div v-show="modal_1" class="bg2" @click="func2();"></div>
    </div>
</div>
</template>

<script>
export default {
    name: 'Patti',
    data() {
        return {
            patti8: [{
                    num: '01',
                    value: ""
                },
                {
                    num: '02',
                    value: ""
                },
                {
                    num: '03',
                    value: ""
                },
                {
                    num: '04',
                    value: ""
                },
                {
                    num: '05',
                    value: ""
                },
                {
                    num: '06',
                    value: ""
                },
                {
                    num: '07',
                    value: ""
                },
                {
                    num: '08',
                    value: ""
                },
            ],
            modal_1: false,
        }
    },
    computed: {
        total() {
            let value = 0;
            for (const field of this.patti8) {
                value = parseInt(value, 10) + parseInt((field.value || 0), 10)
            }
            return value;
        }
    },
    methods:{
        func() {
            if (this.total > 0) {
                this.modal_1 = !this.modal_1
            }

        },
        func2() {
            if (this.total > 0) {
                 this.modal_1 = !this.modal_1
                for (const field of this.patti8) {
                    field.value = "";
                }
            }
        }
    }
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

.pos {
    padding-top: 15px;
    padding-left: 12px;
}

.pos1 {
    margin-top: 20px;
}

.head2 {
    padding-top: 20px;
    width: 100px;
    font-family: Nunito Sans;
    font-style: normal;
    font-weight: 600;
    font-size: 22px;
    line-height: 30px;
    color: #000000;
    display: flex;
    left: 0;
    right: 0;
    margin: auto;
    display: flex;
    justify-content: center;
}

.patti8 {
    padding-top: 25px;
    left: 0;
    right: 0;
    margin: auto;
    margin-left: 32px !important;
    margin-right: 12px !important;
}

.num {
    width: 40px;
    height: 22px;
    font-family: Nunito;
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 22px;
    color: #000000;
    display: flex;
    justify-content: center;
    margin-right: 20px;
}

.input {
    width: 40px;
    height: 22px;
    border-bottom: 1px solid black !important;
    display: flex;
    justify-content: center;
    margin-right: 20px;

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
    margin-top: 30px;
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
.c-modal {
    position: fixed;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    margin: auto;
    width: 70%;
    max-width: 300px;
    height: 246px;
    padding: 12px;
    background-color: white;
    border-radius: 5px;
    /* background-color: rgba(#fff, .4); */
    z-index: 10001;
    opacity: 1;
    transition: .6s;
}

.flexxx {
    display: flex;
    flex-direction: column;
    justify-content: space-evenly;
    align-items: center;
}

.modalhead {
    width: 203px;
    height: 38px;
    font-family: Nunito;
    font-style: normal;
    font-weight: 600;
    font-size: 28px;
    line-height: 38px;
    color: #000000;
}

.modaltext {
    width: 202px;
    height: 25px;
    font-family: Nunito;
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 25px;
    color: #4D4D4D;

}
.button3 {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 8px;
    width: 80%;
    max-width: 220px;
    height: 40px;
    background: #006CA9;
    border-radius: 20px;
    color: white !important;
    text-decoration: none !important;
}

.btntext3 {
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 21px;
    color: #FFFFFF;
}

.bg2 {
    display: block;
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: rgba(0, 0, 0, .6);
    z-index: 10000;
    opacity: 1;
    transition: .3s;
}
@media only screen and (max-width: 320px){
    .c-modal{
        width: 90%;
    }
}
</style>

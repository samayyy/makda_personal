<template>
<div>
    <form @submit.prevent="submit">
        <div class="jantari">
            <div class="row justify-content-center">
                <div v-for="(items,i) in jantari" :key="i" class="col-2 justify-content-center">
                    <div>
                        <div class="num">{{items.num}}</div>
                        <input v-model="items.value" type="number" class="input " />
                    </div>
                </div>
            </div>

        </div>
    </form>
    <div class="bottom">
        <div class="text2"><span>TOTAL: {{total}}</span></div>
        <button class="button" @click="func"><span class="btntext">Submit</span></button>
    </div>
    <div v-if="total>0">
    <div v-show="modal_1" class="c-modal flexxx">
        <div class="modalhead">Congratulations</div>
        <div class="modaltext">Your bet has been placed</div>
        <button type="submit" class="button3" @click="modal_1=!modal_1"><span class="btntext3">Continue</span></button>

    </div>
    <div v-show="modal_1" class="bg2" @click="modal_1=!modal_1"></div>
    </div>

</div>
</template>

<script>
export default {
    name: 'Jantari',
    data() {
        return {
            jantari: [{
                    num: 1,
                    value: ""
                },
                {
                    num: 2,
                    value: ""
                },
                {
                    num: 3,
                    value: ""
                },
                {
                    num: 4,
                    value: ""
                },
                {
                    num: 5,
                    value: ""
                },
                {
                    num: 6,
                    value: ""
                },
                {
                    num: 7,
                    value: ""
                },
                {
                    num: 8,
                    value: ""
                },
                {
                    num: 9,
                    value: ""
                },
                {
                    num: 10,
                    value: ""
                },
                {
                    num: 11,
                    value: ""
                },
                {
                    num: 12,
                    value: ""
                },
                {
                    num: 13,
                    value: ""
                },
                {
                    num: 14,
                    value: ""
                },
                {
                    num: 15,
                    value: ""
                },
                {
                    num: 16,
                    value: ""
                },
                {
                    num: 17,
                    value: ""
                },
                {
                    num: 18,
                    value: ""
                },
                {
                    num: 19,
                    value: ""
                },
                {
                    num: 20,
                    value: ""
                },
                {
                    num: 21,
                    value: ""
                },
                {
                    num: 22,
                    value: ""
                },
                {
                    num: 23,
                    value: ""
                },
                {
                    num: 24,
                    value: ""
                },
                {
                    num: 25,
                    value: ""
                },
                {
                    num: 26,
                    value: ""
                },
                {
                    num: 27,
                    value: ""
                },
                {
                    num: 28,
                    value: ""
                },
                {
                    num: 29,
                    value: ""
                },
                {
                    num: 30,
                    value: ""
                },
                {
                    num: 31,
                    value: ""
                },
                {
                    num: 32,
                    value: ""
                },
                {
                    num: 33,
                    value: ""
                },
                {
                    num: 34,
                    value: ""
                },
                {
                    num: 35,
                    value: ""
                },
                {
                    num: 36,
                    value: ""
                },
                {
                    num: 37,
                    value: ""
                },
                {
                    num: 38,
                    value: ""
                },
                {
                    num: 39,
                    value: ""
                },
                {
                    num: 40,
                    value: ""
                },
                {
                    num: 41,
                    value: ""
                },
                {
                    num: 42,
                    value: ""
                },
                {
                    num: 43,
                    value: ""
                },
                {
                    num: 44,
                    value: ""
                },
                {
                    num: 45,
                    value: ""
                },
                {
                    num: 46,
                    value: ""
                },
                {
                    num: 47,
                    value: ""
                },
                {
                    num: 48,
                    value: ""
                },
                {
                    num: 49,
                    value: ""
                },
                {
                    num: 50,
                    value: ""
                },
                {
                    num: 51,
                    value: ""
                },
                {
                    num: 52,
                    value: ""
                },
                {
                    num: 53,
                    value: ""
                },
                {
                    num: 54,
                    value: ""
                },
                {
                    num: 55,
                    value: ""
                },
                {
                    num: 56,
                    value: ""
                },
                {
                    num: 57,
                    value: ""
                },
                {
                    num: 58,
                    value: ""
                },
                {
                    num: 59,
                    value: ""
                },
                {
                    num: 60,
                    value: ""
                },
                {
                    num: 61,
                    value: ""
                },
                {
                    num: 62,
                    value: ""
                },
                {
                    num: 63,
                    value: ""
                },
                {
                    num: 64,
                    value: ""
                },
                {
                    num: 65,
                    value: ""
                },
                {
                    num: 66,
                    value: ""
                },
                {
                    num: 67,
                    value: ""
                },
                {
                    num: 68,
                    value: ""
                },
                {
                    num: 69,
                    value: ""
                },
                {
                    num: 70,
                    value: ""
                },
                {
                    num: 71,
                    value: ""
                },
                {
                    num: 72,
                    value: ""
                },
                {
                    num: 73,
                    value: ""
                },
                {
                    num: 74,
                    value: ""
                },
                {
                    num: 75,
                    value: ""
                },
                {
                    num: 76,
                    value: ""
                },
                {
                    num: 77,
                    value: ""
                },
                {
                    num: 78,
                    value: ""
                },
                {
                    num: 79,
                    value: ""
                },
                {
                    num: 80,
                    value: ""
                },
                {
                    num: 81,
                    value: ""
                },
                {
                    num: 82,
                    value: ""
                },
                {
                    num: 83,
                    value: ""
                },
                {
                    num: 84,
                    value: ""
                },
                {
                    num: 85,
                    value: ""
                },
                {
                    num: 86,
                    value: ""
                },
                {
                    num: 87,
                    value: ""
                },
                {
                    num: 88,
                    value: ""
                },
                {
                    num: 89,
                    value: ""
                },
                {
                    num: 90,
                    value: ""
                },
                {
                    num: 91,
                    value: ""
                },
                {
                    num: 92,
                    value: ""
                },
                {
                    num: 93,
                    value: ""
                },
                {
                    num: 94,
                    value: ""
                },
                {
                    num: 95,
                    value: ""
                },
                {
                    num: 96,
                    value: ""
                },
                {
                    num: 97,
                    value: ""
                },
                {
                    num: 98,
                    value: ""
                },
                {
                    num: 99,
                    value: ""
                },
                {
                    num: '00',
                    value: ""
                },
            ],
            modal_1: false,
        }
    },
    computed: {
        total() {
            let value = 0;
            for (const field of this.jantari) {
                value = parseInt(value, 10) + parseInt((field.value || 0), 10)
            }
            return value;
        }
    },
    methods:{
        func(){
            if(this.total>0){
            this.modal_1 = !this.modal_1
            }
        }
    }
}
</script>

<style scoped>
.jantari {
    padding-top: 25px;
    left: 0;
    right: 0;
    margin: auto;
    display: flex;
    justify-content: center;
    max-width: 500px;
    margin-right: 20px;
    margin-left: 20px;
}

@media only screen and (min-width:766px) {
    .jantari {
        margin: auto;
    }
}

.num {
    /* width: 25px; */
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

    height: 22px;
    border-bottom: 1px solid black !important;
    left: 0;
    right: 0;
    margin: auto;
}

input {
    font-family: Nunito;
    font-style: normal;
    font-weight: 600;
    font-size: 16px !important;
    line-height: 22px;
    width: 25px;
    display: flex;
    text-align: center;
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

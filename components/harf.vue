<template>
<div>
    <div class="jantari">
        <div class="text1 ">Andar</div>
        <div class="d-flex justify-content-around">
            <div v-for="(items,i) in andar.slice(0, 5)" :key="i">
                <div class="num">{{items.num}}</div>
            </div>
        </div>
        <div class="d-flex justify-content-around ">
            <div v-for="(items,index) in andar.slice(0, 5)" :key="index">
                <input v-model="items.value" type="number" class="input" />
            </div>

        </div>
        <div class="d-flex justify-content-around p">
            <div v-for="(items,i) in andar.slice(5, 10)" :key="i">
                <div class="num">{{items.num}}</div>
            </div>
        </div>
        <div class="d-flex justify-content-around ">
            <div v-for="(items,index) in andar.slice(5, 10)" :key="index">
                <input v-model="items.value" type="number" class="input" />
            </div>
        </div>
    </div>
    <div class="jantari">
        <div class="text1 ">Bahar</div>
        <div class="d-flex justify-content-around">
            <div v-for="(items,i) in bahar.slice(0, 5)" :key="i">
                <div class="num">{{items.num}}</div>
            </div>
        </div>
        <div class="d-flex justify-content-around ">
            <div v-for="(items,index) in bahar.slice(0, 5)" :key="index">
                <input v-model="items.value" type="number" class="input" />
            </div>

        </div>
        <div class="d-flex justify-content-around p">
            <div v-for="(items,i) in bahar.slice(5, 10)" :key="i">
                <div class="num">{{items.num}}</div>
            </div>
        </div>
        <div class="d-flex justify-content-around ">
            <div v-for="(items,index) in bahar.slice(5, 10)" :key="index">
                <input v-model="items.value" type="number" class="input" />
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
</div>
</template>

<script>
export default {
    data() {
        return {
            andar: [
                {
                    num: '00',
                    value: ""
                },
                {
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
                {
                    num: '09',
                    value: ""
                },
            ],
            bahar: [{
                    num: '00',
                    value: ""
                },
                {
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
                {
                    num: '09',
                    value: ""
                },
            ],
            modal_1: false,

        }
    },
    computed: {
        total() {
            let value = 0;
            let value2 = 0;
            for (const field of this.andar) {
                value = parseInt(value, 10) + parseInt((field.value || 0), 10)

            }
            for (const field of this.bahar) {
                value2 = parseInt(value2, 10) + parseInt((field.value || 0), 10)

            }
            value = parseInt(value, 10) + parseInt(value2, 10)
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
                for (const field of this.andar) {
                    field.value = "";
                }
                for (const field2 of this.bahar) {
                    field2.value = "";
                }
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

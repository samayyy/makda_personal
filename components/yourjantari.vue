<template>
<div>
    <form v-if="total>0" @submit.prevent="submit">
         <div class="jantari">
            <div class="d-flex justify-content-around">
                <div v-for="(items,i) in jantari.slice(0, 5)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(0, 5)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>

            </div>
            <div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(5, 10)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(5, 10)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div>
            <div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(10, 15)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(10, 15)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div>
            <div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(15, 20)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(15, 20)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div>
            <div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(20, 25)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(20, 25)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div>
            <div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(25, 30)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(25, 30)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div>
            <div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(30, 35)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(30, 35)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div>
            <div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(35, 40)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(35, 40)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div>
            <div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(40, 45)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(40, 45)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div>
            <div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(45, 50)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(45, 50)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div>
            <div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(50, 55)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(50, 55)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div><div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(55, 60)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(55, 60)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div><div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(60, 65)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(60, 65)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div><div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(65, 70)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(65, 70)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div><div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(70, 75)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(70, 75)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div><div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(75, 80)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(75, 80)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div><div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(80, 85)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(80, 85)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div><div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(85, 90)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(85, 90)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div><div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(90, 95)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(90, 95)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div><div class="d-flex justify-content-around p">
                <div v-for="(items,i) in jantari.slice(95, 100)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in jantari.slice(95, 100)" :key="index">
                    <input v-model="items.value" type="number" class="input" />
                </div>
            </div>
        </div>
    </form>
    <div v-if="total>0" class="bottom">
        <div class="text2"><span>TOTAL:  &#8377;{{total}}</span></div>
    </div>
    <div v-if="total===0" class="jantari">
        <div>
            <img class="img" src="../static/Group 202.svg" />
        </div>
        <div class="text4">You have not placed a bet in this game</div>
    </div>


</div>
</template>

<script>
export default {
    name: 'Yourjantari',
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
                    value: "30"
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
                    value: "50"
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
                    value: "150"
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
                    value: "20"
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
.img {
    width: 224.56px;
    height: 167.33px;
    display: flex;
    left: 0;
    right: 0;
    margin: auto;
}

.text4 {
    text-align: center;
    padding-top: 25px;
    font-family: Nunito;
    font-style: normal;
    font-weight: bold;
    font-size: 20px;
    line-height: 27px;
    text-align: center;
    color: #000000;
}
</style>

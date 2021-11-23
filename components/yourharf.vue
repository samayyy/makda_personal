<template>
<div>
    <div v-if="total>0" class="jantari">
        <div>
            <div class="text1 ">Andar</div>
            <div class="d-flex justify-content-around">
                <div v-for="(items,i) in andar.slice(0, 4)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in andar.slice(0, 4)" :key="index">
                    <input v-model="items.value" type="number" class="input" readonly />
                </div>

            </div>
            <div class="d-flex justify-content-around p">
                <div v-for="(items,i) in andar.slice(5, 9)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in andar.slice(5, 9)" :key="index">
                    <input v-model="items.value" type="number" class="input" readonly />
                </div>
            </div>
        </div>
    </div>
    <div v-if="total>0" class="jantari">
        <div>
            <div class="text1 ">Bahar</div>
            <div class="d-flex justify-content-around">
                <div v-for="(items,i) in bahar.slice(0, 5)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in bahar.slice(0, 5)" :key="index">
                    <input v-model="items.value" type="number" class="input" readonly />
                </div>

            </div>
            <div class="d-flex justify-content-around p">
                <div v-for="(items,i) in bahar.slice(5, 10)" :key="i">
                    <div class="num">{{items.num}}</div>
                </div>
            </div>
            <div class="d-flex justify-content-around ">
                <div v-for="(items,index) in bahar.slice(5, 10)" :key="index">
                    <input v-model="items.value" type="number" class="input" readonly />
                </div>
            </div>
            <div class="bottom">
                <div class="text2"><span>TOTAL: &#8377;{{total}}</span></div>
            </div>
        </div>
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
    data() {
        return {
            andar: [{
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
                    value: "0"
                },
                {
                    num: '08',
                    value: ""
                },
                {
                    num: '09',
                    value: ""
                },
                {
                    num: '00',
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
                    value: "0"
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

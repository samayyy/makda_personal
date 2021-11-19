<template>
<div>
    <div class="jantari">
        <div class="text1 ">Andar</div>
        <div class="d-flex justify-content-around">
            <div v-for="(items,i) in andar.slice(0, 4)" :key="i">
                <div class="num">{{items.num}}</div>
            </div>
        </div>
        <div class="d-flex justify-content-around ">
            <div v-for="(items,index) in andar.slice(0, 4)" :key="index">
                <input v-model="items.value" type="number" class="input" />
            </div>

        </div>
        <div class="d-flex justify-content-around p">
            <div v-for="(items,i) in andar.slice(5, 9)" :key="i">
                <div class="num">{{items.num}}</div>
            </div>
        </div>
        <div class="d-flex justify-content-around ">
            <div v-for="(items,index) in andar.slice(5, 9)" :key="index">
                <input v-model="items.value" type="number" class="input" />
            </div>
        </div>
    </div>
    <div class="jantari">
        <div class="text1 ">Bahar</div>
        <div class="d-flex justify-content-around">
            <div v-for="(items,i) in bahar.slice(0, 4)" :key="i">
                <div class="num">{{items.num}}</div>
            </div>
        </div>
        <div class="d-flex justify-content-around ">
            <div v-for="(items,index) in bahar.slice(0, 4)" :key="index">
                <input v-model="items.value" type="number" class="input" />
            </div>

        </div>
        <div class="d-flex justify-content-around p">
            <div v-for="(items,i) in bahar.slice(5, 9)" :key="i">
                <div class="num">{{items.num}}</div>
            </div>
        </div>
        <div class="d-flex justify-content-around ">
            <div v-for="(items,index) in bahar.slice(5, 9)" :key="index">
                <input v-model="items.value" type="number" class="input" />
            </div>
        </div>
        <div class="bottom">
            <div class="text2"><span>TOTAL: {{total}}</span></div>
            <NuxtLink to=/games> <button class="button"><span class="btntext">Submit</span></button></NuxtLink>
        </div>
    </div>
</div>
</template>

<script>
export default {
    data() {
        return {
            andar: [{
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
                {
                    num: '00',
                    value: ""
                },
            ],
            bahar: [{
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
                {
                    num: '00',
                    value: ""
                },
            ],

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

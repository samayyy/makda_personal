<template>
<div class="opensheet">
    <form @submit.prevent="submit">
        <input v-model="opensheet.number" class="formelement" type="number" placeholder="Enter Number" required>
        <input v-model="opensheet.count" class="formelement" type="number" placeholder="Enter Amount" required>
        <button class="button"><span class="btntext">Add</span>
            <div class="bg"></div>
        </button>

    </form>
    <div class="data">
        <div class="d-flex justify-content-evenly">
            <div class="head2">Number Type</div>
            <div class="head2">Number</div>
            <div class="head2">Amount</div>

        </div>
    </div>

    <div v-for="(items, index) in opensheetAdded" :key="index">
        <div class="data2">
            <div class="d-flex justify-content-evenly">
                <div class="head3">{{items.type}}</div>
                <div class="head3">{{items.numberAdded}}</div>
                <div class="head3">{{items.countAdded}}</div>
            </div>
        </div>
    </div>
    <form @submit.prevent="func();">
        <div class="bottom">
            <div class="text2"><span>TOTAL:  &#8377;{{total}}</span></div>
            <button class="button2"><span class="btntext2">Submit</span></button>
        </div>
    </form>
    <div>
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
    name: 'Opensheet',
    data() {
        return {
            opensheet: {
                count: null,
                number: null,
                type: 'jodi'
            },
            opensheetAdded: [],
            total: 0,
            modal_1: false,
        }
    },
    methods: {
        submit() {
            if (this.opensheet.number < 100 && this.opensheet.number >= 0 && this.opensheet.number.length<=2) {
                const addData = {
                    countAdded: this.opensheet.count,
                    numberAdded: this.opensheet.number,
                    type: 'Jodi'
                }

                this.opensheetAdded.push(addData);
                this.total = parseFloat(this.total) + parseFloat(addData.countAdded)
                this.opensheet.count = null;
                this.opensheet.number = null;
            }
        },
        func() {
            if (this.total > 0) {
                this.modal_1 = !this.modal_1;
            }
        },
        func2() {
            if (this.total > 0) {
                this.total = 0;
                this.modal_1 = !this.modal_1;
                for (const items in this.opensheetAdded.slice('0,this.opensheetAdded.length+2')) {
                    this.opensheetAdded.pop(items);
                }
            }
        }
    },

}
</script>

<style scoped>
.opensheet {
    padding-top: 25px;
    padding-left: 12px;
}

.formelement {
    width: 95%;
    max-width: 400px;
    height: 40px;
    left: 0;
    right: 0;
    margin: auto;
    display: flex;
    justify-content: center;
    padding: 5px 10px;
    border-bottom: 1px solid grey;
}

input {
    margin-top: 15px !important;
    margin-bottom: 10px !important;
}

input[type="number"] {
    font-size: 18px !important;
}

textarea:focus,
input:focus {
    outline: none;
}

.button {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    width: 142px;
    height: 40px;
    background: #006CA9;
    border-radius: 20px;
    left: 0;
    right: 0;
    margin: auto;
    margin-top: 25px;
}

.btntext {
    width: 35px;
    height: 25px;
    font-family: Nunito;
    font-style: normal;
    font-weight: 600;
    font-size: 18px;
    line-height: 25px;
    color: #FFFFFF;
    margin-right: 25px;
}

.bg {
    width: 25px;
    height: 25px;
    background: url('data:image/svg+xml,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20xmlns%3Axlink%3D%22http%3A%2F%2Fwww.w3.org%2F1999%2Fxlink%22%20width%3D%2225%22%20height%3D%2225%22%20preserveAspectRatio%3D%22xMidYMid%20meet%22%20viewBox%3D%220%200%2024%2024%22%3E%3Cg%20fill%3D%22none%22%3E%3Cpath%20d%3D%22M12%208v4m0%200v4m0-4h4m-4%200H8%22%20stroke%3D%22white%22%20stroke-width%3D%222%22%20stroke-linecap%3D%22round%22%2F%3E%3Ccircle%20cx%3D%2212%22%20cy%3D%2212%22%20r%3D%2210%22%20stroke%3D%22white%22%20stroke-width%3D%222%22%2F%3E%3C%2Fg%3E%3C%2Fsvg%3E');
    background-size: 100%;
    background-repeat: no-repeat;
}

.data {
    padding-top: 40px;
}

.data2 {
    padding-top: 20px;
}

.head2 {
    width: 94px;
    height: 21px;
    font-family: Poppins;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 21px;
    color: #B7B7B7;
    display: flex;
    justify-content: center;

}

.head3 {
    width: 94px;
    height: 25px;
    font-family: Nunito;
    font-style: normal;
    font-weight: 600;
    font-size: 18px;
    line-height: 25px;
    color: #000000;
    display: flex;
    justify-content: center;
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

.button2 {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 8px;
    width: 85vw;
    max-width: 330px;
    /* min-width: 200px; */
    height: 40px;
    background: #006CA9;
    border-radius: 20px;
    color: white !important;
    text-decoration: none !important;
    margin-top: 20px;
}

.btntext2 {
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

@media only screen and (max-width: 320px) {
    .c-modal {
        width: 90%;
    }
}
</style>

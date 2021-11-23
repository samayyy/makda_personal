<template>
<div>
    <div v-if="total>0" class="card">
        <div class="d-flex justify-content-around bgcolor">
            <div class="head1">Bet Amount</div>
            <div class="head1">Number</div>
            <div class="head1">Potential Profits</div>
        </div>
        <div class="p">
        <div v-for="(items,i) in youropensheet" :key="i" class="d-flex justify-content-around">
            <div class="head1 head">&#8377;{{items.count}}</div>
            <div class="head1 head">{{items.number}}</div>
            <div class="head1 head green">{{items.potentialprofit}}</div>
        </div>
        </div>
        <div class="head2">TOTAL BET AMOUNT: &#8377;{{total}} </div>
    </div>
    <div v-if="total===0" class="bot">
        <div>
            <img class="img" src="../static/Group 202.svg" />
        </div>
        <div class="text4">You have not placed a bet in this game</div>
    </div>
</div>
</template>

<script>
export default {
    name: 'Youropensheet',
    data() {
        return {
            youropensheet: [{
                    count: 20,
                    number: '09',
                    potentialprofit: null
                },
                {
                    count: 30,
                    number: '09',
                    potentialprofit: null
                },
                {
                    count: 40,
                    number: '09',
                    potentialprofit: null
                },
                {
                    count: 50,
                    number: '09',
                    potentialprofit: null
                },
                {
                    count: 20,
                    number: '09',
                    potentialprofit: null
                },
            ],
        }
    },
    computed: {
        total() {
            let value = 0;
            for (const field of this.youropensheet) {
                value = parseInt(value, 10) + parseInt((field.count || 0), 10)
            }
            return value;
        },

    },
    mounted() {
        for (const field of this.youropensheet) {
            field.potentialprofit = parseInt((field.count || 0), 10) * 90;
        }
    }
}
</script>

<style scoped>
.card {
    max-width: 310px;
    width: 90vw;
    /* height: 273px; */
    background: #FFFFFF;
    box-shadow: 0px 2px 12px rgba(0, 0, 0, 0.12);
    border-radius: 12px;
    left: 0;
    right: 0;
    margin: auto;
    margin-top: 25px;
}
.bot{
    margin-top: 25px;
}
.bgcolor {
    background: rgba(0, 108, 169, 0.27);
    border-radius: 12px 12px 0px 0px;
}

.head1 {
    /* width: 76px; */
    height: 30px;
    font-family: Nunito;
    font-style: normal;
    font-weight: normal;
    font-size: 14px;
    line-height: 19px;
    color: #0F0F0F;
    display: flex;
    justify-content: center;
    align-items: center;
}

.head2 {
    max-width: 310px;
    width: 90vw;
    height: 27px;
    font-family: Nunito;
    font-style: normal;
    font-weight: 800;
    font-size: 16px;
    line-height: 27px;
    color: #000000;
    margin-top: 20px;
    margin-bottom: 20px;
    display: flex;
    justify-content: center;
}

.head {
    font-family: Nunito Sans;
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 25px;
    color: #000000;
}
.green{
    color: #1D8546;
}

.p {
    padding-top: 20px;
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

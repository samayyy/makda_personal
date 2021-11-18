<template>
<div class="opensheet">
    <form>
        <input v-model="opensheet.number" class="formelement" type="number" placeholder="Enter Number">
        <input v-model="opensheet.count" class="formelement" type="number" placeholder="Enter Amount">
        <NuxtLink to="/games"><button type="submit" class="button"><span class="btntext">Add</span>
                <Icon icon="akar-icons:circle-plus" color="white" height="25" width="25" /></button></NuxtLink>

    </form>
    <div class="data">
        <div class="d-flex justify-content-center justify-items-between">
            <div class="head2">Number Type</div>
            <div class="head2">Number</div>
            <div class="head2">Amount</div>

        </div>
    </div>
    {{openamount}}
</div>
</template>

<script>
import {
    Icon
} from '@iconify/vue2';
export default {
    name: 'Opensheet',
    components: {
        Icon
    },
    data() {
        return {
            opensheet: {
                    count: 0,
                    number: null
                }
        }
    },
    computed: {
        openamount() {
            let count = 0;
                count += this.opensheet.count;
            return count;
        }
    }
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
.data{
    padding-top: 40px;
}
.head2 {
    width: 94px;
    height: 21px;
    font-family: Poppins;
    font-style: normal;
    font-weight: normal;
    font-size: 14px;
    line-height: 21px;
    color: #B7B7B7;
    display: flex;
    justify-content: center;

}
</style>

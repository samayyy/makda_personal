<template>
<div>
    <form>
        <div class="head4">Enter Amount to deposit</div>
        <input type="number" class="formelement" placeholder="2000" required>
        <button class="button"><span class="btntext">Make Payment</span></button>
    </form>
</div>
</template>

<script>
export default {
    name: 'Paymentgateway'
}
</script>

<style scoped>
.head4 {
    width: 85vw;
    max-width: 400px;
    left: 0;
    right: 0;
    margin: auto;
    height: 27px;
    font-family: Nunito;
    font-style: normal;
    font-weight: bold;
    font-size: 20px;
    line-height: 27px;
    color: #000000;
    margin-top: 25px;
}

.button {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 8px;
    background: #006CA9;
    border-radius: 20px;
    max-width: 400px;
    width: 84vw;
    left: 0;
    right: 0;
    margin: auto;
    margin-top: 25px;

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

.formelement {
    width: 85vw;
    max-width: 400px;
    display: flex;
    justify-content: center;
    height: 40px;
    left: 0;
    right: 0;
    margin: auto;
    border-bottom: 1px solid grey;
}

input {
    margin-top: 10px !important;
    /* margin-bottom: 10px !important; */
    width: 85vw;
    max-width: 400px;
    height: 40px;
    left: 0;
    right: 0;
    margin: auto;
}

input[type="number"] {
    font-size: 18px !important;
}

textarea:focus,
input:focus {
    outline: none;
}
</style>

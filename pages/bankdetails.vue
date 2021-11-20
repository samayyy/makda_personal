<template>
<div>
    <div v-if="$vuetify.breakpoint.smAndDown">
    <div class="d-flex justify-content-between align-items-center pos">
        <NuxtLink to="/withdraw">
            <div class="back-icon2" icon="akar-icons:arrow-left"></div>
        </NuxtLink>
        <div class="head1">Wallet</div>
        <div class="back-icon3" icon="akar-icons:arrow-left"></div>
    </div>
    </div>
    <form>
        <div class="head4">Enter Baank Account Details</div>
        <input type="text" class="formelement" placeholder="Account Number" required>
        <input type="text" class="formelement" placeholder="Account Holder Name" required>
        <input type="text" class="formelement" placeholder="IFSC CODE" required>
        <input type="text" class="formelement" placeholder="Branch" required>

        <button class="button"><span class="btntext">Make Payment</span></button>
    </form>
</div>
</template>

<script>
export default {
    name: 'Withdraw'
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

.pos {
    padding-top: 15px;
    padding-left: 12px;
}
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

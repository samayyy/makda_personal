<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div class="flexx1">
        <NuxtLink to="/">
            <div class="back-icon" icon="akar-icons:arrow-left"></div>
        </NuxtLink>
        <p class="headsignup">Sign Up</p>
    </div>

    <div class="logosignup1">
        <img class="logo" src="../static/taj logo.svg" />
    </div>

    <form class="form">
        <input class="formelement" type="text" placeholder="Name">
        <br>
        <input class="formelement" type="number" placeholder="Phone">
        <br>
        <input class="formelement second" type="password" placeholder="Password">
        <br>
    </form>
    <div class="abc">
        <NuxtLink to="/otp"><button class="button"><span class="btntext">Get Started</span></button></NuxtLink>
    </div>
</div>
</template>

<script>
export default {
    name: 'Signup1',
}
</script>

<style scoped>
.headsignup {
    padding-top: 40px;
    width: 108px;
    left: 0;
    right: 0;
    margin: auto;
    text-align: center;
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 28px;
    line-height: 42px;
}

.flexx1 {
    display: flex;
    flex-direction: row;
}

.logosignup1 {
    left: 0;
    right: 0;
    margin: auto;
    padding-top: 60px;
    width: 170px;
    height: 57px;
}

.back-icon {
    width: 35px;
    height: 35px;
    padding-left: 27px;
    margin-top:  27px !important;
    background: url('data:image/svg+xml,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20xmlns%3Axlink%3D%22http%3A%2F%2Fwww.w3.org%2F1999%2Fxlink%22%20width%3D%221em%22%20height%3D%221em%22%20preserveAspectRatio%3D%22xMidYMid%20meet%22%20viewBox%3D%220%200%2024%2024%22%3E%3Cpath%20fill%3D%22%23006ca9%22%20d%3D%22M19%2011H7.14l3.63-4.36a1%201%200%201%200-1.54-1.28l-5%206a1.19%201.19%200%200%200-.09.15c0%20.05%200%20.08-.07.13A1%201%200%200%200%204%2012a1%201%200%200%200%20.07.36c0%20.05%200%20.08.07.13a1.19%201.19%200%200%200%20.09.15l5%206A1%201%200%200%200%2010%2019a1%201%200%200%200%20.64-.23a1%201%200%200%200%20.13-1.41L7.14%2013H19a1%201%200%200%200%200-2z%22%2F%3E%3C%2Fsvg%3E');
    background-repeat: no-repeat;
    background-size: 100%;
}

.logo {
    left: 0;
    right: 0;
    margin: auto;
    width: 100%;
    color: #000000;
}

.form {
    padding-top: 130px;
}

.formelement {
    display: flex;
    justify-content: center;
    width: 70vw;
    max-width: 500px;
    height: 50px;
    padding: 5px 10px;
}

input {
    background-color: #F0F0F0 !important;
    font-size: 18px !important;
    font-family: Inter;
    font-style: normal;
    font-weight: normal;
    line-height: 24px;
    letter-spacing: -0.011em;
    left: 0;
    right: 0;
    margin: auto;
}

.button {
    width: 70vw;
    max-width: 400px;
    height: 60px;
    margin-top: 30px;
    background: #006CA9;
    border-radius: 20px;
}

.btntext {
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 22px;
    line-height: 36px;
    color: #FFFFFF;
}

.abc {
    display: flex;
    justify-content: center;
}
</style>

<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <p class="headsignup">Sign Up</p>
    <div class="logosignup1">
        <p class="logosignup2"><span class="bglogo">Logo</span></p>
        <div class="container">
            <div class="container">
                <div class="container">
                    <div class="container">
                        <form class="form">
                            <input class="formelement" type="text" placeholder="   Name">
                            <br>
                            <input class="formelement" type="number" placeholder="   Phone">
                            <br>
                            <input class="formelement" type="password" placeholder="   Password">
                            <br>
                        </form>
                    </div>
                </div>
            </div>
        </div>
        <NuxtLink to="/otp"><button class="button"><span class="btntext">Get Started</span></button></NuxtLink>
        <NuxtLink to="/login" >
            <p class="link">Already an user?</p>
        </NuxtLink>
    </div>
</div>
</template>

<script>
export default {
    name: 'Signup1'
}
</script>

<style scoped>
.headsignup {
    top: 80px;
    position: absolute;
    width: 108px;
    left: 0;
    right: 0;
    margin: auto;
    transform: translateY(-50%);
    text-align: center;
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 28px;
    line-height: 42px;
}

.logosignup2 {
    left: 0;
    right: 0;
    margin: auto;
    transform: translateY(-50%);
    top: 180px;
    position: absolute;
    text-align: center;
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 24px;
    line-height: 36px;
    color: #000000;
}

.bglogo {
    background: #C4C4C4;
    padding: 10px 25% !important;
}

.form {
    position: absolute;
    top: 300px;

}

.formelement {
    left: 0;
    right: 0;
    margin: auto;
    width: 70vw;
    height: 50px;
    /* padding-bottom: 10px; */
    left: 0;
    right: 0;
    margin: auto;
    transform: translateY(-50%);
    margin-bottom: 18px !important;
}

input {
    background-color: #F0F0F0 !important;
}

.button {
    position: absolute;
    width: 70vw;
    height: 60px;
    /* left: 37px; */
    left: 0;
    right: 0;
    margin: auto;
    top: 520px;
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

.link {
    top: 620px;
    position: absolute;
    left: 0;
    right: 0;
    margin: auto;
    transform: translateY(-50%);
    text-align: center;
}
</style>

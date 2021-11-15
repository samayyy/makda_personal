<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div class="flexx1">
        <NuxtLink to="/">
            <Icon class="back-icon" icon="akar-icons:arrow-left" />
        </NuxtLink>
    </div>
    <p class="headsignup">Login</p>
    <div class="logosignup1">
        <p class="logosignup2"><span class="bglogo">Logo</span></p>
        <div class="container">
            <div class="container">
                <div class="container">
                    <div class="container">
                        <form class="form">
                            <input class="formelement" type="number" placeholder="   Phone">
                            <br>
                            <input class="formelement" type="password" placeholder="   Password">
                            <br>
                        </form>
                    </div>
                </div>
            </div>
        </div>
        <NuxtLink to="/otp"><button class="button"><span class="btntext">Login</span></button></NuxtLink>
    </div>
</div>
</template>

<script>
import { Icon } from '@iconify/vue2';
export default {
    components: { Icon }
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

.flexx1 {
    display: flex;
    flex-direction: ro  w;
}

.back-icon {
    position: absolute;
    width: 25px;
    height: 25px;
    left: 27px;
    top: 65px;
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
    top: 465px;
    background: #006CA9;
    border-radius: 20px;
}

.btntext {
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 22px;
    line-height: 36px;
    /* identical to box height */

    color: #FFFFFF;

}
</style>

<template>
<div v-if="$vuetify.breakpoint.smAndDown">

<div class="flexx container">
    <p class="head"> Play Online Matka with Fairplay </p>
    <NuxtLink to="/signup"><button class="button"><span class="btntext">Get Started</span></button></NuxtLink>
</div>
</div>
</template>

<style scoped>
.head {
    position: absolute;
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 24px;
    top: 45%;
    transform: translateY(-50%);
}

.button {
    position: absolute;
    width: 70vw;
    height: 60px;
    top: 60%;
    transform: translateY(-50%);
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
.flexx{
    height: 100vh;
  position: relative;
}
</style>

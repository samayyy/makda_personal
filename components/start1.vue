<template>
<div v-if="$vuetify.breakpoint.smAndDown">

    <div class="float">
        <img class="logo" src="../static/taj logo.svg">
        <p class="head"> Play Online Matka with Taj </p>
        <NuxtLink to="/signup"><button class="button"><span class="btntext">Get Started</span></button></NuxtLink>
        <p class="link">
            Already have an account?
            <NuxtLink to="/login">
                Login
            </NuxtLink>
        </p>
    </div>
</div>
</template>

<style scoped>
.logo {
    /* max-width: 300px; */
    width: 80vw;
    height: 57px;
    display: flex;
    justify-content: center;
}

.float {
    width: 80vw;
    height: 455px;
    position: fixed;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    margin: auto;
}

.head {
    padding-top: 120px;
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 28px;
    line-height: 42px;
    color: #000000;
}
.button {
    width: 80vw;
    max-width: 400px;
    height: 60px;
    left: 0;
    right: 0;
    margin: auto;
    display: flex;
    justify-content: center;
    align-items: center;
    background: #006CA9;
    border-radius: 20px;
    margin-top: 100px;
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
 
    margin: auto;
    text-align: center;
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 24px;
    color: #252525;
    padding-top: 10px;
}
@media only screen and (min-width: 417px){
    .head{
    text-align: center;
    }
}
</style>

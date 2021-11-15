<template>
    <div v-if="$vuetify.breakpoint.smAndDown">
      <div class="flexx">
        <Icon class="back-icon" icon="akar-icons:arrow-left" />
        <p class="headsignup">Sign Up</p>
        </div>
    </div>
</template>

<script>
import { Icon } from '@iconify/vue2';
export default {
    components: { Icon }
}
</script>

<style>
.flexx{
  flex-direction: row;
  position: relative;
  justify-content: center;
  align-items: center;
}
.back-icon{
position: absolute;
width: 35px;
height: 35px;
left: 27px;
top: 48px;
}

.headsignup{
  /* position: absolute; */
/* width: 108px; */
height: 42px;
/* left: 153px; */
text-align: center;
top: 45px;
font-family: Poppins;
font-style: normal;
font-weight: 600;
font-size: 28px;
line-height: 42px;
}
</style>

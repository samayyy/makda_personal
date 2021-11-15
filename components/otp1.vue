<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div class="flexx1">
        <NuxtLink to="/">
        <Icon class="back-icon" icon="akar-icons:arrow-left" />
        </NuxtLink>
    </div>
    <p class="headsignup">Sign Up</p>

    <p class="logosignup2"><span class="bglogo">Logo</span></p>
    <p class="otptext1"> A 4 Digit Otp
        <br>
        <span class="otptext2">has been seen to <b>750683xxxx</b> </span></p>
    <div class="centered">
        <form class="form flexx">
            <!-- <input v-model="amount" class="formelement pad"  type="number" oninput="javascript: if (this.value.length > this.maxLength) this.value = this.value.slice(0, this.maxLength);" maxlength="1"> -->
            <input  v-for="(key, i) in  otpKeyFields" :key="i" :ref="`input-${i}`" v-model="key.value"  :data-length="key.length"  :data-index="i" class="formelement pad" type="text" oninput="javascript: if (this.value.length > this.maxLength) this.value = this.value.slice(0, this.maxLength);" maxlength="1" @input="handleotpInput($event)"  >
            <!-- <input class="formelement pad" type="number">
            <input class="formelement" type="number"> -->

        </form>

    </div>
    <!-- </div>
                </div>
            </div>
        </div> -->
    <NuxtLink to="/home"><button class="button"><span class="btntext">Get Started</span></button></NuxtLink>
</div>
</template>

<script>
import {
    Icon
} from '@iconify/vue2';
export default {
    components: {
        Icon
    },
    data:  ()=> {
        return {
        // Our input fields.
        // length is the max char allowed
        otpKeyFields: [{
                length: 1,
                value: ''
            },
            {
                length: 1,
                value: ''
            },
            {
                length: 1,
                value: ''
            },
            {
                length: 1,
                value: ''
            },
        ],
        }
    },
    computed: {
        otpKey() {
            let value = '';
            for (const field of this.otpKeyFields) {
                value += field.value;
            }
            return value;
        }
    },
    methods: {
        handleotpInput(e) {
            // Grab input's value
            const value = e.target.value;
            // Grab data-index value
            const index = parseInt(e.target.dataset.index);
            // Grab data-length value
            const maxlength = e.target.dataset.length;

            if (this.otpKeyFields[index].value.length > maxlength) {
                e.preventDefault();
                this.otpKeyFields[index].value = value.slice(0, 5);
                try {
                    this.$refs[`input-${parseInt(index + 1)}`][0].focus();
                } catch (e) {}
                return;
            }

            // Shift focus to next input field if max length reached
            if (value.length >= maxlength) {
                if (typeof this.otpKeyFields[index + 1] === 'undefined') {
                    e.preventDefault();
                    return;
                }
                this.$refs[`input-${parseInt(index + 1)}`][0].focus();
                e.preventDefault();
            }
        },
    },

    
}
</script>

<style scoped>
.flexx1 {
    display: flex;
    flex-direction: row;
}

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
.back-icon{
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
    top: 440px;
    left: 30px;
    transform: translateY(-50%);
}

.flexx {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
}

.formelement {
    left: 0;
    right: 0;
    margin: auto;
    width: 15vw;
    height: 70px;
    left: 0;
    right: 0;
    margin: auto;
    transform: translateY(-50%);
}

input {
    background-color: #F0F0F0 !important;
    text-align: center;
}

.pad {
    margin-right: 3.33vw !important;
}

.button {
    position: absolute;
    width: 70vw;
    height: 60px;
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

.otptext1 {
    position: absolute;
    width: 218px;
    height: 24px;
    left: 30px;
    top: 274px;
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 24px;
    line-height: 24px;
}

.otptext2 {
    font-family: Montserrat;
    font-style: normal;
    font-weight: normal;
    font-size: 16px;
    line-height: 24px;
    letter-spacing: -0.011em;
}
</style>

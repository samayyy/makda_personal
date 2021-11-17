<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div id="offcanvas" class="offcanvas offcanvas-start h-75 b" tabindex="-1" data-bs-keyboard="false" data-bs-backdrop="false">
        <div class="offcanvas-header">
            <button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas" aria-label="Close"></button>
        </div>
        <div class="offcanvas-body">
            <div class="d-flex justify-content-center p">
                <div class="justify-self-center">
                    Profile
                </div>
            </div>
            <hr>
            <div class="d-flex justify-content-between p">
                <div class=" justify-self-start">
                    <Icon icon="bi:share-fill" color="#006ca9" width="16" height="16" />
                </div>
                <div class="justify-self-center textt">
                    Share App
                </div>
                <div class=" justify-self-end none">
                </div>
            </div>
            <hr>
            <div class="d-flex justify-content-between p">
                <div class=" justify-self-start">
                    <Icon icon="carbon:result" color="#006ca9" width="16" height="16" />
                </div>
                <div class="justify-self-center textt">
                    Results
                </div>
                <div class=" justify-self-end none">
                </div>
            </div>
            <hr>

            <div class="d-flex justify-content-between p">
                <div class=" justify-self-start">
                    <Icon icon="fluent:wallet-24-filled" color="#006ca9" width="16" height="16" />
                </div>
                <div class="justify-self-center textt">
                    Wallet
                </div>
                <div class=" justify-self-end none">
                </div>
            </div>
            <hr>
            <div class="d-flex justify-content-between p">
                <div class=" justify-self-start">
                    <Icon icon="teenyicons:password-solid" color="#006ca9" width="16" height="16" />
                </div>
                <div class="justify-self-center textt">
                    Change Password
                </div>
                <div class=" justify-self-end none">
                </div>
            </div>
            <hr>
            <div class="d-flex justify-content-between p">
                <div class=" justify-self-start">
                    <Icon icon="fluent:call-20-filled" color="#006ca9" width="16" height="16" />
                </div>
                <div class="justify-self-center textt">
                    Help
                </div>
                <div class=" justify-self-end none">
                </div>
            </div>
            <hr>
            <div class="d-flex justify-content-between p">
                <div class=" justify-self-start">
                    <Icon icon="carbon:document" color="#006ca9" width="16" height="16" />
                </div>
                <div class="justify-self-center textt">
                    Terms & Conditions
                </div>
                <div class=" justify-self-end none">
                </div>
            </div>
            <hr>
            <div class="d-flex justify-content-between p">
                <div class=" justify-self-start">
                    <Icon icon="ant-design:logout-outlined" color="#006ca9" width="16" height="16" />
                </div>
                <div class="justify-self-center textt">
                    Logout
                </div>
                <div class=" justify-self-end none">
                </div>
            </div>
            <hr>

        </div>
    </div>
    <div class=" pos1">
        <div class="d-flex justify-content-between">

            <div class=" justify-self-start logo">
                <button data-bs-toggle="offcanvas" data-bs-target="#offcanvas" role="button">
                    <span class="logo1" data-bs-toggle="offcanvas" data-bs-target="#offcanvas">Logo</span>
                </button></div>

            <div class="search justify-self-center">
                <Icon icon="akar-icons:search" color="white" class="search2" />
            </div>
            <div class="balance justify-self-end d-flex justify-content-evenly">
                <Icon icon="fluent:wallet-24-filled" color="#006ca9" class="balance1" />
                <div> $ 4000 </div>
            </div>
        </div>
    </div>
    <div class="banner"><span class="banner1">Banner</span></div>
    <div class="pos2">
        <div class="d-flex justify-content-between">
            <div class="head2 justify-self-start">Top Results</div>

            <div class="head3 justify-self-end">
                <NuxtLink to="/allresults"><div>View All</div></NuxtLink>
            </div>
        </div>
    </div>
</div>
</template>

<script>
import {
    Icon
} from '@iconify/vue2';
export default {
    name: 'Home1',
    components: {
        Icon
    }

}
</script>

<style scoped>
.none {
    width: 0px;
}

.textt {
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 16px;
    line-height: 27px;
    display: flex;
    align-items: center;
    color: #000000;
    margin-left: -25px !important;
}

.offcanvas-body {
    flex-grow: 1;
    padding: 1rem 0 !important;
    overflow-y: auto;
}

.b {
    border: 1px solid #006CA9 !important;
    width: 60vw;
}

.p {
    padding-left: 12px;
}

hr {
    margin: 8px 0 !important;
}

.pos1 {
    height: 44px;
    top: 37px;
}

.logo {
    width: 109px;
    height: 44px;
    background: #E7E7E7;
}

.logo1 {
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 44px;
    display: flex;
    align-items: center;
    color: #262626;
    text-align: center;
    justify-content: center;
}

.search2 {
    width: 52px;
    height: 25px;
    color: black;
    padding: 3px 0 !important;
    border-radius: 50px;
    background: #006CA9;
}

.balance {
    border: 1px solid #006CA9;
    border-radius: 30px;
    width: 109px;
    height: 35px;
    vertical-align: middle;
}

.balance1 {
    width: 23px;
    height: 23px;
}

.d-flex {

    align-items: center !important;
}

.banner {
    position: absolute;
    width: 90vw;
    height: 133px;
    left: 14px;
    top: 82px;
    background: #C4C4C4;
    border-radius: 20px;
}

.banner1 {
    position: absolute;
    top: 50%;
    height: 133px;
    left: 40%;
    right: 0;
    margin: auto;
    transform: translateY(-50%);
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 20px;
    line-height: 30px;
    display: flex;
    align-items: center;
    color: #000000;
}

.pos2 {
    height: 30px;
    padding-left: 12px;
    padding-right: 12px;
    padding-top: 190px;
    z-index: 1;
}

.head2 {
    height: 30px;
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 20px;
    line-height: 30px;
    display: flex;
    align-items: center;
    color: #000000;
    z-index: 10;
}

.head3 {
    font-family: Poppins;
    font-style: normal;
    font-weight: 600;
    font-size: 14px;
    line-height: 21px;
    text-decoration: line;
    display: flex;
    align-items: center;
    color: #006CA9;
    z-index: 10;
}
</style>

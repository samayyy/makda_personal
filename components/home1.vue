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
                    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="16" height="16" preserveAspectRatio="xMidYMid meet" viewBox="0 0 16 16">
                        <g fill="#006ca9">
                            <path d="M11 2.5a2.5 2.5 0 1 1 .603 1.628l-6.718 3.12a2.499 2.499 0 0 1 0 1.504l6.718 3.12a2.5 2.5 0 1 1-.488.876l-6.718-3.12a2.5 2.5 0 1 1 0-3.256l6.718-3.12A2.5 2.5 0 0 1 11 2.5z" />
                        </g>
                    </svg>
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
                    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="16" height="16" preserveAspectRatio="xMidYMid meet" viewBox="0 0 16 16">
                        <g fill="#006ca9">
                            <path d="M11 2.5a2.5 2.5 0 1 1 .603 1.628l-6.718 3.12a2.499 2.499 0 0 1 0 1.504l6.718 3.12a2.5 2.5 0 1 1-.488.876l-6.718-3.12a2.5 2.5 0 1 1 0-3.256l6.718-3.12A2.5 2.5 0 0 1 11 2.5z" />
                        </g>
                    </svg>
                </div>
                <div class="justify-self-center textt">
                    <NuxtLink to=/allbets>Results </NuxtLink> </div> <div class=" justify-self-end none">
                </div>
            </div>
            <hr>

            <div class="d-flex justify-content-between p">
                <div class=" justify-self-start">
                    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="16" height="16" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24">
                        <g fill="none">
                            <path d="M3 5v12.75A3.25 3.25 0 0 0 6.25 21h12a3.25 3.25 0 0 0 3.25-3.25v-8.5A3.251 3.251 0 0 0 19 6.087V5.25A2.25 2.25 0 0 0 16.75 3H5.25a2.25 2.25 0 0 0-2.236 2H3zm2.25 1a.75.75 0 0 1 0-1.5h11.5a.75.75 0 0 1 .75.75V6H5.25zm11 7h2a.75.75 0 0 1 0 1.5h-2a.75.75 0 0 1 0-1.5z" fill="#006ca9" />
                        </g>
                    </svg>

                </div>
                <div class="justify-self-center textt">
                    <NuxtLink to=/wallet>Wallet </NuxtLink> </div> <div class=" justify-self-end none">
                </div>
            </div>
            <hr>
            <div class="d-flex justify-content-between p">
                <div class=" justify-self-start">
                    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="16" height="16" preserveAspectRatio="xMidYMid meet" viewBox="0 0 15 15">
                        <g fill="none">
                            <path d="M11 11h-1v-1h1v1z" fill="#006ca9" />
                            <path d="M8 11h1v-1H8v1z" fill="#006ca9" />
                            <path d="M13 11h-1v-1h1v1z" fill="#006ca9" />
                            <path fill-rule="evenodd" clip-rule="evenodd" d="M3 6V3.5a3.5 3.5 0 1 1 7 0V6h1.5A1.5 1.5 0 0 1 13 7.5v.55a2.5 2.5 0 0 1 0 4.9v.55a1.5 1.5 0 0 1-1.5 1.5h-10A1.5 1.5 0 0 1 0 13.5v-6A1.5 1.5 0 0 1 1.5 6H3zm1-2.5a2.5 2.5 0 0 1 5 0V6H4V3.5zM8.5 9a1.5 1.5 0 1 0 0 3h4a1.5 1.5 0 0 0 0-3h-4z" fill="#006ca9" />
                        </g>
                    </svg>
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
                    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="16" height="16" preserveAspectRatio="xMidYMid meet" viewBox="0 0 20 20">
                        <g fill="none">
                            <path d="M6.987 2.066a2 2 0 0 1 2.327.946l.075.149l.661 1.471a2.497 2.497 0 0 1-.442 2.718l-.132.132l-1.044.973c-.188.178-.047.867.634 2.045c.611 1.06 1.11 1.555 1.354 1.582h.043l.053-.01l2.05-.627a1.5 1.5 0 0 1 1.564.441l.092.115l1.356 1.88a2 2 0 0 1-.124 2.497l-.122.126l-.543.514a3.5 3.5 0 0 1-3.715.705c-1.935-.78-3.693-2.562-5.29-5.328c-1.6-2.773-2.265-5.19-1.968-7.26a3.5 3.5 0 0 1 2.262-2.789l.193-.064l.716-.216z" fill="#006ca9" />
                        </g>
                    </svg>
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
                    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="16" height="16" preserveAspectRatio="xMidYMid meet" viewBox="0 0 32 32">
                        <path d="M25.7 9.3l-7-7c-.2-.2-.4-.3-.7-.3H8c-1.1 0-2 .9-2 2v24c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V10c0-.3-.1-.5-.3-.7zM18 4.4l5.6 5.6H18V4.4zM24 28H8V4h8v6c0 1.1.9 2 2 2h6v16z" fill="#006ca9" />
                        <path d="M10 22h12v2H10z" fill="#006ca9" />
                        <path d="M10 16h12v2H10z" fill="#006ca9" /></svg>
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
                    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="16" height="16" preserveAspectRatio="xMidYMid meet" viewBox="0 0 1024 1024">
                        <path d="M868 732h-70.3c-4.8 0-9.3 2.1-12.3 5.8c-7 8.5-14.5 16.7-22.4 24.5a353.84 353.84 0 0 1-112.7 75.9A352.8 352.8 0 0 1 512.4 866c-47.9 0-94.3-9.4-137.9-27.8a353.84 353.84 0 0 1-112.7-75.9a353.28 353.28 0 0 1-76-112.5C167.3 606.2 158 559.9 158 512s9.4-94.2 27.8-137.8c17.8-42.1 43.4-80 76-112.5s70.5-58.1 112.7-75.9c43.6-18.4 90-27.8 137.9-27.8c47.9 0 94.3 9.3 137.9 27.8c42.2 17.8 80.1 43.4 112.7 75.9c7.9 7.9 15.3 16.1 22.4 24.5c3 3.7 7.6 5.8 12.3 5.8H868c6.3 0 10.2-7 6.7-12.3C798 160.5 663.8 81.6 511.3 82C271.7 82.6 79.6 277.1 82 516.4C84.4 751.9 276.2 942 512.4 942c152.1 0 285.7-78.8 362.3-197.7c3.4-5.3-.4-12.3-6.7-12.3zm88.9-226.3L815 393.7c-5.3-4.2-13-.4-13 6.3v76H488c-4.4 0-8 3.6-8 8v56c0 4.4 3.6 8 8 8h314v76c0 6.7 7.8 10.5 13 6.3l141.9-112a8 8 0 0 0 0-12.6z" fill="#006ca9" /></svg>
                </div>
                <div class="justify-self-center textt">
                    <NuxtLink to=/> Logout </NuxtLink>
                </div>
                <div class=" justify-self-end none">
                </div>
            </div>
            <hr>

        </div>
    </div>
    <div class=" pos1">
        <div class="d-flex justify-content-between">

            <div class=" justify-self-start">
                <button data-bs-toggle="offcanvas" data-bs-target="#offcanvas" role="button">
                    <img class="logo" src="../static/taj logo.svg" />
                </button></div>

            <div class="search justify-self-center">
                <svg class="search2" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="1em" height="1em" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24">
                    <g fill="none">
                        <path d="M21 21l-4.486-4.494M19 10.5a8.5 8.5 0 1 1-17 0a8.5 8.5 0 0 1 17 0z" stroke="white" stroke-width="2" stroke-linecap="round" />
                    </g>
                </svg>
            </div>
            <NuxtLink to="/wallet">
                <div class="balance justify-self-end d-flex justify-content-evenly">
                    <svg class="balance1" xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="23" height="23" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24">
                        <g fill="none">
                            <path d="M3 5v12.75A3.25 3.25 0 0 0 6.25 21h12a3.25 3.25 0 0 0 3.25-3.25v-8.5A3.251 3.251 0 0 0 19 6.087V5.25A2.25 2.25 0 0 0 16.75 3H5.25a2.25 2.25 0 0 0-2.236 2H3zm2.25 1a.75.75 0 0 1 0-1.5h11.5a.75.75 0 0 1 .75.75V6H5.25zm11 7h2a.75.75 0 0 1 0 1.5h-2a.75.75 0 0 1 0-1.5z" fill="#006ca9" />
                        </g>
                    </svg>
                    <div> &#8377; 4000 </div>
                </div>
            </NuxtLink>
        </div>
    </div>
    <div class="banner"><img class="banner2" src="../static/Banner.png"></div>
    <div class="scrolling-wrapper1">
        <div class="img">
            <NuxtLink to="/patti5"><img class="img1" src="../static/Group 245.svg" /></NuxtLink>
            <NuxtLink to="/patti8"><img class="img1" src="../static/Group 246.svg" /></NuxtLink>
        </div>
    </div>
    <div class="pos2">
        <div class="d-flex justify-content-between">
            <div class="head2 justify-self-start">Top Results</div>

            <div class="head3 justify-self-end">
                <NuxtLink to="/allresults">
                    <div class="view">View All</div>
                </NuxtLink>
            </div>
        </div>
    </div>
</div>
</template>

<script>
export default {
    name: 'Home1',
}
</script>

<style scoped>
.none {
    width: 0px;
}
a{
    color: black;
}
.view{
    color: #006CA9 !important;
    text-decoration: underline;
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
    padding-top: 10px;
}

.logo {
    width: 109px;
    height: 44px;
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
    background: #EFF9FF;
}

.balance1 {
    width: 23px;
    height: 23px;
}

.d-flex {

    align-items: center !important;
}

.banner {
    /* position: relative; */
    width: 90vw;
    max-width: 500px;

    left: 0px;
    right: 0px;
    margin: auto;
    margin-top: 23px;
    background: #C4C4C4;
    border-radius: 20px;
    display: flex;
    justify-content: center;
    /* margin-left: 12px */
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

.banner2 {
    width: 90vw;
    max-width: 1000px;
    height: 243px;
}

.scrolling-wrapper1 {
    padding-top: 13px;
    overflow-x: scroll;
    overflow-y: hidden;
    white-space: nowrap;

}

.scrolling-wrapper1 .img {
    display: inline-block;
    margin-right: 5px;

}

.img1 {
    width: 270px;
    height: 221px;
    margin-right: 10px;
}

.scrolling-wrapper1::-webkit-scrollbar {
    display: none;
}

.pos2 {
    height: 25px;
    padding-left: 12px;
    padding-right: 12px;
    padding-top: 30px;
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

@media only screen and (min-width: 766px) {

    .scrolling-wrapper1 {
        padding-top: 13px;
        overflow-x: scroll;
        overflow-y: hidden;
        white-space: nowrap;
        display: flex;
        justify-content: center;
    }

}
</style>

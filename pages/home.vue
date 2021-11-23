<template>
<div v-if="$vuetify.breakpoint.smAndDown">
    <div id="offcanvas" class="offcanvas offcanvas-start h-100 b" tabindex="-1" data-bs-keyboard="false" data-bs-backdrop="false">
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
                    <span class="btntext" @click="func();">Share App</span>
                    <div v-show="modal_1" class="c-modal">
                        <h3 class="text-center">Share Taj Exchange App</h3>
                        <div class="d-flex justify-content-around ptop">
                            <a href="https://api.whatsapp.com/send?text=www.google.com" data-action="share/whatsapp/share" target="_blank" @click="func">
                                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="40" height="40" preserveAspectRatio="xMidYMid meet" viewBox="0 0 256 259">
                                    <path d="M67.663 221.823l4.185 2.093c17.44 10.463 36.971 15.346 56.503 15.346c61.385 0 111.609-50.224 111.609-111.609c0-29.297-11.859-57.897-32.785-78.824c-20.927-20.927-48.83-32.785-78.824-32.785c-61.385 0-111.61 50.224-110.912 112.307c0 20.926 6.278 41.156 16.741 58.594l2.79 4.186l-11.16 41.156l41.853-10.464z" fill="#00E676" />
                                    <path d="M219.033 37.668C195.316 13.254 162.531 0 129.048 0C57.898 0 .698 57.897 1.395 128.35c0 22.322 6.278 43.947 16.742 63.478L0 258.096l67.663-17.439c18.834 10.464 39.76 15.347 60.688 15.347c70.453 0 127.653-57.898 127.653-128.35c0-34.181-13.254-66.269-36.97-89.986zM129.048 234.38c-18.834 0-37.668-4.882-53.712-14.648l-4.185-2.093l-40.458 10.463l10.463-39.76l-2.79-4.186C7.673 134.63 22.322 69.058 72.546 38.365c50.224-30.692 115.097-16.043 145.79 34.181c30.692 50.224 16.043 115.097-34.18 145.79c-16.045 10.463-35.576 16.043-55.108 16.043zm61.385-77.428l-7.673-3.488s-11.16-4.883-18.136-8.371c-.698 0-1.395-.698-2.093-.698c-2.093 0-3.488.698-4.883 1.396c0 0-.697.697-10.463 11.858c-.698 1.395-2.093 2.093-3.488 2.093h-.698c-.697 0-2.092-.698-2.79-1.395l-3.488-1.395c-7.673-3.488-14.648-7.674-20.229-13.254c-1.395-1.395-3.488-2.79-4.883-4.185c-4.883-4.883-9.766-10.464-13.253-16.742l-.698-1.395c-.697-.698-.697-1.395-1.395-2.79c0-1.395 0-2.79.698-3.488c0 0 2.79-3.488 4.882-5.58c1.396-1.396 2.093-3.488 3.488-4.883c1.395-2.093 2.093-4.883 1.395-6.976c-.697-3.488-9.068-22.322-11.16-26.507c-1.396-2.093-2.79-2.79-4.883-3.488H83.01c-1.396 0-2.79.698-4.186.698l-.698.697c-1.395.698-2.79 2.093-4.185 2.79c-1.395 1.396-2.093 2.79-3.488 4.186c-4.883 6.278-7.673 13.951-7.673 21.624c0 5.58 1.395 11.161 3.488 16.044l.698 2.093c6.278 13.253 14.648 25.112 25.81 35.575l2.79 2.79c2.092 2.093 4.185 3.488 5.58 5.58c14.649 12.557 31.39 21.625 50.224 26.508c2.093.697 4.883.697 6.976 1.395h6.975c3.488 0 7.673-1.395 10.464-2.79c2.092-1.395 3.487-1.395 4.882-2.79l1.396-1.396c1.395-1.395 2.79-2.092 4.185-3.487c1.395-1.395 2.79-2.79 3.488-4.186c1.395-2.79 2.092-6.278 2.79-9.765v-4.883s-.698-.698-2.093-1.395z" fill="#FFF" />
                                </svg>
                            </a>
                            <a href="https://www.facebook.com/sharer.php?u=www.google.com" target="_blank" @click="func">
                                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="40" height="40" preserveAspectRatio="xMidYMid meet" viewBox="0 0 24 24">
                                    <g fill="none">
                                        <path fill-rule="evenodd" clip-rule="evenodd" d="M0 12.067C0 18.033 4.333 22.994 10 24v-8.667H7V12h3V9.333c0-3 1.933-4.666 4.667-4.666c.866 0 1.8.133 2.666.266V8H15.8c-1.467 0-1.8.733-1.8 1.667V12h3.2l-.533 3.333H14V24c5.667-1.006 10-5.966 10-11.933C24 5.43 18.6 0 12 0S0 5.43 0 12.067z" fill="#3b5998" />
                                    </g>
                                </svg>
                            </a>
                            <a href="https://t.me/share/url?url=www.google.com&text=Taj Exchange" target="_blank" @click="func">
                                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="40" height="40" preserveAspectRatio="xMidYMid meet" viewBox="0 0 256 256">
                                    <path d="M128 0C57.307 0 0 57.307 0 128s57.307 128 128 128s128-57.307 128-128S198.693 0 128 0z" fill="#40B3E0" />
                                    <path d="M190.283 73.63L167.42 188.899s-3.197 7.994-11.99 4.157l-52.758-40.448l-19.184-9.272l-32.294-10.872s-4.956-1.758-5.436-5.595c-.48-3.837 5.596-5.915 5.596-5.915l128.376-50.36s10.552-4.636 10.552 3.038" fill="#FFF" />
                                    <path d="M98.618 187.603s-1.54-.144-3.46-6.22c-1.917-6.075-11.67-38.049-11.67-38.049l77.538-49.24s4.477-2.718 4.317 0c0 0 .799.48-1.6 2.718c-2.397 2.239-60.91 54.836-60.91 54.836" fill="#D2E5F1" />
                                    <path d="M122.901 168.115l-20.867 19.026s-1.632 1.238-3.416.462l3.996-35.34" fill="#B5CFE4" />
                                </svg>
                            </a>
                        </div>
                        <div class="d-flex justify-content-around pbot">
                            <div class="social">Whatsapp</div>
                            <div class="social">Facebook</div>
                            <div class="social">Telegram</div>
                        </div>

                        <!-- <div class="d-flex justify-content-around ptop">
                            <a href="https://reddit.com/submit?url=www.google.com&title=Taj Exchange" target="_blank" @click="func">
                                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="40" height="40" preserveAspectRatio="xMidYMid meet" viewBox="0 0 256 256">
                                    <circle fill="#FF4500" cx="128" cy="128" r="128" />
                                    <path d="M213.15 129.22c0-10.376-8.391-18.617-18.617-18.617a18.74 18.74 0 0 0-12.97 5.189c-12.818-9.157-30.368-15.107-49.9-15.87l8.544-39.981l27.773 5.95c.307 7.02 6.104 12.667 13.278 12.667c7.324 0 13.275-5.95 13.275-13.278c0-7.324-5.95-13.275-13.275-13.275c-5.188 0-9.768 3.052-11.904 7.478l-30.976-6.562c-.916-.154-1.832 0-2.443.458c-.763.458-1.22 1.22-1.371 2.136l-9.464 44.558c-19.837.612-37.692 6.562-50.662 15.872a18.74 18.74 0 0 0-12.971-5.188c-10.377 0-18.617 8.391-18.617 18.617c0 7.629 4.577 14.037 10.988 16.939a33.598 33.598 0 0 0-.458 5.646c0 28.686 33.42 52.036 74.621 52.036c41.202 0 74.622-23.196 74.622-52.036a35.29 35.29 0 0 0-.458-5.646c6.408-2.902 10.985-9.464 10.985-17.093zM85.272 142.495c0-7.324 5.95-13.275 13.278-13.275c7.324 0 13.275 5.95 13.275 13.275s-5.95 13.278-13.275 13.278c-7.327.15-13.278-5.953-13.278-13.278zm74.317 35.251c-9.156 9.157-26.553 9.768-31.588 9.768c-5.188 0-22.584-.765-31.59-9.768c-1.371-1.373-1.371-3.51 0-4.883c1.374-1.371 3.51-1.371 4.884 0c5.8 5.8 18.008 7.782 26.706 7.782c8.699 0 21.058-1.983 26.704-7.782c1.374-1.371 3.51-1.371 4.884 0c1.22 1.373 1.22 3.51 0 4.883zm-2.443-21.822c-7.325 0-13.275-5.95-13.275-13.275s5.95-13.275 13.275-13.275c7.327 0 13.277 5.95 13.277 13.275c0 7.17-5.95 13.275-13.277 13.275z" fill="#FFF" />
                                </svg>
                            </a>
                            <a href="https://pinterest.com/pin/create/bookmarklet/?&url=www.google.com&description=Taj Exchange" target="_blank" @click="func">
                                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="40" height="40" preserveAspectRatio="xMidYMid meet" viewBox="0 0 256 256">
                                    <path d="M0 128.002c0 52.414 31.518 97.442 76.619 117.239c-.36-8.938-.064-19.668 2.228-29.393c2.461-10.391 16.47-69.748 16.47-69.748s-4.089-8.173-4.089-20.252c0-18.969 10.994-33.136 24.686-33.136c11.643 0 17.268 8.745 17.268 19.217c0 11.704-7.465 29.211-11.304 45.426c-3.207 13.578 6.808 24.653 20.203 24.653c24.252 0 40.586-31.149 40.586-68.055c0-28.054-18.895-49.052-53.262-49.052c-38.828 0-63.017 28.956-63.017 61.3c0 11.152 3.288 19.016 8.438 25.106c2.368 2.797 2.697 3.922 1.84 7.134c-.614 2.355-2.024 8.025-2.608 10.272c-.852 3.242-3.479 4.401-6.409 3.204c-17.884-7.301-26.213-26.886-26.213-48.902c0-36.361 30.666-79.961 91.482-79.961c48.87 0 81.035 35.364 81.035 73.325c0 50.213-27.916 87.726-69.066 87.726c-13.819 0-26.818-7.47-31.271-15.955c0 0-7.431 29.492-9.005 35.187c-2.714 9.869-8.026 19.733-12.883 27.421a127.897 127.897 0 0 0 36.277 5.249c70.684 0 127.996-57.309 127.996-128.005C256.001 57.309 198.689 0 128.005 0C57.314 0 0 57.309 0 128.002z" fill="#CB1F27" /></svg>
                            </a>
                            <a href="https://www.linkedin.com/shareArticle?url=www.google.com&title=Taj Exchange" target="_blank" @click="func">
                                <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="40" height="40" preserveAspectRatio="xMidYMid meet" viewBox="0 0 256 256">
                                    <path d="M218.123 218.127h-37.931v-59.403c0-14.165-.253-32.4-19.728-32.4c-19.756 0-22.779 15.434-22.779 31.369v60.43h-37.93V95.967h36.413v16.694h.51a39.907 39.907 0 0 1 35.928-19.733c38.445 0 45.533 25.288 45.533 58.186l-.016 67.013zM56.955 79.27c-12.157.002-22.014-9.852-22.016-22.009c-.002-12.157 9.851-22.014 22.008-22.016c12.157-.003 22.014 9.851 22.016 22.008A22.013 22.013 0 0 1 56.955 79.27m18.966 138.858H37.95V95.967h37.97v122.16zM237.033.018H18.89C8.58-.098.125 8.161-.001 18.471v219.053c.122 10.315 8.576 18.582 18.89 18.474h218.144c10.336.128 18.823-8.139 18.966-18.474V18.454c-.147-10.33-8.635-18.588-18.966-18.453" fill="#0A66C2" /></svg>
                            </a>
                        </div> -->
                    </div>
                    <div v-show="modal_1" class="bg2" @click="func();"></div>
                </div>
                <div class=" justify-self-end none">
                </div>
            </div>
            <hr>
            <div class="d-flex justify-content-between p">
                <div class=" justify-self-start">
                    <svg xmlns="http://www.w3.org/2000/svg" xmlns:xlink="http://www.w3.org/1999/xlink" aria-hidden="true" role="img" width="16" height="16" preserveAspectRatio="xMidYMid meet" viewBox="0 0 32 32">
                        <path d="M14 23h8v2h-8z" fill="#006ca9" />
                        <path d="M10 23h2v2h-2z" fill="#006ca9" />
                        <path d="M14 18h8v2h-8z" fill="#006ca9" />
                        <path d="M10 18h2v2h-2z" fill="#006ca9" />
                        <path d="M14 13h8v2h-8z" fill="#006ca9" />
                        <path d="M10 13h2v2h-2z" fill="#006ca9" />
                        <path d="M25 5h-3V4a2 2 0 0 0-2-2h-8a2 2 0 0 0-2 2v1H7a2 2 0 0 0-2 2v21a2 2 0 0 0 2 2h18a2 2 0 0 0 2-2V7a2 2 0 0 0-2-2zM12 4h8v4h-8zm13 24H7V7h3v3h12V7h3z" fill="#006ca9" /></svg>
                </div>
                <div class="justify-self-center textt">
                    <NuxtLink to="/allresults">Reuslts</NuxtLink>
                </div>
                <div class=" justify-self-end none">
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
                    <NuxtLink to="/wallet">Wallet </NuxtLink>
                </div>
                <div class=" justify-self-end none">
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
                    <NuxtLink to="/"> Logout </NuxtLink>
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
        <div class="align2">
            <div class="d-flex justify-content-between align">
                <div class="head2 justify-self-start">Top Results</div>

                <div class="head3 justify-self-end">
                    <NuxtLink to="/allresults">
                        <div class="view">View All</div>
                    </NuxtLink>
                </div>
            </div>
        </div>
    </div>
    <home2 />
    <home3 />
    <home4 />
    <home5 />
</div>
</template>

<script>
export default {
    name: 'Home1',
    data() {
        return {
            modal_1: false,
        }
    },
    methods: {
        func() {
            this.modal_1 = !this.modal_1
        },
    },
}
</script>

<style scoped>
.none {
    width: 0px;
}

a {
    color: black;
}

.view {
    color: #006ca9 !important;
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
.social{
    width: 40px;
    font-size: 12px;
}
.b {
    border: 1px solid #006ca9 !important;
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
    background: #006ca9;
}

.balance {
    border: 1px solid #006ca9;
    border-radius: 30px;
    width: 109px;
    height: 35px;
    vertical-align: middle;
    background: #eff9ff;
}

@media only screen and (max-width: 300px) {
    .balance {
        width: 90px;
        height: 35px;
    }
}

.balance1 {
    width: 23px;
    height: 23px;
}

.d-flex {
    align-items: center !important;
}

.banner {
    width: 90vw;
    max-width: 500px;
    left: 0px;
    right: 0px;
    margin: auto;
    margin-top: 23px;
    background: #c4c4c4;
    border-radius: 20px;
    /* margin-right: 0 !important;
    margin-right: 0 !important; */
    display: flex;
    justify-content: center;
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
    color: #006ca9;
    z-index: 10;
}

.align2 {
    display: flex;
    justify-content: center;
    margin-left: -12px;
}

.align {
    max-width: 600px;
    width: 84vw;
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

.c-modal {
    position: fixed;
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    margin: auto;
    width: 70%;
    max-width: 300px;
    height: 246px;
    padding: 12px;
    background-color: white;
    border-radius: 5px;
    /* background-color: rgba(#fff, .4); */
    z-index: 10001;
    opacity: 1;
    transition: 0.6s;
}

.bg2 {
    display: block;
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background-color: rgba(0, 0, 0, 0.6);
    z-index: 10000;
    opacity: 1;
    transition: 0.3s;
}

.ptop {
    padding-top: 50px;
    /* height: 130px; */
}

@media only screen and (max-width: 320px) {
    .c-modal {
        width: 90%;
    }
}
</style>

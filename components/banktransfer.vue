<template>
<div>
    <div class="details">
        <div class="card">
            <div class="card-text">
                <div class="head1">
                    Bank Details
                </div>
                <div class="head2">
                    Account Number
                </div>
                <div class="d-flex align-items-center">
                    <div class="number">
                        {{number}}
                    </div>
                    <button v-clipboard:copy="number" type="button">
                        <div class="iconpaste"></div>
                    </button>
                </div>
                <div class="d-flex">
                    <div class="p">
                        <div class="head3">IFSC CODE</div>
                        <div class="d-flex align-items-center">
                            <div class="code">{{code}}</div>
                            <button v-clipboard:copy="code" type="button">
                                <div class="iconpaste"></div>
                            </button>
                        </div>
                    </div>
                    <div>
                        <div class="head3">Branch Name</div>
                        <div class="d-flex align-items-center">
                            <div class="name">{{name}}</div>
                            <button v-clipboard:copy="name" type="button">
                                <div class="iconpaste"></div>
                            </button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <form>
            <div class="head4">Enter Amount to deposit</div>
            <input type="number" class="formelement" placeholder="2000" required>
            <div class="head4 height">Upload Transfer Screenshot</div>
            <input id="upload" type="file" accept="image/*" required hidden @change="onFileChanged" />
            <div class="screen">
                <label class="screenshot" for="upload">
                    <div class="iconupload"></div>
                </label>
            </div>
            <div v-if="files">
                <div v-for="(file, index) in files" :key="index" class="filename">
                    {{ file.name }}
                </div>
            </div>
            <div class="head4">Enter UTR ID</div>
            <input type="number" class="formelement" placeholder="UTR Number" required>
            <br>
            <button class="button"><span class="btntext">Make Payment</span></button>
        </form>
    </div>
</div>
</template>

<script>
export default {
    name: 'Banktransfer',
    data() {
        return {
            number: '81510887102004',
            code: 'HDFC10502',
            name: 'Matunga',
            files: false
        }
    },
    methods: {
        onFileChanged(e) {
            const files = e.target.files;
            this.files = files;
        }
    }
}
</script>

<style scoped>
.card {
    width: 85vw;
    max-width: 400px;
    height: 203px;
    background: #FFFFFF;
    box-shadow: 0px 2px 12px rgba(0, 0, 0, 0.12);
    border-radius: 12px;
    left: 0;
    right: 0;
    margin: auto;
    background: #FFFFFF;
    box-shadow: 0px 2px 12px rgba(0, 0, 0, 0.12);
    border-radius: 12px;
    padding: 10px 15px;
    margin-top: 25px;
}

.head1 {
    width: 116px;
    height: 27px;
    font-family: Nunito;
    font-style: normal;
    font-weight: bold;
    font-size: 20px;
    line-height: 27px;
    color: #000000;
}

.head2 {
    height: 22px;
    font-family: Nunito;
    font-style: normal;
    font-weight: bold;
    font-size: 16px;
    line-height: 22px;
    color: #000000;
    margin-top: 20px;
}

.number {
    /* width: 152px; */
    height: 25px;
    font-family: Nunito;
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 25px;
    margin-top: 5px;
    padding-right: 5px;
}

.head3 {
    width: 100px;
    height: 22px;
    font-family: Nunito;
    font-style: normal;
    font-weight: bold;
    font-size: 16px;
    line-height: 22px;
    margin-top: 10px;
}

.p {
    margin-right: 25px;
}

.code {
    margin-top: 5px;
    /* width: 103px; */
    height: 25px;
    font-family: Nunito;
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 25px;
    color: #000000;
    padding-right: 5px;
}

.name {
    /* width: 72px; */
    height: 25px;
    font-family: Nunito;
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 25px;
    color: #000000;
    margin-top: 5px;
    padding-right: 5px;
}

.head4 {
    width: 85vw;
    max-width: 400px;
    left: 0;
    right: 0;
    margin: auto;
    height: 27px;
    font-family: Nunito;
    font-style: normal;
    font-weight: bold;
    font-size: 20px;
    line-height: 27px;
    color: #000000;
    margin-top: 25px;
}

.screenshot {
    width: 85vw;
    max-width: 400px;
    height: 114px;
    border: 1px solid #CECECE;
    box-sizing: border-box;
    left: 0;
    right: 0;
    margin: auto;
    margin-top: 25px;
}

.screen {
    display: flex;
    justify-content: center;
}

.filename {
    width: 85vw;
    max-width: 400px;
    left: 0;
    right: 0;
    margin: auto;
    height: 27px;
    font-family: Nunito;
    font-style: normal;
    font-weight: bold;
    font-size: 14px;
    line-height: 27px;
    color: #000000;
    margin-top: 5px;
}

@media only screen and (max-width: 300px) {
    .height {
        font-size: 18px;
    }

    .head1 {
        font-size: 18px;
    }

    .head2 {
        font-size: 14px;
    }

    .head3 {
        font-size: 14px;
    }

    .name {
        font-size: 16px;
        margin-top: 0px;

    }

    .code {
        font-size: 16px;
        margin-top: 0px;
    }
}

.formelement {
    width: 85vw;
    max-width: 400px;
    display: flex;
    justify-content: center;
    height: 40px;
    left: 0;
    right: 0;
    margin: auto;
    border-bottom: 1px solid grey;
}

input {
    margin-top: 10px !important;
    width: 85vw;
    max-width: 400px;
    height: 40px;
    left: 0;
    right: 0;
    margin: auto;
}

input[type="number"] {
    font-size: 18px !important;
}

textarea:focus,
input:focus {
    outline: none;
}

.button {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 8px;
    background: #006CA9;
    border-radius: 20px;
    max-width: 400px;
    width: 84vw;
    left: 0;
    right: 0;
    margin: auto;
    margin-top: 25px;

}

.btntext {
    font-family: Poppins;
    font-style: normal;
    font-weight: 500;
    font-size: 14px;
    line-height: 21px;
    display: flex;
    align-items: center;
    color: #FFFFFF;
}

.iconpaste {
    width: 21px;
    height: 20px;
    background: url('data:image/svg+xml,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20xmlns%3Axlink%3D%22http%3A%2F%2Fwww.w3.org%2F1999%2Fxlink%22%20width%3D%2220%22%20height%3D%2221%22%20preserveAspectRatio%3D%22xMidYMid%20meet%22%20viewBox%3D%220%200%2024%2024%22%3E%3Cg%20fill%3D%22none%22%3E%3Cpath%20d%3D%22M8%204v12a2%202%200%200%200%202%202h8a2%202%200%200%200%202-2V7.242a2%202%200%200%200-.602-1.43L16.083%202.57A2%202%200%200%200%2014.685%202H10a2%202%200%200%200-2%202z%22%20stroke%3D%22%23006ca9%22%20stroke-width%3D%222%22%20stroke-linecap%3D%22round%22%20stroke-linejoin%3D%22round%22%2F%3E%3Cpath%20d%3D%22M16%2018v2a2%202%200%200%201-2%202H6a2%202%200%200%201-2-2V9a2%202%200%200%201%202-2h2%22%20stroke%3D%22%23006ca9%22%20stroke-width%3D%222%22%20stroke-linecap%3D%22round%22%20stroke-linejoin%3D%22round%22%2F%3E%3C%2Fg%3E%3C%2Fsvg%3E');
    background-repeat: no-repeat;
    background-size: 100%;
}

.iconupload {
    width: 52px;
    height: 52px;
    background: url('data:image/svg+xml,%3Csvg%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%20xmlns%3Axlink%3D%22http%3A%2F%2Fwww.w3.org%2F1999%2Fxlink%22%20width%3D%2252%22%20height%3D%2252%22%20preserveAspectRatio%3D%22xMidYMid%20meet%22%20viewBox%3D%220%200%201024%201024%22%3E%3Cpath%20d%3D%22M400%20317.7h73.9V656c0%204.4%203.6%208%208%208h60c4.4%200%208-3.6%208-8V317.7H624c6.7%200%2010.4-7.7%206.3-12.9L518.3%20163a8%208%200%200%200-12.6%200l-112%20141.7c-4.1%205.3-.4%2013%206.3%2013zM878%20626h-60c-4.4%200-8%203.6-8%208v154H214V634c0-4.4-3.6-8-8-8h-60c-4.4%200-8%203.6-8%208v198c0%2017.7%2014.3%2032%2032%2032h684c17.7%200%2032-14.3%2032-32V634c0-4.4-3.6-8-8-8z%22%20fill%3D%22black%22%2F%3E%3C%2Fsvg%3E');
    background-repeat: no-repeat;
    background-size: 100%;
    left: 0;
    right: 0;
    margin: auto;
    transform: translateY(50%);
}
</style>

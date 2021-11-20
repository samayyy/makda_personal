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
                <div class="number">
                    81510887102004
                </div>
                <div class="d-flex">
                    <div class="p">
                        <div class="head3">IFSC CODE</div>
                        <div class="code">HDFC10502</div>
                    </div>
                    <div>
                        <div class="head3">Branch Name</div>
                        <div class="name">Matunga</div>
                    </div>
                </div>
            </div>
        </div>
        <form>
            <div class="head4">Enter Amount to deposit</div>
            <input type="number" class="formelement" placeholder="$2000" required>
            <div class="head4">Upload Transfer Screenshot</div>
            <div class="head4">Enter UTR ID</div>
            <input type="number" class="formelement" placeholder="UTR Number" required>
            <br>
            <button class="button"><span class="btntext">Make Payment</span></button>
        </form>
    </div>
</div>
</template>

<style scoped>
.card {
    width: 85vw;
    /* max-width: 400px; */
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
    margin-bottom: 15px;
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
    width: 125px;
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
    width: 152px;
    height: 25px;
    font-family: Nunito;
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 25px;
    margin-top: 5px;
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
   margin-top: 15px;
    width: 103px;
    height: 25px;
    font-family: Nunito;
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 25px;
    color: #000000;
}

.name {
    width: 72px;
    height: 25px;
    font-family: Nunito;
    font-style: normal;
    font-weight: normal;
    font-size: 18px;
    line-height: 25px;
    color: #000000;
    margin-top: 15px;
}

.head4 {
    /* width: 231px; */
    height: 27px;
    font-family: Nunito;
    font-style: normal;
    font-weight: bold;
    font-size: 20px;
    line-height: 27px;
    color: #000000;
}
.formelement {
    width: 95%;
    max-width: 400px;
    height: 40px;
    left: 0;
    right: 0;
    margin: auto;
    /* display: flex;
    justify-content: center; */
    padding: 5px 10px;
    border-bottom: 1px solid grey;
}

input {
    margin-top: 5px !important;
    margin-bottom: 10px !important;
}

input[type="number"] {
    font-size: 18px !important;
}

textarea:focus,
input:focus {
    outline: none;
}
.details
{   margin-left: 7.5vw;
    /* display: flex;
    flex-direction: column;
    justify-content: center; */
}
</style>

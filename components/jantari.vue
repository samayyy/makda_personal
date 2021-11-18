<template>
<div>
    <div class="jantari">
        <div class="d-flex justify-content-around">
            <div class="num">01</div>
            <div class="num">02</div>
            <div class="num">03</div>
            <div class="num">04</div>
            <div class="num">05</div>
            <div class="num">06</div>

        </div>
        <div class="d-flex justify-content-around ">
            <div v-for="index in 6" :key="index">
                <input class="input" />
            </div>

        </div>
        <div class="d-flex justify-content-around p">
            <div class="num">07</div>
            <div class="num">08</div>
            <div class="num">09</div>
            <div class="num">10</div>
            <div class="num">11</div>
            <div class="num">12</div>

        </div>
        <div class="d-flex justify-content-around ">
            <div v-for="index in 6" :key="index">
                <input class="input" />
            </div>

        </div>
        <div class="d-flex justify-content-around p">
            <div class="num">13</div>
            <div class="num">14</div>
            <div class="num">15</div>
            <div class="num">16</div>
            <div class="num">17</div>
            <div class="num">18</div>

        </div>
        <div class="d-flex justify-content-around ">
            <div v-for="index in 6" :key="index">
                <input class="input" />
            </div>

        </div>
        <div class="d-flex justify-content-around p">
            <div class="num">19</div>
            <div class="num">20</div>
            <div class="num">21</div>
            <div class="num">22</div>
            <div class="num">23</div>
            <div class="num">24</div>

        </div>
        <div class="d-flex justify-content-around">
            <div v-for="index in 6" :key="index">
                <input class="input" />
            </div>

        </div>
        <div class="d-flex justify-content-around p">
            <div class="num">25</div>
            <div class="num">26</div>
            <div class="num">27</div>
            <div class="num">28</div>
            <div class="num">29</div>
            <div class="num">30</div>

        </div>
        <div class="d-flex justify-content-around">
            <div v-for="index in 6" :key="index">
                <input class="input" />
            </div>

        </div>
        <div class="d-flex justify-content-around p">
            <div class="num">31</div>
            <div class="num">32</div>
            <div class="num">33</div>
            <div class="num">34</div>
            <div class="num">35</div>
            <div class="num">36</div>

        </div>
        <div class="d-flex justify-content-around">
            <div v-for="index in 6" :key="index">
                <input class="input" />
            </div>

        </div>
        <div class="d-flex justify-content-around p">
            <div class="num">37</div>
            <div class="num">38</div>
            <div class="num">39</div>
            <div class="num">40</div>
            <div class="num">41</div>
            <div class="num">42</div>

        </div>
        <div class="d-flex justify-content-around">
            <div v-for="index in 6" :key="index">
                <input class="input" />
            </div>

        </div>
        <div class="d-flex justify-content-around p">
            <div class="num">43</div>
            <div class="num">44</div>
            <div class="num">45</div>
            <div class="num">46</div>
            <div class="num">47</div>
            <div class="num">48</div>

        </div>
        <div class="d-flex justify-content-around">
            <div v-for="index in 6" :key="index">
                <input class="input" />
            </div>

        </div>
        <div class="bottom">
            <div class="text2"><span>TOTAL: 0</span></div>
            <NuxtLink to=/games> <button class="button"><span class="btntext">Submit</span></button></NuxtLink>
        </div>
    </div>
</div>
</template>

<style scoped>
.jantari {
    padding-top: 25px;
    left: 0;
    right: 0;
    margin: auto;
}

.num {
    width: 25px;
    height: 22px;
    font-family: Nunito;
    font-style: normal;
    font-weight: 600;
    font-size: 16px;
    line-height: 22px;
    color: #000000;
    display: flex;
    justify-content: center;
}

.input {
    width: 25px;
    height: 22px;
    border-bottom: 1px solid black !important;
    display: flex;
    justify-content: center;
}

input {
    font-family: Nunito;
    font-style: normal;
    font-weight: 600;
    font-size: 16px !important;
    line-height: 22px;
    color: #000000;
}

textarea:focus,
input:focus {
    outline: none;
}

.p {
    padding-top: 22px;
}

.bottom {
    padding-top: 25px;
    display: flex;
    justify-content: center;
    flex-direction: column;
    align-items: center;
}

.text2 {
    height: 27px;
    font-family: Nunito;
    font-style: normal;
    font-weight: bold;
    font-size: 20px;
    line-height: 27px;
    color: #000000;
}

.button {
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    padding: 8px;
    width: 90vw;
    max-width: 330px;
    height: 40px;
    background: #006CA9;
    border-radius: 20px;
    color: white !important;
    text-decoration: none !important;
    margin-top: 20px;
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
</style>

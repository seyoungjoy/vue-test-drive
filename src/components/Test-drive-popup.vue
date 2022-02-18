<template>
    <div class="popup-wrap">
        <div class="popup-form">
            <h1>시승신청 내역을 확인해주세요</h1>
            <ul class="carInfo">
                <li>LS 500</li>
                <li><figure>
                    <img src="../assets/img/ls500hImg.jpeg">
                </figure></li>
            </ul>
            <ul class="locationInfo">
                <li>렉서스 서울 전시장</li>
                <li>031-983-2323</li>
                <li>경기도 고양시 일산동구 백마로 512</li>
            </ul>
            <v-btn x-large>확인</v-btn>
        </div>
    </div>

</template>
<script>

export default {
    data(){
        return{
        }
    }

}
</script>

<style scoped>
.popup-wrap{
    position: absolute;
    top:0;
    left:0;
    width:100vw;
    height:100vh;
    background:rgba(0,0,0,0.8);
    display: none;
}
.popup-form{
    position: absolute;
    top:50%; left:50%;
    transform: translate(-50%,-50%);
    width:80rem;
    padding:5rem;
    background: #fff;
    text-align: center;
    border:1px solid #000;
}
.carInfo li, .locationInfo li{
    padding:0.5rem 0;
    font-size: 1.5rem;
    list-style-type:none;
}
</style>

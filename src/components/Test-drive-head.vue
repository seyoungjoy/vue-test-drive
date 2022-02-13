<template>
    <div>
        <ul>
            <li>{{selectedCar}}</li>
            <li>{{selectedShowRoom}}</li>
            <li>개인정보 입력</li>
        </ul>

    </div>
</template>
<script>
    export default{
        data(){
            return{
                // selectedCar : '차량 선택'
            }
        },
        props:["selectedCar", "selectedShowRoom"]
    }

</script>
<style scoped>
ul{
    display: flex;
    justify-content: center;
    margin:2rem 0;
    list-style: none;
}
ul li{
    padding:0 2rem;
}
</style>
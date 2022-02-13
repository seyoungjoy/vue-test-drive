<template>
    <div>
        <h1>시승신청</h1>
        <TestDriveHead
            :selectedCar = "selectedCar"
            :selectedShowRoom = "selectedShowRoom"
        />
        <TestDriveStep1
            @getCarName="getCarName"
        />
        <TestDriveStep2
            @getShowRoomList="getShowRoomList"
        />
    </div>
</template>
<script>
import TestDriveHead from './Test-drive-head'
import TestDriveStep1 from './Test-drive-step-1'
import TestDriveStep2 from './Test-drive-step-2'

export default{
    data(){
        return{
            selectedCar : '차량선택',
            selectedShowRoom : '전시장 선택',
            status : null,
        }
    },
    components:{
        TestDriveHead,
        TestDriveStep1,
        TestDriveStep2
    },
    methods:{
        getCarName(carName){
            this.selectedCar = carName.name
            
        },
        getShowRoomList(showRoomList){
            this.selectedShowRoom =showRoomList.name 
        }
        
    }
}
</script>

<style scoped>
h1{
    margin:2rem 0 1rem;
    text-align: center;
}
</style>

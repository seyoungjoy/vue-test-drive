<template>
    <div>
        <h1>1</h1>
        <p>시승을 희망하는 모델을 선택해주세요</p>
        <small>* 전시장에 따라 시승 가능한 모델이 상이할 수 있습니다.</small>

        <ul>
            <li 
            v-for="(carList,idx) in carLists" :key="idx"
            @click="getData(carList)"
            >
            <p>{{carList.name}}</p>
            
            </li>
        </ul>
        

    </div>
</template>

<script>
import {eventBus} from "../main"

export default{
    data(){
        return{
            carLists: [
                {id:1, name:'Ls 500h'},
                {id:2, name:'Es 300h'},
                {id:3, name:'UX 250h'},
            ]
        }
    },
    methods:{
        getData(carName){
            this.$emit('getCarName', carName)
            eventBus.$emit('statusOn', 'on')
        },

        
        
        
    },

    
}


</script>

<style scoped>
div{
    margin-bottom:2rem;
    padding:2rem;
    text-align:center;
    border:1px solid #000;
}
ul{
    list-style:none;
    width:50vw;
    margin:0 auto;

}
li{
    margin:1rem 0;
    padding:1rem;
    border:1px solid #000;
    cursor: pointer;
}
small{
    color:red;
}
</style>

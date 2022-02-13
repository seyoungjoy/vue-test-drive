<template>
    <div
        v-if="this.status === 'on'"
    >
        <h1>2</h1>
        <p>시승을 희망하는 지역을 선택해주세요</p>
        <small>* 전시장에 따라 시승 가능한 모델이 상이할 수 있습니다.</small>

        <ul>
            <li
            v-for="(showRoomList, idx) in showRoomLists"
            :key="idx"
            @click="getShowRoomList(showRoomList)"
            >
            {{showRoomList.name}}
            </li>
        </ul>

    </div>
</template>
<script>

    import {eventBus} from "../main"
    export default{
        data(){
            return{
                showRoomLists:[
                    {id:1, name:'서울'},
                    {id:2, name:'인천'},
                    {id:3, name:'경기'},
                ],
                status:'off'
            }
        },
        created(){
            eventBus.$on('statusOn', (status) =>{
                this.status = status
            })
        },
        props:["currentStatus"],
        methods:{
            getShowRoomList(showRoomList){
                this.$emit('getShowRoomList', showRoomList)
            },
            
        }
    }
    

</script>
<style scoped>
div{
    /* display: block; */
    text-align:center;
    padding:2rem;
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

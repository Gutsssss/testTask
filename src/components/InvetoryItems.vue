<template>
    <div class="item">
    <div class="item__inventory" v-on:click="isVisble = !isVisble">
    <div class="item__inventory_counter">{{ itemCounter }}</div>
    <img class="item__inventory_Img"
    :src="itemImg"
     />
    </div>
    </div>
</template>

<script>
export default {
    name:'ItemInventory',
    props:['itemCounter','itemImg']
   
}


    
</script>
<style>
.item__inventory_counter {
    position: absolute;
    color: black;
    bottom: 2px;
    right: 2px;
}
.item__inventory {
    width: 105px;
    height: 100px;
    border: 1px solid #4D4D4D;
    position: relative;
    align-items: center;
    background-color:#262626 ;
    cursor: pointer;
}
.item__inventory:hover {
    background-color: #2F2F2F;
}
.item__inventory_Img {
    width:54px ;
    height: 54px;
    left: 27px;
    position: absolute;
    top: 27px;
    
   
}

</style>
<template>
    <div class="item">
    <div class="item__inventory">
    <div class="item__inventory_counter">{{ itemCounter }}
    </div>
    <img class="item__inventory_Img"
    :src="require(itemImg)"
     />
    </div>
    </div>
</template>

<script>
export default {
    name:'ItemInventory',
    props:['itemCounter','itemImg',],
    
   
}
</script>
<style>
.item__inventory_counter {
    position: absolute;
    color: rgba(77, 77, 77, 1);
    bottom: 0px;
    right: 0px;
    width: 16px;
    height: 16px;
    border:1px solid rgba(77, 77, 77, 1) ;
    border-radius: 6px 0 0 0 ;
}
.item__inventory {
    width: 103px;
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
    left: 27px;
    position: absolute;
    top: 27px;
    
   
}

</style>
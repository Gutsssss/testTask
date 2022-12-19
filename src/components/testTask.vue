<template>
<div class="main">
    <div class="main__left">
    <img class="main__left__img" src="@/assets/logo.png">
    <div class="main__left__description">
    <img class="main__left__description_1" src="@/assets/Stub.png">
    <img class="main__left__description_2" src="@/assets/Stub.png">
    <img class="main__left__description_3" src="@/assets/Stub.png">
    <img class="main__left__description_4" src="@/assets/Stub.png">
    <img class="main__left__description_5" src="@/assets/Stub.png">
    <img class="main__left__description_6" src="@/assets/Stub.png">
    <img class="main__left__description_7" src="@/assets/Stub.png">
    </div>
    </div>
    <div class="main__right">
    <ul class="main__right_ul">
    <div v-for="(item,index) in items"
    :key="index"
    ><InventoryItems
     :itemCounter = item.itemCounter
     :itemImg = item.itemImg
     /></div>
    </ul>
    <!-- <div class="toggle"><InventoryToggle /></div> -->
    <div class="main__down"><img class="main__down__description" src="@/assets/Skeleton.png"><img class="main__down__close" src="@/assets/Vector.png"> </div>
    </div>
</div>
</template>


<script>
import InventoryItems from '@/components/InvetoryItems.vue'
export default { 
    components: {
    InventoryItems,
    
},
    data() {
    return {
        items: [{itemCounter:4, itemImg:"@/assets/Skeleton.png"},
        {itemCounter:2,itemImg:"@/assets/Rectangle8.png"},
        {itemCounter:5,itemImg:"@/assets/Rectangle8.png"},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},
        {itemCounter:null,itemImg:" "},]
    }
    
}}
</script>
<style> 
.main {
    width: 849px;
    height: 660px;
    display: flex;
    background-color: black;
    padding: 0 5px
}
.main__left {
    border-radius:12px ;
    width: 236px;
    height: 500px;
    background-color:#262626;
    border: 1px solid #4D4D4D;
    margin-right: 12px;
    margin-top: 32px;
    margin-left: 32px;
}
.main__left__img {
    margin-top:18px;
    padding-bottom: 20px;
}
.main__left__description {
    height: 230px;
}
.main__left__description_1 {
    padding-bottom: 24px;
}
.main__left__description_2 {
    width: 155px;
    height: 10px;
    padding-bottom: 8px;
}
.main__left__description_3 {
    width: 190px;
    height: 10px;
    padding-top: 8px;
    padding-bottom:8px ;
}
.main__left__description_4 {
    width: 170px;
    height: 10px;
    padding-top: 8px;
    padding-bottom:8px ;
}
.main__left__description_5 {
    width:160px ;
    height: 10px;
    padding-top: 8px;
    padding-bottom:8px ;
}
.main__left__description_6 {
    width: 140px;
    height: 10px;
    padding-top: 8px;
}
.main__left__description_7 {
    width: 80px;
    height: 10px;
    padding-top:24px ;
}
.main__right {
    width: 540px;
    height: 500px;
    margin-left: 12px;
    position: relative;
    margin-top: 32px;
}
.main__right__toggleShow {
    width: 250px;
    height: 500px;
    position: absolute;
    left: 273px;
}
.main__right_ul {
    display: flex;
    padding: 0;
    flex-wrap: wrap;
    margin-top: 0;
    margin-bottom: 0;
}
.main__down {
    background-color:#262626;
    width: 785px;
    height: 72px;
    margin: 24px;
    border-radius:12px ;
    text-align: center;
    border: 1px solid #4D4D4D;
    position: absolute;
    left: -279px;
}
.main__down__description {
    margin: 0 auto;
    text-align: center;
    padding: 18px;
    padding-right: 68px;
}
.main__down__close {
    position: absolute;
    left: 97%;
    right: 25%;
    top: 15%;
    bottom: 25%;
    cursor: pointer;
}

</style>
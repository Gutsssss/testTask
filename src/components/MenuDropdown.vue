<template>
    <div class="item">
        <img class="item__inventory_picture"
        :src="itemImg"
     />
     <div>
    <div class="item__inventory__description">
    <img class="item__inventory__description_1" src="@/assets/Stub.png">
    <img class="item__inventory__description_2" src="@/assets/Stub.png">
    <img class="item__inventory__description_3" src="@/assets/Stub.png">
    <img class="item__inventory__description_4" src="@/assets/Stub.png">
    <img class="item__inventory__description_5" src="@/assets/Stub.png">
    <img class="item__inventory__description_6" src="@/assets/Stub.png">
    <img class="item__inventory__description_7" src="@/assets/Stub.png">
    </div>
     <button class="item__inventory__deleteBtn" v-on:click="deleteItem">Удалить предмет</button>
     </div>
    </div>
</template>

<script>
import props from '@/components/InvetoryItems.vue'
export default {
    name:'MenuDropdown',
    props:['itemImg'],
    components:
    props
}
</script>

<style>
.item {
}
.item__inventory_picture {
    width: 130px;
    height: 130px;
    margin-top: 32px;
    margin-bottom: 30px;

}
.item__inventory__deleteBtn {
    width: 220px;
    height: 39px;
    size: 14px; 
    border-radius: 8px;
    background-color:#FA7272;
    color: white;
    margin-top: 6px;
    margin-bottom: 18px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 16.71px;
}
.item__inventory__deleteBtn:hover {
    background-color: #FF8888;
}
.item__inventory__description {
    border-top:1px solid #4D4D4D;
    border-bottom: 1px solid #4D4D4D;
    padding-bottom: 24px;
    padding-top: 24px;
}
</style>
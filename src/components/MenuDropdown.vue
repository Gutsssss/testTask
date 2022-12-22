<template>
    <div class="item">
        <img class="item__inventory_picture"
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
     <button class="item__inventory__deleteBtn" v-on:click="showDelete = !showDelete">Удалить предмет</button>
     </div>
     <div class="item__inventory__delete" v-show="showDelete">
     <input class="item__inventory__delete__input" type="number" placeholder="Введите количество"  v-model="deleteCounter"/>
     <button class="item__inventory__delete__false" v-on:click="showDelete = !showDelete">Отмена</button>
     <button class="item__inventory__delete__true" v-on:click = "resetInput" >Подтвердить</button>
    </div>
    </div>
    
</template>

<script>
export default {
    name:'MenuDropdown',
    props:['itemImgDrop'],
    data() {
        return {
            showDelete:false,
            deleteCounter:""
        }
    },
    methods: {
        resetInput() {
            this.deleteCounter = ""
        }
    }
    
}
</script>

<style>
.item {
    position: relative;
}
.item__inventory__delete {
    width: 252px;
    height: 133px;
    background-color:rgba(38, 38, 38, 0.6);
    position: absolute;
    bottom: 0;
    left: 0;
    backdrop-filter: blur(8px);
    border:1px solid #4D4D4D
}
.item__inventory__delete__input {
    width: 210px;
    height: 40px;
    border-radius: 4px;
    background-color: #262626;
    border: 1px solid #4d4d4d;
    font-size: 14px;
    font-weight: 500;
    color: white;
    margin-top: 20px;
}
.item__inventory__delete__false {
    width: 88px;
    height: 33px;
    border-radius: 8px;
    color: black;
    background-color: white;
    gap: 12px;
    cursor: pointer;
    margin-right: 5px;
    margin-top: 20px;
}
.item__inventory__delete__false:hover {
    background-color: azure;
}
.item__inventory__delete__true {
    width: 112px;
    height: 33px;
    border-radius: 8px;
    background-color:#FA7272 ;
    color: white;
    cursor: pointer;
    margin-left: 5px;
    margin-top: 20px;
    
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
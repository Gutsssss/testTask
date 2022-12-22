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
    <!-- <div v-for="(item,index) in items"
    :key="index"
    > -->
    <draggable
          v-for="(item, index) in getRowsAndColumns"
          :key="index"
          :group="'people' + index"
          :list="item"
          ghost-class="ghost"
          @start="drag=true"
          @end="drag=false"
          item-key="index"
        >
          <template #item="{ element }">
            <div class="iteminventory" v-on:click="visible = !visible">
                <div class="iteminventory_counter">{{ element[index].itemCounter }}</div>
                <img
                class="iteminventory_Img"
                :src="require(`@/${element[index].itemImg}`)"
                alt="123"
              />
                <!-- <img
                class="iteminventory_Img"
                :src="require(`@/${element[index].itemImg}`)"
                alt="123"
              />
              <div class="iteminventory_counter">{{ element.itemCounter }}</div>
                <img
                class="iteminventory_Img"
                :src="require(`@/${element[index].itemImg}`)"
                alt="123"
              /> -->
            </div>
          </template>
        </draggable>
        <!-- </div> -->
    </ul>
    <div class="main__down"><img class="main__down__description" src="@/assets/Skeleton.png"><img class="main__down__close" src="@/assets/Vector.png"> </div>
    </div>
    <div class="main__menu"
    v-show="visible"
     ><img @click="visible = !visible" class="main__menu__close" src="@/assets/Vector.png"
     ><MenuDropdown
     /></div>
</div>
</template>


<script>
// import InventoryItems from '@/components/InvetoryItems.vue'
import MenuDropdown from '@/components/MenuDropdown.vue'
import draggable from 'vuedraggable'
export default { 
    components: {
    // InventoryItems,
    MenuDropdown,
    draggable
},
computed : {
    generateColums() {
      const data = this.items.reduce(
        (c, p) => {
          if (c[c.length - 1].length === 5) {
            c.push([]);
          }
          c[c.length - 1].push(JSON.parse(JSON.stringify(p)));
          return c;
        },
        [[]]
      );
    //   console.log(data);
      return data;
    },
    getRowsAndColumns() {
      const rows = 5;
      const generateRows = new Array(rows).fill(null);
        //  const generateRows = new Array(rows).fill({}).map((element,inx)=>{
        //    return {
        //        itemCounter: inx || 0,
        //        itemImg: "assets/ItemImage.png",
        //  }
        //  })
      const data = generateRows.reduce((acc, value, index) => {
        acc = [...acc];
        acc[index] = [...this.generateColums];
        return acc;
      }, []);
    //   console.log(data);
      return data;
    },
},
    data() {
    return {
        items: [{itemCounter:4, itemImg:"assets/ItemImage.png"},
        {itemCounter:2,itemImg:"assets/ItemImage1.png"},
        {itemCounter:5,itemImg:"assets/ItemImage2.png"},
        {itemCounter:null,itemImg:'assets/Rectangle9.png'},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},
        {itemCounter:null,itemImg:"assets/Rectangle9.png"},],
        visible:false,
        drag:false,
    }
    
    
    
}}
</script>
<style>
.iteminventory_counter {
    position: absolute;
    color: rgba(77, 77, 77, 1);
    bottom: 0px;
    right: 0px;
    width: 16px;
    height: 16px;
    border:1px solid rgba(77, 77, 77, 1) ;
    border-radius: 6px 0 0 0 ;
}
.iteminventory {
    width: 103px;
    height: 100px;
    border: 1px solid #4D4D4D;
    position: relative;
    align-items: center;
    background-color:#262626 ;
    cursor: pointer;
}
.iteminventory:hover {
    background-color: #2F2F2F;
}
.iteminventory_Img {
    left: 27px;
    position: absolute;
    top: 27px;
    
   
}
.main {
    width: 849px;
    height: 660px;
    display: flex;
    background-color: black;
    padding: 0 5px;
    position: relative;
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
    width: 525px !important;
    height: 500px !important;
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
.main__menu {
    width: 250px;
    height: 500px;
    right: 36px;
    position: absolute;
    background-color:rgba(38, 38, 38, 0.5);
    margin-top: 32px;
    border: 1px solid #4D4D4D;
    backdrop-filter: blur(8px)
}
.main__menu__close {
    position: absolute;
    top: 14px;
    right: 14px;
    cursor: pointer;
}
</style>
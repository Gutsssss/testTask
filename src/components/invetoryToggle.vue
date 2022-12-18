<template>
<div class="main__right">
  <div class="main__right__toggleShow" v-show="!isVisble">
    <div class="main__right__toggleShow__img">{{ itemImg }}</div>
    <div class="main__right__toggleShow__description">
    <img class="main__left__description_1" src="@/assets/Stub.png">
    <img class="main__left__description_2" src="@/assets/Stub.png">
    <img class="main__left__description_3" src="@/assets/Stub.png">
    <img class="main__left__description_4" src="@/assets/Stub.png">
    <img class="main__left__description_5" src="@/assets/Stub.png">
    <img class="main__left__description_6" src="@/assets/Stub.png">
    </div>
    </div>
  </div>
</template>

<script>
export default {
   data() {
    return {
        isVisble:false
    }
   }
}
</script>
<style>
.main__right {
  width: 250px ;
  height: 500px;
}
</style>
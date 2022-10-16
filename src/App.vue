<script setup  >


import ImageGallery from './components/ImageGallery.vue'
import SideBar from './components/SideBar.vue'
import {ref} from "vue"



const isWithColor = ref(true)

const OnselectOp  =  (isColor) => 
{
  isWithColor.value = isColor

}
</script>



<template>
<v-app>

<!--Sidebar-->

<SideBar @select-option="OnselectOp" />



<VMain>

  <!--Content Cards-->
  <ImageGallery  :isWithColor="isWithColor"/>
</VMain>


</v-app>

</template>



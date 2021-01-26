<template>
  <teleoport to="body">
    <div 
    v-if="state.isActive"
    class=" fixed top-0 left-0 z-50 flex items-center justify-center w-full h-full bg-black bg-opacity-50 "
    @click="handlerModalToogle({state: false})"
    >
     <div class="fixed mx-10">
      <div class="flex flex-col overflow-hideen bg-white rounded-lg animate__animated animate__fadeInUp animate__faster">
       <div>
        <div class="flex flex-col px-12 py-10 bg-white">
         <component :is="state.component" />
        </div>
       </div>
      </div>
     </div>
    </div>
  </teleoport>
</template>

<script>
import { reactive } from 'vue';

const DEFAULT_WIDTH = 'W-3/4 lg:w-1/3'
export default {
 setup () {
  const state = reactive({
   isActive: false,
   component: {},
   props: {},
   width: DEFAULT_WIDTH
  })

  function handlerModalToogle({status}) {
   
  }

  return {
   state
  }
 }
};
</script>

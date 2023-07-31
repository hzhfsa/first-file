<template>
  <div class="about">
    <h1 v-show="Ispage">This is an about page</h1>
    <button @click="changeIspage">change</button>
  </div>
</template>

<script setup>
import bus from '@/utils/bus.js'
import { ref } from 'vue';

let Ispage = ref(true)
function changeIspage(){
  console.log('ccc');
  Ispage.value = !Ispage.value;
  console.log('Ispage:',Ispage.value);
}

bus.on('changestatus', () => {
  console.log('123');
  changeIspage()
})
</script>

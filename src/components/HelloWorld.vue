<template>
  hello
  <button @click="fn">dianw</button>
</template>

<script setup>
import bus from '@/utils/bus.js'
import { useRouter } from 'vue-router';

const router = useRouter()
function fn(){
  console.log('aaa');
  router.push('/about')
  bus.emit('changestatus')
}

</script>

<style>

</style>
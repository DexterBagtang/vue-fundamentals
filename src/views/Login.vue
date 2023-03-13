<script setup>
import { ref } from 'vue'
import {useRouter} from 'vue-router'

const router = useRouter();

const emailInput = ref('');
const login = function (){
  router.push('/');
}

</script>

<template>
  <div class="container w-1/3 p-3 bg-gray-600 rounded flex flex-col mx-auto mt-10">
    <div class="text-gray-100 text-xl">Login</div>
    <div class="grid gap-1 text-gray-800">
      <input class="border rounded p-1 mt-3" type="email" v-model="emailInput" placeholder="Email">
      <input class="border rounded p-1 mb-1" type="password" placeholder="Password">
      <button class="border rounded text-gray-200 p-1 bg-blue-600 w-5/6 mx-auto"
              @click="login"
      >Login</button>
    </div>
  </div>
</template>

<style scoped>
@tailwind base;
@tailwind components;
@tailwind utilities;
</style>
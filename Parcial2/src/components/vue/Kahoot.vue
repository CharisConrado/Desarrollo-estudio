<script setup>
import { ref } from 'vue';

const respuetas = ref([])

function loadData(){
    fetch('Objeto,json')
    .then(function(response){
        return response.json()
    })

    .then(function(data){
        console.log(data)
        respuetas.value = data;
    })
}

</script>

<template>
    <div class="flex justify-center bg-blue-700 w-[60vh] h-42 p-10 m-10 w-96 h-24  border border-2 rounded mx-auto">
           <h6 class=" text-white"><strong>UFPSO</strong></h6>
    </div>
   
    <div  class="grid grid-cols-2 gap-2 w-full max-w-4xl justify-center mt-5 w-[60vh] h-42 p-1 m-10 h-24 mx-auto">
        <button  class=" cursor-pointer bg-red-400 h-10 flex items-center justify-center text-white"> </button>
        <button class=" cursor-pointer bg-blue-400 h-10 flex items-center justify-center text-white"></button>
        <button class=" cursor-pointer bg-yellow-400 h-10 flex items-center justify-center text-white"></button>
        <button class=" cursor-pointer bg-green-400 h-10 flex items-center justify-center text-white"></button>
    </div>

    <button class=" flex bg-green-300 text-white justify-center p-3 items-end rounded mx-auto">Siguiente</button>
    

</template>
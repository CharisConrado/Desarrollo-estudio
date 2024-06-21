<script setup>
import { ref } from "vue";

const carpetas = ref([])
const carpetas2 = ref([])
let palabra = ref("Mostrar");

let props = defineProps({
        title: String,
        information: String
    })

    function loadData(){
    fetch('EsteEquipo.json')
    .then(function(response){
        return response.json()
       
    })

    .then(function(data){
        console.log(data)
        carpetas.value = data;
    })}

    function loadData2(){
    fetch('EsteEquipo.json')
    .then(function(response2){
        return response2.json()
       
    })

    .then(function(data2){
        console.log(data2)
        carpetas2.value = data2;
    })}

    

    let mostrar = ref(false);
    function ocultar(){
        
        if(mostrar.value == false){
            mostrar.value = true;
            palabra.value = "Ocultar";
        }
        else{
            mostrar.value = false;
            palabra.value = "Mostrar";
        }}

    
    
</script>

<template>

    <div class="m-4 bg-zinc-300 p-4 w-auto inline-block">
        <button @click="loadData" class=" bg-white" >Este Esquipo</button>
        <div v-for="carpeta in carpetas":key="carpeta.name" class=" bg-slate-300 mb-1">
            <button @click="loadData2">{{ carpeta.name }}</button>
            <div   v-if="carpetas2[0].name" v-for="carpeta2, in carpetas2[0]":key="carpeta2.name" >{{ carpetas2[0].carpeta1 }}</div>
            
        </div>
        
    </div>

    <div class="bg-zinc-300 grid mx-auto text-center justify-center">
        <div class="w-60 bg-black text-white p-6">
            <div class="flex justify-between border-b-2 border-white bg-slate-800 py-3 px-2 align-center">
                <h1>{{ title }}</h1>
            <button class="bg-white h-10 rounded text-black"
                @click="ocultar">
                {{ palabra }}
            </button>
            </div>
            <p v-show="mostrar" class="bg-slate-800">
               {{ information }}
            </p>
        </div>    
            
    </div>

    
    
    
</template>
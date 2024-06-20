<script setup>
import { ref } from 'vue';

const data2 = ref(await fetch('https://thesimpsonsquoteapi.glitch.me/quotes?count=10')
.then(function (response){
    return response.json()
} ));
    console.log(data2);
    const left = "Left";
    const right = "Right";

</script>

<template>

<div class="flex items-center justify-around bg-white w-[60vh] h-42 p-10 m-10 border border-yellow-400 border-8 rounded mx-auto">
    
    <div :class="{'hidden': data2[0].characterDirection  === right}"
    class=" flex-shrink-0 w-28 h-28 bg-slate-500 bg-top bg-cover rounded-full m-4"
    :style="{backgroundImage:`url(${data2[0].image})`}"></div>

    <div class="grid max-w-[50%]">
        <h5><strong>{{ data2[0].character }}</strong></h5>
        <p class="text-sm"><strong>Character:</strong> {{ data2[0].character }}</p>
        <p class="text-sm"><strong>Quote:</strong> {{ data2[0].quote }}</p>
    </div>

    <div :class="{'hidden': data2[0].characterDirection  === left}"
    class=" flex-shrink-0 w-28 h-28 bg-slate-500 bg-top bg-cover rounded-full m-4"
    :style="{backgroundImage:`url(${data2[0].image})`}"></div>
</div>

<div class=" m-4 flex items-center justify-around bg-white w-[60vh] h-42 p-10 m-10 border border-yellow-400 border-8 rounded mx-auto">
    
    <div :class="{'hidden': data2[1].characterDirection  === right}"
    class=" flex-shrink-0 w-28 h-28 bg-slate-500 bg-top bg-cover rounded-full m-4"
    :style="{backgroundImage:`url(${data2[1].image})`}"></div>

    <div class="grid max-w-[50%]">
        <h5><strong>{{ data2[1].character }}</strong></h5>
        <p class="text-sm"><strong>Character:</strong> {{ data2[1].character }}</p>
        <p class="text-sm"><strong>Quote:</strong> {{ data2[1].quote }}</p>
    </div>

    <div :class="{'hidden': data2[1].characterDirection  === left}"
    class=" flex-shrink-0 w-28 h-28 bg-slate-500 bg-top bg-cover rounded-full m-4"
    :style="{backgroundImage:`url(${data2[1].image})`}"></div>
</div>

<div class="flex items-center justify-around bg-white w-[60vh] h-42 p-10 m-10 border border-yellow-400 border-8 rounded mx-auto">
    
    <div :class="{'hidden': data2[2].characterDirection  === right}"
    class=" flex-shrink-0 w-28 h-28 bg-slate-500 bg-top bg-cover rounded-full m-4"
    :style="{backgroundImage:`url(${data2[2].image})`}"></div>

    <div class="grid max-w-[50%]">
        <h5><strong>{{ data2[2].character }}</strong></h5>
        <p class="text-sm"><strong>Character:</strong> {{ data2[2].character }}</p>
        <p class="text-sm"><strong>Quote:</strong> {{ data2[2].quote }}</p>
    </div>

    <div :class="{'hidden': data2[2].characterDirection  === left}"
    class=" flex-shrink-0 w-28 h-28 bg-slate-500 bg-top bg-cover rounded-full m-4"
    :style="{backgroundImage:`url(${data2[2].image})`}"></div>
</div>

<div class="flex items-center justify-around bg-white w-[60vh] h-42 p-10 m-10 border border-yellow-400 border-8 rounded mx-auto">
    
    <div :class="{'hidden': data2[3].characterDirection  === right}"
    class=" flex-shrink-0 w-28 h-28 bg-slate-500 bg-top bg-cover rounded-full m-4"
    :style="{backgroundImage:`url(${data2[3].image})`}"></div>

    <div class="grid max-w-[50%]">
        <h5><strong>{{ data2[3].character }}</strong></h5>
        <p class="text-sm"><strong>Character:</strong> {{ data2[3].character }}</p>
        <p class="text-sm"><strong>Quote:</strong> {{ data2[3].quote }}</p>
    </div>

    <div :class="{'hidden': data2[3].characterDirection  === left}"
    class=" flex-shrink-0 w-28 h-28 bg-slate-500 bg-top bg-cover rounded-full m-4"
    :style="{backgroundImage:`url(${data2[3].image})`}"></div>
</div>

<div class="flex items-center justify-around bg-white w-[60vh] h-42 p-10 m-10 border border-yellow-400 border-8 rounded mx-auto">
    
    <div :class="{'hidden': data2[4].characterDirection  === right}"
    class=" flex-shrink-0 w-28 h-28 bg-slate-500 bg-top bg-cover rounded-full m-4"
    :style="{backgroundImage:`url(${data2[4].image})`}"></div>

    <div class="grid max-w-[50%]">
        <h5><strong>{{ data2[4].character }}</strong></h5>
        <p class="text-sm"><strong>Character:</strong> {{ data2[4].character }}</p>
        <p class="text-sm"><strong>Quote:</strong> {{ data2[4].quote }}</p>
    </div>

    <div :class="{'hidden': data2[4].characterDirection  === left}"
    class=" flex-shrink-0 w-28 h-28 bg-slate-500 bg-top bg-cover rounded-full m-4"
    :style="{backgroundImage:`url(${data2[4].image})`}"></div>
</div>



</template>
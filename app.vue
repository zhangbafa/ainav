<script setup>
import localDeployment from '@/data/localDeployment'
import webui from '@/data/webUI'
import frameworksTools from '@/data/frameworksTools'
import search from '@/data/search'
import speech from '@/data/speech'
import video from '@/data/video'
import image from '@/data/image'
import music from '@/data/music'
import digitalHuman from '@/data/digitalHuman'
import three from '@/data/three'

import computingPower from '@/data/computingPower'
import llmGlobal from '@/data/llmGlobal'
import llmChina from './data/llmChina'
useSeoMeta({
  title:'AI精选合集',
  description:'最实用、最热门的 AI 工具，帮助你在工作与学习上更轻松有效率'
})
</script>

<template>
  <div class="relative">
   
    <div class="text-center text-4xl font-bold m-12 mt-14">AI 精选合集</div>
    <div class="w-11/12 md:w-8/12 mx-auto mb-10 mt-16">
      <AiTool :tool="localDeployment" category="本地部署"/>
      <AiTool :tool="webui" category="webUI"/>
      <AiTool :tool="frameworksTools" category="框架/工具"/>
      <AiTool :tool="search" category="搜索"/>
      <AiTool :tool="speech" category="语音"/>
      <AiTool :tool="video" category="视频"/>
      <AiTool :tool="image" category="图像"/>
      <AiTool :tool="music" category="音乐"/>
      <AiTool :tool="digitalHuman" category="数字人"/>
      <AiTool :tool="three" category="3D"/>

      <AiTool :tool="computingPower" category="算力"/>
      <AiTool :tool="llmGlobal" category="LLM"/>
      <AiTool :tool="llmChina" category="国产大模型"/>
    </div>
    
    <!-- <div v-for="(obj, index) in llm" :key="index" class="w-11/12 md:w-8/12 mx-auto mb-10 mt-16">
      <div v-for="(value, key) in obj" :key="key" >
        <h1  class="mt-4 mb-6 font-bold text-gray-600">{{ key }}</h1>
        <div class="grid grid-cols-2 mg:grid-cols-2 lg:grid-cols-4 gap-6">
          <div v-for="(item, i) in value" :key="i" class="text-center">
          <div class="border rounded-md shadow-sm hover:bg-gray-50 transition duration-300">
            <a :href="item.url" target="_blank" class="block w-full h-full p-4">
              <img :src="'/downloads/' + item.image" :alt="item.name" style="width: 50px;min-height:50px;border-radius: 10px;margin:0 auto"/>
              <p class="mt-4 text-gray-500 dark:text-gray-500">{{ item.name }}</p>
            </a>
          </div>
         
        </div>
        </div>
        
      </div>
    </div> -->
  </div>
</template>

<template>
  <div :class="'w-full flex flex-col place-items-center space-y-12'" id="roadmapSection">
    <h1 :class="'text-white text-5xl font-bold italic'" data-aos="fade-in">
      Roadmap
    </h1>
    <div  :class="'timeline'">
      <div v-for="(roadMapItem,index) in roadMapItems" :key="roadMapItem.title">
        <div v-if="index % 2 ===1" :class="'container right'" data-aos="fade-up">
          <div :class="'content'">
            <h1 :class="'date'">{{ roadMapItem.date }}</h1>
            <h2 :class="'title'">{{ roadMapItem.title }}</h2>
            <p :class="'text'">
              {{ roadMapItem.content }}
            </p>
          </div>
        </div>
        <div v-if="index % 2 ===0" :class="'container left'" data-aos="fade-up">
          <div :class="'content'">
            <h1 :class="'date'">{{ roadMapItem.date }}</h1>
            <h2 :class="'title'">{{ roadMapItem.title }}</h2>
            <p :class="'text'">
              {{ roadMapItem.content }}
            </p>
          </div>
        </div>
      </div>
      
    </div>
  </div>
</template>

<script setup>
import constants from './constant/Constant';
const roadMapItems = constants.roadMapAdapter;
</script>
<template>
  <div :class="'w-full'" id='about' :style="{ backgroundImage: '../assets/images/desktop/background_about.svg', backgroundPosition: 'center', backgroundRepeat: 'no-repeat', backgroundSize: 'cover' }">
    <div :class="'w-full flex flex-col  place-items-center space-y-20 pt-20 pb-24 md:pt-16'" :style="{ backgroundImage: 'linear-gradient(180deg, rgba(6, 22, 31, .8), transparent)'}">
      <div :class="'flex flex-col place-items-center w-full h-auto'" data-aos="fade-down">
        <div :class="'w-[35rem] space-y-6 md:w-auto md:text-center md:space-y-6'">
          <h1 :class="'text-gray-200 text-6xl font-bold uppercase md:text-[3em] tracking-wide'">Fortune Towers</h1>
          <p :class="'text-white text-3xl md:text-[1.1rem]'">
            Fortune Towers is a play to earn casino metaverse with exciting new slot machine gaming experiences
          </p>
        </div>
      </div>
      <div v-for="aboutItem in aboutItems" :class="'flex flex-col w-[80%] h-auto bg-black bg-opacity-40 border border-y-2 border-[#007A7A] md:w-[70%] md:flex-row'">
        <div :class="'w-full ml-12 md:w-[40%] md:ml-0'" :style="{ mixBlendMode: 'lighten' }"  >
          <img :class="'object-cover'" :src='aboutItem.image' alt='casio_logo' />
        </div>
        <div :class="'flex flex-col justify-center w-full h-auto p-10 space-y-4 md:w-[60%] md:p-0 md:pr-8'">
          <h1 :class="'text-gray-200 text-3xl font-bold md:text-xl'">
            {{ aboutItem.title }}
          </h1>
          <p :class="'text-white text-2xl md:text-base'">
            {{ aboutItem.detail }}
          </p>
        </div>
      </div>
     
    </div>
  </div>
</template>

<script setup>
import constants from './constant/Constant';
const aboutItems = constants.aboutUs;
</script>
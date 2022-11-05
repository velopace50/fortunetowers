<template>
  <div :class="'flex flex-col space-y-20 w-full py-28'">
    <div :class="'flex flex-col place-items-center text-center space-y-10 md:space-y-3'" data-aos="fade-up">
      <h1 :class="'text-gray-200 w-[65%] text-[3em] font-bold uppercase'">
        2nd nft drop
      </h1>
      <p :class="'text-white text-2xl md:text-[0.9rem] w-fit'">
        Priority for the 2nd drop will be given to holders from 1st drop
      </p>
    </div>
    <div
      :class="'grid grid-cols-1 place-items-center h-full space-y-12 px-16 md:grid-cols-3 md:space-y-0 md:px-24'" 
      data-aos="fade-in"
    >
      <div v-for="secondNFTItem in secondNFTItems"  :class="'w-[90%] px-5 space-y-5 rounded-lg pb-12 bg-[#161731] shadow-md card-scale md:h-full'">
        <div :class="'w-full px-24 py-5'">
          <img :class="'w-full h-full object-contain'" :src='secondNFTItem.image' alt='lifetime_logo' />
        </div>
        <div :class="'flex flex-col place-items-center w-full h-[50%] space-y-7'">
          <h1 :class="'text-white text-4xl font-bold md:text-2xl'">{{ secondNFTItem.type }}</h1>
          <p :class="'text-white text-center text-2xl md:text-base'">
            {{ secondNFTItem.detail }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import constants from './constant/Constant';
const secondNFTItems = constants.secondNFTList;
</script>
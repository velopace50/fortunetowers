<template>
  <div 
    id='nfts' 
    :class="'flex flex-col space-y-20 w-full pt-28 pb-44'" 
    :style="{ backgroundImage: 'url(/_nuxt/assets/images/desktop/background_coming.png)', backgroundPosition: 'center', backgroundRepeat: 'no-repeat', backgroundSize: 'cover', mixBlendMode: 'lighten' }"
  >
    <div :class="'flex flex-col place-items-center text-center space-y-10 md:space-y-3'" data-aos="fade-in">
      <h1 :class="'w-[90%] text-gray-200 text-[3em] font-bold uppercase md:w-[65%]'">
        Will you get in early?
      </h1>
      <p :class="'text-white text-3xl md:text-[1.1rem] w-fit'">
        Our first drop of utility NFT's is coming soon
      </p>
    </div>
    <div :class="'grid grid-cols-1 place-items-center space-y-12 px-16 md:grid-cols-3 md:space-y-0 md:px-24'" data-aos="fade-up">
      <div
        v-for="nftItem in nftItems" 
        :class="'w-[90%] border border-y-2 border-[#007A7A] px-5 py-8 space-y-5 rounded-lg card-up md:h-full md:space-y-0'" 
        :style="{ backgroundImage: 'radial-gradient(farthest-side at 50% 3%, rgba(0, 178, 255, 0.47), rgba(0, 178, 255, 0.13), rgba(0, 0, 0, 0.10))', backdropFilter: 'blur(10px)' }"
        >
        <div :class="'w-full h-[9rem]'">
          <img :class="'w-full h-full object-contain'" :src='nftItem.image' alt='lifetime_logo' />
        </div>
        <div :class="'flex flex-col place-items-center w-full space-y-8 md:space-y-4 py-5'">
          <h3 :class="'text-white text-4xl font-bold md:text-xl'">{{ nftItem.type }}</h3>
          <h1 :class="'text-6xl font-extrabold rainbow-font w-fit -ml-6 md:text-4xl'">x {{ nftItem.count }}</h1>
          <p :class="'text-white text-center text-2xl md:text-base'">
            {{ nftItem.detail }}
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import constants from './constant/Constant';
const nftItems = constants.nftList;
</script>
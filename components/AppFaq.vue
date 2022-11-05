<template>
  <div :class="'relative grid grid-cols-1 pt-32 md:grid-cols-2'">
    <div :class="'flex flex-col z-10 space-y-4 px-16 md:px-0 md:pl-24'" id='faq'>
      <h1 :class="'text-white text-5xl font-bold tracking-widest'">FAQ</h1>
      <div :class="'w-full space-y-8 md:space-y-3 md:w-[95%]'">
        <div v-for="(faqItem,index) in accordion " :key="faqItem.title" :class="'w-full h-auto flex flex-col border-b border-gray-600'" data-aos="fade-right">
          <button :class="'relative w-full font-bold text-3xl text-left overflow-hidden text-white py-4 pr-20 bg-transparent md:text-[1.3em]'"
          @click="setActive(index)">
            <div :class="`absolute right-6 transform top-1/2 -translate-y-1/2 transition-all duration-500 ${faqItem.isOpen === true ? 'rotate-45' :'rotate-0'}`">
              <span :class="'text-4xl mt-[-0.3em] block md:text-2xl'">+</span>
            </div>
            {{ faqItem.title }}
          </button>
        
          <div :class="`${faqItem.isOpen===true ? 'max-h-96 overflow-hidden transitionall duration-700' : 'max-h-0 overflow-hidden transition-all duration-700' }`">
            <p :class="'text-white text-2xl pb-2 md:text-base'">
              {{ faqItem.detail }}
            </p>
          </div>
        </div>
      </div>
    </div>
    <div :class="'md:relative'">
      <img :class="'absolute top-0 opacity-30 md:opacity-100'" src='../assets/images/desktop/background_faq.jpg' alt='image'/>
    </div>
  </div>
</template>

<script setup>
import { onMounted } from 'vue';
import constants from './constant/Constant';
const faqItems = constants.FAQ;
const accordion = ref([]);
onMounted(()=>{
  faqItems.map(item=>{
    return accordion.value = [
      ...accordion.value,
      item
    ]
  });
});
function setActive(i){
  let newAccordion = [...accordion.value];
  newAccordion[i].isOpen = !newAccordion[i].isOpen;
}
</script>
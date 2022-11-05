<template>
  <div :class="`fixed w-full z-30 transition-all duration-700 ${ visible===false ? '-top-32' : 'top-0' }`">
    <nav :class="'flex relative md:justify-between place-items-center w-full h-auto px-16 bg-[#121328] border-b border-white overflow-hidden'">
      <div :class="'text-[2.5em] text-white px-5 py-8 block md:hidden'">
        <button @click="setSidebarOpen(!sidebarOpen)">
          <Icon name="uis:align-justify"></Icon>
        </button>
      </div>
      <div :class="'mobile:absolute mobile:top-0 mobile:left-1/2 mobile:transform mobile:-translate-x-1/2 w-[16em] md:relative md:w-[8.5rem]'">
        <img src='../assets/images/logo.svg' alt='logo_img' />
      </div>
      <div :class="`sidenav md:relative md:w-auto ${sidebarOpen===true ? 'w-1/2' : 'w-0' }`">
        <button :class="'closebtn text-white block md:hidden'" @click="setSidebarOpen(false)">
          &times;
        </button>
        <ul :class="'flex flex-col relative text-white text-md whitespace-nowrap overflow-x-hidden md:flex-row md:w-auto'">
          <li :class="'text-4xl w-auto px-12 py-5 cursor-pointer navbar-item md:text-lg md:p-auto'"><a href='#about'>About us</a></li>
          <li :class="'text-4xl w-auto px-12 py-5 cursor-pointer navbar-item md:text-lg md:p-auto'"><a href='#nfts'>NFTs</a></li>
          <li :class="'text-4xl w-auto px-12 py-5 cursor-pointer navbar-item md:text-lg md:p-auto'"><a href='#faq'>FAQ</a></li>
          <li :class="'text-4xl w-auto px-12 py-5 cursor-pointer navbar-item md:text-lg md:p-auto'"><a href='#roadmapSection'>Road map</a></li>
        </ul>
      </div>
      
    </nav>
  </div>
</template>

<script setup>
  import {onMounted,onBeforeMount} from 'vue'

  const visible = ref(false);
  const sidebarOpen = ref(false);
  function scrollHandler(){
    window.pageYOffset >100 ? visible.value = true : visible.value = false
  }
  function setSidebarOpen(val){
    sidebarOpen.value = val;
  }
  onMounted(()=>{
  window.addEventListener('scroll',scrollHandler);
  scrollHandler();
  })
  onBeforeMount(()=>{
  window.removeEventListener('scroll',scrollHandler);
  })
</script>
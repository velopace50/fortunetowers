<template>
  <div :class="'w-full h-[52em] flex flex-col justify-end place-items-center'" 
  :style="{ backgroundImage: 'url(_nuxt/assets/images/desktop/background_footer.jpg)', backgroundPosition: 'center', backgroundRepeat: 'no-repeat', backgroundSize: 'cover', mixBlendMode: 'lighten' }"
  >
    <div :class="'w-max h-fit flex flex-col place-items-center space-y-6 py-12'">
      <h1 
        :style="{ color: '#cf9bff', background: 'rgba(0,0,0,0.5)', padding: '0.2em 0.3em' }"
        :class="'text-white text-5xl font-bold aos-init aos-animate'">
          Follow us to find out when it will drop
      </h1>
      <div :class="'flex space-x-16'">
        <a href='https://discord.gg/hbQCkQj9' target="_blank" rel="noopener noreferrer">
          <span :class="'text-white text-6xl cursor-pointer'">
            <i :class="'fa-brands fa-discord'"></i>
          </span>
        </a>
        <a href='https://twitter.com/fortunetowersx' target="_blank" rel="noopener noreferrer">
          <span :class="'text-white text-6xl cursor-pointer'">
            <i :class="'fa-brands fa-twitter'"></i>
          </span>
        </a>
      </div>
      <p :class="'text-white text-xs'">
        @Fortune Towers. All rights reserved
      </p>
    </div>
  </div>
</template>
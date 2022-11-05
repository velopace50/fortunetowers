<template>
  <div :class="'grid gird-cols-1 pt-24 md:grid-cols-2'">
  
    <video id="bgVideo1" :class="'bgVideo'" autoPlay="true" loop="true" muted="true" playsinline="true" data-wf-ignore="true" data-object-fit="cover">
      <source src='../assets/videos/stock-footage-retrofuturistic-cityscape-seamless-background.webm' data-wf-ignore="true" />
    </video>
  
    <div :class="'hidden md:block'" data-aos="fade-in">
      <img src='../assets/images/desktop/building.png' alt='build_image' />
    </div>
    <div :class="'flex flex-col place-items-center space-y-10 pt-6 md:pr-20'">
      <div :class="'w-[85%] md:w-auto'" data-aos="fade-left">
        <h1 :class="'text-gray-200 text-[3.25em] font-bold uppercase'">Why Fortune towers?</h1>
        <p :class="'text-white text-2xl md:text-[0.9rem]'">
          We've been developing 3D slots and casino games for years. We know how to build them into a gaming metaverse better than anyone
        </p>
      </div>
  
      <div :class="'block md:hidden'" data-aos="fade-left">
        <img src='../assets/images/desktop/building.png' alt='build_image' />
      </div>
  
      <div :class="'flex flex-col w-[80%] space-y-6 md:w-full'">
        <div :class="'flex flex-col bg-[rgba(22,23,49,0.7)] place-items-center md:px-5 space-x-6 shadow-md md:flex-row'" data-aos="fade-up">
          <div :class="'w-full px-24 py-20 md:h-[9em] md:p-0 md:px-3 flex items-center md:w-[40%]'">
            <img :class="'object-contain w-full h-full'" src='../assets/images/desktop/item_1.png' alt='image'/>
          </div>
          <div :class="'flex flex-col w-full px-8 pb-16 space-y-8 md:space-y-3 md:p-0 md:py-7 md:w-[60%]'">
            <h1 :class="'text-gray-200 text-4xl font-bold md:text-xl'">
              Established slots engine
            </h1>
            <p :class="'text-white text-2xl md:text-base'">
              We have an advanced, well tested slots engine all written by our existing team
            </p>
          </div>
        </div>
  
        <div :class="'flex flex-col bg-[rgba(22,23,49,0.7)] place-items-center md:px-5 space-x-6 shadow-md md:flex-row'" data-aos="fade-up">
          <div :class="'w-full px-24 py-10 md:h-[9em] md:p-0 md:px-3 flex items-center md:w-[40%]'">
            <img :class="'object-contain w-full h-full'" src='../assets/images/desktop/item_3.png' alt='image'/>
          </div>
          <div :class="'flex flex-col w-full px-8 pb-16 space-y-8 md:space-y-3 md:p-0 md:py-7 md:w-[60%]'">
            <h1 :class="'text-gray-200 text-4xl font-bold md:text-xl'">
              Library of existing games
            </h1>
            <p :class="'text-white text-2xl md:text-base'">
              We have a broad library of high quality games that we're modifying to fit into the Fortune Towers metaverse
            </p>
          </div>
        </div>
  
        <div :class="'flex flex-col bg-[rgba(22,23,49,0.7)] place-items-center md:px-5 space-x-6 shadow-md md:flex-row'" data-aos="fade-up">
          <div :class="'w-full px-24 md:h-[9em] md:p-0 md:px-3 flex items-center md:w-[40%]'">
            <img :class="'object-contain w-full h-full'" src='../assets/images/desktop/item_2.png' alt='image'/>
          </div>
          <div :class="'flex flex-col w-full px-8 pb-16 space-y-8 md:space-y-3 md:p-0 md:py-7 md:w-[60%]'">
            <h1 :class="'text-gray-200 text-4xl font-bold md:text-xl'">
              Web based
            </h1>
            <p :class="'text-white text-2xl md:text-base'">
              Playable on any device! You can jump in and play on your phone on the bus
            </p>
          </div>
        </div>
  
      </div>
    </div>
  </div>
</template>
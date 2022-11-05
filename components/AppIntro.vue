<template>
    <div :class="'relative w-full h-[86.7em] md:h-[48.6em] overflow-hidden intro-background'" 
    :style="{
        backgroundPosition: 'center',
        backgroundRepeat: 'no-repeat',
        backgroundSize: 'cover',
        overflow: 'hidden',
        }">
        <!-- For Desktop -->
        <div :class="'hidden md:block'">
            <nav :class="'relative w-full h-auto py-5'">
                <div :class="'w-full flex justify-center space-x-[32em]'">
                    <ul :class="'flex flex-row w-auto relative text-white text-md space-x-24'">
                        <li :class="'text-lg w-auto p-auto cursor-pointer navbar-item'"><a href='#about'>About us</a></li>
                        <li :class="'text-lg w-auto p-auto cursor-pointer navbar-item'"><a href='#nfts'>NFTs</a></li>
                    </ul>
                    <ul :class="'flex flex-row w-auto relative text-white text-md space-x-24'">
                        <li :class="'text-lg w-auto p-auto cursor-pointerr navbar-item'"><a href='#faq'>FAQ</a></li>
                        <li :class="'text-lg w-auto p-auto cursor-pointer navbar-item'"><a href='#roadmapSection'>Road Map</a></li>
                    </ul>
                </div>
                <div :class="'absolute w-[13em] top-0 left-1/2 transform -translate-x-1/2'">
                    <img src='../assets/images/logo.svg' alt='logo_img' />
                </div>
            </nav>

            <div>
                <img :class="'w-full h-auto'" src='../assets/images/desktop/line_1.svg' alt='line_img' />
            </div>

            <div :class="'w-auto h-auto ml-48 mt-24 space-y-16'">
                <div :class="'space-y-6'" data-aos="fade-right">
                    <h1 :class="'text-5xl text-gray-200 font-bold uppercase'">
                        play to earn<br/>casino metaverse
                    </h1>
                    <p :class="'text-xl text-white'">
                        Own the metaverse!
                    </p>
                </div>
                <a href='#about'>
                    <button :class="'text-white text-xl uppercase mt-4 px-20 py-2 hover:px-24 button-scale-x'" data-aos="zoom-in" :style="{
                        backgroundImage: 'linear-gradient(90deg, #BD1296, #B809F5 10%, #09E1F5)'
                    }">
                        <p :class="'tracking-wider'">LEARN MORE</p>
                    </button>
                </a>
            </div>

            <div :class="'absolute bottom-[7%]'">
                <img :class="'w-full h-auto'" src='../assets/images/desktop/line_2.svg' alt='line_img' />
            </div>
        </div>

        <!-- For Mobile -->
        <div :class="'block md:hidden'">
            <nav :class="'relative w-full h-auto md:py-5'">
                <div :class="`sidenav ${sidebarOpen === true ? 'w-1/2' : 'w-0'}`">
                    <button
                        :class="'closebtn text-white'"
                        @click="sidebarOpen = false">
                        &times;
                    </button>
                    <ul :class="'relative text-white text-md whitespace-nowrap overflow-x-hidden'">
                        <li :class="'text-4xl w-auto px-12 py-5 cursor-pointer navbar-item'"><a href='#about'>About us</a></li>
                        <li :class="'text-4xl w-auto px-12 py-5 cursor-pointer navbar-item'"><a href='#roadmap'>Contacts</a></li>
                        <li :class="'text-4xl w-auto px-12 py-5 cursor-pointerr navbar-item'"><a href='#faq'>FAQ</a></li>
                        <li :class="'text-4xl w-auto px-12 py-5 cursor-pointer navbar-item'"><a href='#metaverse'>Metaverse</a></li>
                    </ul>
                </div>
                <div :class="'absolute w-[18em] top-0 left-1/2 transform -translate-x-1/2'">
                    <img src='../assets/images/logo.svg' alt='logo_img' />
                </div>
                <div :class="'text-[2.5em] text-white px-5 py-8'">
                    <button @click="sidebarOpen = !sidebarOpen">
                        <i :class="'fa-solid fa-bars'"></i>
                    </button>
                </div>
            </nav>

            <div>
                <img :class="'w-full h-auto'" src='../assets/images/desktop/line_1.svg' alt='line_img' />
            </div>

            <div :class="'w-auto flex flex-col place-items-center pt-[9rem] space-y-[24rem]'">
                <div :class="'space-y-6 w-[80%]'">
                    <h1 :class="'text-7xl text-gray-200 font-bold uppercase'">
                        play to earn casino metaverse
                    </h1>
                    <p :class="'text-3xl text-white'">
                        Own the metaverse
                    </p>
                </div>
                <button :class="'text-white text-4xl uppercase w-[80%] py-6 hover:px-24'" :style="{
                    backgroundImage: 'linear-gradient(90deg, #BD1296, #B809F5 10%, #09E1F5)'
                }">
                    <p :class="'tracking-wider'">play now &#62;</p>
                </button>
            </div>

            <div :class="'absolute bottom-[7%]'">
                <img :class="'w-full h-auto'" src='../assets/images/desktop/line_2.svg' alt='line_img' />
            </div>
        </div>
    </div>
</template>

<script setup>
    const sidebarOpen = useState('sidebarOpen', () => false)
</script>
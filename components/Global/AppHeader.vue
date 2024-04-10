<template>
    <nav class="bg-transparent :bg-gray-900 w-screen relative top-0 left-0 border-b border-gray-200 :border-gray-600">
        <div class="max-w-7xl mx-auto px-6 md:px-12 xl:px-6">
            <div class="flex flex-wrap items-center justify-between py-2 gap-6 md:py-4 md:gap-0 relative">
                <input aria-hidden="true" type="checkbox" name="toggle_nav" id="toggle_nav" class="hidden peer">
                <div class="relative z-20 w-full flex justify-between lg:w-max md:px-0">
                <NuxtLink to="/" class="flex items-center">
                    <img src="~/assets/Pictures/coess.png" class="h-8 mr-3" alt="CoESS Logo">
                    <span class="text-orange-800 self-center text-2xl font-semibold whitespace-nowrap :text-red-700 ">EASE</span>
                </NuxtLink>      
                    <div class="relative flex items-center lg:hidden max-h-10">
                        <label role="button" for="toggle_nav" aria-label="humburger" id="hamburger" class="relative  p-6 -mr-6">
                            <div aria-hidden="true" id="line" class="m-auto h-0.5 w-5 rounded bg-sky-900 :bg-gray-300 transition duration-300"></div>
                            <div aria-hidden="true" id="line2" class="m-auto mt-2 h-0.5 w-5 rounded bg-sky-900 :bg-gray-300 transition duration-300"></div>
                        </label>
                    </div>
                </div>
                <div aria-hidden="true" class="fixed z-10 inset-0 h-screen w-screen bg-white/70 backdrop-blur-2xl origin-bottom scale-y-0 transition duration-500 peer-checked:origin-top peer-checked:scale-y-100 lg:hidden :bg-gray-900/70"></div>
                <div class="flex-col z-20 flex-wrap gap-6 p-8 rounded-3xl border border-gray-100 bg-white shadow-2xl shadow-gray-600/10 justify-end w-full invisible opacity-0 translate-y-1  absolute top-full left-0 transition-all duration-300 scale-95 origin-top 
                            lg:relative lg:scale-100 lg:peer-checked:translate-y-0 lg:translate-y-0 lg:flex lg:flex-row lg:items-center lg:gap-0 lg:p-0 lg:bg-transparent lg:w-7/12 lg:visible lg:opacity-100 lg:border-none
                            peer-checked:scale-100 peer-checked:opacity-100 peer-checked:visible lg:shadow-none 
                            :shadow-none :bg-gray-800 :border-gray-700">      
                    <div class="text-gray-600 :text-gray-300 lg:pr-4 lg:w-auto w-full lg:pt-0">
                        <ul class="tracking-wide font-medium lg:text-sm flex-col flex lg:flex-row gap-6 lg:gap-0">
                            <li>
                                <NuxtLink to="/" class="block md:px-4 transition hover:text-orange-500">
                                    <span>Home</span>
                                </NuxtLink>
                            </li>
                            <li>
                                <NuxtLink to="/about-us" class="block md:px-4 transition hover:text-orange-500">
                                    <span>About Us</span>
                                </NuxtLink>
                            </li>
                            <li>
                                <NuxtLink to="/events" class="block md:px-4 transition hover:text-orange-500">
                                    <span>Events</span>
                                </NuxtLink>
                            </li>
                            <li>
                                <button @click="" class="block md:px-4 transition hover:text-orange-500">
                                    <a href="/merchandise">
                                    <span>Merchandise</span>
                                    </a>
                                </button>
                            </li>
                        </ul>
                    </div>

                    <div class="mt-12 lg:mt-0">
                    <a href="https://docs.google.com/forms/d/e/1FAIpQLSdHNzq46JOza3xWm3WCT4N5RYqUTmCXWPbL0pHBoboZE0qxYw/viewform?usp=sf_link" target="_blank" class="cursor-pointer booma rainbow-buttona focus:outline-none text-white bg-orange-500 hover:bg-orange-600 focus:ring-4 focus:ring-orange-300 font-medium rounded-lg text-sm px-5 py-2.5 mr-2 mb-2 :bg-orange-600  :hover:bg-orange-700 :focus:ring-orange-900">Be One of Us</a>
                    </div>
                    <!-- <div class="mt-4 lg:mt-0">
                    <NuxtLink href="https://coess-space.netlify.app" type="button" class="cursor-pointer booma rainbow-buttonb focus:outline-none text-white bg-orange-500 hover:bg-orange-600 focus:ring-4 focus:ring-orange-300 font-medium rounded-lg text-sm px-5 py-2.5 mr-2 mb-2 :bg-orange-600  :hover:bg-orange-700 :focus:ring-orange-900">Go to CoESS Space</NuxtLink>
                    </div> -->
                </div>
            </div>
        </div>
    </nav>
</template>

<style scoped>
#toggle_nav:checked ~ div #hamburger #line{
        @apply rotate-45 translate-y-1.5 
    }

#toggle_nav:checked ~ div #hamburger #line2{
        @apply -rotate-45 -translate-y-1
    }

.router-link-exact-active{
    color: #F7771D;
}

.rainbow-buttona {
  background-image: linear-gradient(90deg, #F75102 0%, #F7771D 49%, #F7A102 80%, #FEAD0F 100%);
}

.rainbow-buttonb {
  background-image: linear-gradient(90deg, #FEAD0F 0%, #F7A102 49%, #F7771D 80%, #F75102 100%);
}
.rainbow-buttona:hover {
  animation:slidebg 3s linear infinite;
}
.rainbow-buttonb:hover {
  animation:slidebg 3s linear infinite;
}
@keyframes slidebg {
  to {
    background-position:10vw;
  }
}
</style>

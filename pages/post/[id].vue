<template>
  <div id="PostPage"
    class="fixed lg:flex justify-between z-50 top-0 left-0 w-full h-full bg-black lg:overflow-hidden overflow-auto">
    <div class="lg:w-[calc(100%-540px)] h-full relative">
      <NuxtLink class="absolute z-20 m-5 rounded-full bg-gray-700 p-1.5 hover:bg-gray-800">
        <Icon name="material-symbols:close" color="#FFFFFF" size="27" />
      </NuxtLink>
      <div v-if="true">
        <button :disabled="!isLoaded" @click="loopThroughPostsUp()"
          class="absolute z-20 right-4 top-4 flex items-center justify-center rounded-full bg-gray-700 p-1.5 hover:bg-gray-800">
          <Icon name="mdi:chevron-up" size="30" color="#FFFFFF" />
        </button>

        <button :disabled="!isLoaded" @click="loopThroughPostsDown()"
          class="absolute z-20 right-4 top-20 flex items-center justify-center rounded-full bg-gray-700 p-1.5 hover:bg-gray-800">
          <Icon name="mdi:chevron-down" size="30" color="#FFFFFF" />
        </button>
      </div>
      <img class="absolute top-[18px] left-[70px] rounded-full lg:mx-0 mx-auto" width="45"
        src="~/assets/images/tiktok-logo-small.png">
      <video v-if="true" class="absolute object-cover w-full my-auto z-[-1] h-screen" src="/180386 (1080p).mp4" />
      <div v-if="!isLoaded" class="flex items-center justify-center bg-black bg-opacity-70 h-screen lg:min-w-[480px]">
        <Icon class="animate-spin ml-1" name="mingcute:loading-line" size="100" color="#FFFFFF" />
      </div>
      <div class="bg-black bg-opacity-70 lg:min-w-[480px]">
        <video ref="video" loop muted class="h-screen mx-auto" src="/180386 (1080p).mp4" />
      </div>
    </div>
    <div id="InfoSection" class="lg:max-w-[550px] relative w-full h-full bg-white">
      <div class="py-7" />

      <div class="flex items-center justfy-between px-8">
        <div class="flex items-center">
          <NuxtLink href="/">
            
          </NuxtLink>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>

</script>
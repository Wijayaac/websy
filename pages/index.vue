<template>
  <div>
    <header class="fixed top-0 left-0 w-full h-[60px] px-4">
      <div class="header-wrapper flex justify-between items-center h-full max-w-[760px] mx-auto">
        <div class="header-logo"></div>
        <div class="header-button">
          <UIButton @click="showModal = true" class="w-full p-2 rounded-full bg-gray-100 hover:bg-gray-300">
            <IconsDots />
          </UIButton>
        </div>
      </div>
    </header>
    <UIModal v-if="showModal" :showModal="showModal" title="Share this Profile" content="This is the content of my modal." @close="showModal = false" />
    <div class="container w-full max-w-[720px] mx-auto px-5 py-[65px]">
      <!-- profile -->
      <div class="profile text-center mb-5">
        <div class="flex flex-col">
          <div class="profile-image w-full h-full max-w-[110px] max-h-[110px] mx-auto rounded-full overflow-hidden mb-2">
            <div class="media pt-[100%]">
              <img src="/img/placeholder.png" alt="placeholder" />
            </div>
          </div>
          <div class="profile-text">
            <h1 class="font-bold text-xl">@namehere</h1>
          </div>
        </div>
      </div>
      <!-- content -->
      <div class="content">
        <!-- card -->
        <a href="#" class="card block p-2 bg-gray-100 rounded-lg my-4">
          <div class="card-wrapper grid gap-3 grid-cols-5 items-center justify-between">
            <div class="card-image w-full min-w-[30px] max-w-[75px] rounded-md overflow-hidden">
              <div class="media pt-[100%]">
                <img src="/img/placeholder.png" alt="placeholder" />
              </div>
            </div>
            <div class="card-text col-span-3 text-center">
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed nisi corrupti eius</p>
            </div>
          </div>
        </a>
        <a href="#" class="card block p-2 bg-gray-100 rounded-lg my-4">
          <div class="card-wrapper grid gap-3 grid-cols-5 items-center justify-between">
            <div class="card-image w-full min-w-[30px] max-w-[75px] rounded-md overflow-hidden">
              <div class="media pt-[100%]">
                <img src="/img/placeholder.png" alt="placeholder" />
              </div>
            </div>
            <div class="card-text col-span-3 text-center">
              <p>Lorem ipsum dolor.</p>
            </div>
          </div>
        </a>
        <a href="#" class="card block p-2 bg-gray-100 rounded-lg my-4">
          <div class="card-wrapper grid gap-3 grid-cols-5 items-center justify-between">
            <div class="card-image w-full min-w-[30px] max-w-[75px] rounded-md overflow-hidden">
              <div class="media pt-[100%]">
                <img src="/img/placeholder.png" alt="placeholder" />
              </div>
            </div>
            <div class="card-text col-span-3 text-center">
              <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
            </div>
          </div>
        </a>
        <a href="#" class="card block p-2 bg-gray-100 rounded-lg my-4">
          <div class="card-wrapper grid gap-3 grid-cols-5 items-center justify-between">
            <div class="card-image w-full min-w-[30px] max-w-[75px] rounded-md overflow-hidden">
              <div class="media pt-[100%]">
                <img src="/img/placeholder.png" alt="placeholder" />
              </div>
            </div>
            <div class="card-text col-span-3 text-center">
              <p>Lorem ipsum dolor sit.</p>
            </div>
          </div>
        </a>
        <a href="#" class="card block p-2 bg-gray-100 rounded-lg my-4">
          <div class="card-wrapper grid gap-3 grid-cols-5 items-center justify-between">
            <div class="card-image w-full min-w-[30px] max-w-[75px] rounded-md overflow-hidden">
              <div class="media pt-[100%]">
                <img src="/img/placeholder.png" alt="placeholder" />
              </div>
            </div>
            <div class="card-text col-span-3 text-center">
              <p>Lorem ipsum dolor sit amet consectetur.</p>
            </div>
          </div>
        </a>
      </div>
    </div>
  </div>
</template>

<script setup>
const showModal = ref(false);
</script>

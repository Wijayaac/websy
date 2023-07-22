<template>
  <Teleport to="body">
    <div v-if="showModal" class="modal">
      <div class="modal-overlay" @click="closeModal"></div>
      <div class="modal-content">
        <!-- modal header -->
        <div class="modal-header">
          <h2 class="font-bold text-md">{{ title }}</h2>
          <UIButton @click="closeModal" class="absolute top-0 right-0">
            <IconsClose />
          </UIButton>
        </div>
        <!-- Modal slot Content Wrapper -->
        <slot />
        <!-- slot end -->
        <div class="flex flex-col">
          <a href="#" class="flex items-center gap-4 py-3">
            <IconsFacebook class="w-7 h-7" />
            <p class="font-bold text-md">Share on Facebook</p>
          </a>
          <a href="#" class="flex items-center gap-4 py-3">
            <IconsFacebook class="w-7 h-7" />
            <p class="font-bold text-md">Share on Facebook</p>
          </a>
          <a href="#" class="flex items-center gap-4 py-3">
            <IconsFacebook class="w-7 h-7" />
            <p class="font-bold text-md">Share on Facebook</p>
          </a>
          <a href="#" class="flex items-center gap-4 py-3">
            <IconsFacebook class="w-7 h-7" />
            <p class="font-bold text-md">Share on Facebook</p>
          </a>
          <UIButton class="flex justify-between py-3 px-2 my-2 border-[1px] border-gray-100 rounded-md font-medium">
            <span class="inline-flex gap-2">
              <IconsFacebook class="w-6 h-6" />
              <p>Lorem.ipsum/test</p>
            </span>
            <span>Copy</span>
          </UIButton>
        </div>
      </div>
    </div>
  </Teleport>
</template>

<script setup>
defineProps({
  showModal: Boolean,
  title: String,
});

const emit = defineEmits();

const closeModal = () => {
  emit("close", true);
};
</script>

<style>
/* Add your modal styles here */
.modal {
  @apply absolute inset-0 z-20 h-screen w-screen flex items-end justify-center;
}

.modal-header {
  @apply relative flex justify-center mb-10;
}

.modal-content {
  @apply relative z-20 min-h-[300px] min-w-full bg-white px-5 py-6 rounded-3xl;
}

.modal-overlay {
  @apply content-[''] absolute inset-0 h-screen w-screen opacity-30 z-10 bg-gray-950;
}

@media screen and (min-width: 992px) {
  .modal {
    @apply items-center;
  }

  .modal-content {
    @apply min-w-[400px] rounded-md;
  }
}
</style>

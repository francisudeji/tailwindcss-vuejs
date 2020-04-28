<template>
  <div>
    <!-- modal layout -->
    <div
      v-if="isModalOpen"
      class="fixed top-0 left-0 flex items-center justify-center w-full h-screen bg-overlay"
    >
      <!-- Modal -->
      <div
        class="absolute w-4/5 px-6 py-10 bg-white rounded shadow-lg md:w-3/5 lg:w-2/5"
      >
        <div class="text-right">
          <button @click="toggleModal" class="text-4xl text-gray-600">
            &times;
          </button>
        </div>

        <h1 class="block text-3xl font-bold text-center text-gray-800">
          One more step!
        </h1>

        <p class="block mt-2 text-base font-light text-center text-gray-700">
          We sent a One Time Password (OTP) to abc.xyz@email.com.
        </p>

        <div class="flex px-16 mt-6">
          <input type="text" class="w-1/4 h-16 text-center border-2" />
          <input type="text" class="w-1/4 h-16 text-center border-2" />
          <input type="text" class="w-1/4 h-16 text-center border-2" />
          <input type="text" class="w-1/4 h-16 text-center border-2" />
        </div>

        <div class="px-6 mt-6">
          <button
            class="block w-full px-6 py-3 text-white uppercase bg-blue-500 rounded-lg shadow-lg focus:bg-blue-600 hover:bg-blue-600"
          >
            Continue
          </button>
        </div>
      </div>
    </div>

    <!-- content -->
    <div class="flex items-center justify-center w-full h-screen">
      <button
        @click="toggleModal"
        class="px-6 py-2 text-white bg-blue-500 rounded-lg shadow-lg focus:bg-blue-600 hover:bg-blue-600"
      >
        Open Modal
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      isModalOpen: false,
    };
  },
  methods: {
    toggleModal() {
      this.isModalOpen = !this.isModalOpen;
    },
  },
};
</script>

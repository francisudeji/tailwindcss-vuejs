<template>
  <div>
    <!-- modal layout -->
    <div
      v-if="isModalOpen"
      class="bg-overlay fixed top-0 left-0 h-screen w-full flex items-center justify-center"
    >
      <!-- Modal -->
      <div class="w-2/5 bg-white rounded py-10 px-6 shadow-lg absolute">
        <div class="text-right">
          <button @click="toggleModal" class="text-4xl text-gray-600">
            &times;
          </button>
        </div>

        <h1 class="text-3xl text-gray-800 font-bold block text-center">
          One more step!
        </h1>

        <p class="mt-2 text-base text-gray-700 font-light block text-center">
          We sent a One Time Password (OTP) to abc.xyz@email.com.
        </p>

        <div class="flex px-16 mt-6">
          <input type="text" class="text-center h-16 w-1/4 border-2" />
          <input type="text" class="text-center h-16 w-1/4 border-2" />
          <input type="text" class="text-center h-16 w-1/4 border-2" />
          <input type="text" class="text-center h-16 w-1/4 border-2" />
        </div>

        <div class="mt-6 px-6">
          <button
            class="w-full block uppercase bg-blue-500 text-white py-3 px-6 rounded-lg shadow-lg focus:bg-blue-600 hover:bg-blue-600"
          >
            Continue
          </button>
        </div>
      </div>
    </div>

    <div class="h-screen w-full flex items-center justify-center">
      <button
        @click="toggleModal"
        class="bg-blue-500 text-white rounded-lg shadow-lg py-2 px-6 focus:bg-blue-600 hover:bg-blue-600"
      >
        Open Modal
      </button>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      isModalOpen: false
    };
  },
  methods: {
    toggleModal() {
      if (this.isModalOpen) {
        this.isModalOpen = false;
        return;
      }

      this.isModalOpen = true;
    }
  }
};
</script>

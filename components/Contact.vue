<template>
  <div class="py-10" id="contact">
    <div>
      <p class="text-xl font-semibold sm:text-2xl text-center font-Poppins mb-[20px] text-green-600" data-aos="fade-up">Contact me</p>
      <div class="px-[24px] mx-[16px] sm:mx-[120px] md:mx-[200px] lg:mx-[350px] py-[24px] bg-neutral-800 rounded-[15px]" data-aos="fade-up">
        <form @submit.prevent="handleSubmit">
          <div data-aos="fade-up">
            <div class="flex flex-col">
              <label class="text-white mb-2 text-base font-Poppins font-semibold">Nama :</label>
              <input class="py-[10px] px-[20px] rounded-lg bg-neutral-800 border focus:bg-white" type="text" v-model="form.name" placeholder="Nama" required />
            </div>
            <div class="flex flex-col mt-[24px]">
              <label class="text-white mb-2 text-base font-Poppins font-semibold">Email :</label>
              <input class="py-[10px] px-[20px] rounded-lg bg-neutral-800 border focus:bg-white" type="email" v-model="form.email" placeholder="example@gmail.com" required />
            </div>
            <div class="flex flex-col mt-[24px]">
              <label class="text-white mb-2 text-base font-Poppins font-semibold">Message :</label>
              <textarea class="py-[10px] px-[20px] rounded-lg bg-neutral-800 border focus:bg-white" v-model="form.message" placeholder="message" required></textarea>
            </div>
            <button class="text-white mt-[24px] hover:scale-95 bg-green-500 hover:bg-green-600 rounded-lg py-[10px] px-[20px] font-Poppins font-semibold" type="submit">Send</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue';
import Aos from 'aos';
import 'aos/dist/aos.css';

const form = ref({
  name: '',
  email: '',
  message: '',
});

onMounted(() => {
  Aos.init();
});

const handleSubmit = () => {
  console.log('form submitted', form.value);
  // Reset form
  form.value = {
    name: '',
    email: '',
    message: '',
  };
};
</script>

<style scoped></style>

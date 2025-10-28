<script setup>
const email = ref("");
const password = ref("");

const submit = () => {
  console.log(email.value, password.value);
};
</script>

<template>
  <div class="flex bg-[#09090B] h-screen">
    <!-- Sidebar -->
    <div
      class="bg-[#18181B] w-[516px] px-15 flex flex-col justify-center font-[Inter]"
    >
      <Logo />
      <h1 class="text-white font-bold text-lg mt-11">
        Sign up for a free account
      </h1>
      <p class="text-sm mt-2.5 text-zinc-300">
        Already registered?
        <span class="font-bold text-[#FFAC00] underline">Log in</span> to your
        account
      </p>

      <form @submit.prevent="submit()">
        <div class="mt-8">
          <label for="" class="text-zinc-300 text-sm block mb-0.5"
            >Email Address</label
          >
          <input
            v-model="email"
            placeholder="you@example.com"
            type="email"
            class="block w-full bg-[#27272A] border border-[#3F3F46] rounded text-white px-4 py-2 placeholder:text-zinc-500 text-sm focus:outline-0"
            required
          />
        </div>

        <div class="mt-6">
          <label for="" class="text-zinc-300 text-sm block mb-0.5"
            >Password</label
          >
          <input
            v-model="password"
            placeholder="****************"
            type="password"
            class="block w-full bg-[#27272A] border border-[#3F3F46] rounded text-white px-4 py-2 placeholder:text-zinc-500 text-sm focus:outline-0"
            required
          />
        </div>
        <div>
          <button
            class="w-full mt-8 bg-[#FFAC00] rounded-full px-4 py-3 text-sm font-bold flex justify-center items-center space-x-2"
          >
            <span>Sign Up</span>
            <img src="/arrow.svg" alt="" />
          </button>
        </div>
      </form>
    </div>
    <!-- /Sidebar -->

    <!-- Note introduction -->
    <div class=""></div>
    <!-- /Note introduction -->
  </div>
</template>

<style lang="scss" scoped></style>

<template>
  <div class="min-h-screen flex flex-col items-center justify-center text-center p-4">
    <h1 class="text-3xl font-bold">About My Portfolio</h1>
    <p class="mt-4 max-w-prose">
      Hello! I am a third-year computer science student with a passion for web development. This
      portfolio showcases various projects I have worked on, highlighting my skills in Python, C++,
      and web technologies such as Vue.js and Tailwind CSS. Here you will find detailed descriptions
      of my projects, the challenges I faced, and the solutions I implemented.
    </p>
    <router-link to="/" class="mt-6">
      <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
        Go Back Home
      </button>
    </router-link>
  </div>
</template>

<script>
export default {
  name: 'AboutView'
}
</script>

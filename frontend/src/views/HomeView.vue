<template>
  <div class="min-h-screen flex flex-col items-center justify-center text-center p-4">
    <h1 class="text-4xl font-bold">Welcome to Task-Ticker</h1>
    <p class="mt-4 text-lg">
      Task-Ticker is a powerful and flexible tool for managing your tasks, notes, and projects. Stay
      organized and efficient with our easy-to-use interface.
    </p>
    <div class="mt-6 flex space-x-4">
      <router-link to="/about">
        <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold py-2 px-4 rounded">
          About
        </button>
      </router-link>
      <router-link to="/editor">
        <button class="bg-green-500 hover:bg-green-700 text-white font-bold py-2 px-4 rounded">
          Go to Editor
        </button>
      </router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeView'
}
</script>

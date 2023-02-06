<template>
    <header class="fixed w-full bg-indigo-800 shadow-md">
      <div class="container mx-auto flex items-center p-3">
        <NuxtLink class="logo text-2xl font-bold text-white ">Jober</NuxtLink>
        <nav class="ml-auto">
          <NuxtLink class="px-4 py-2 text-white hover:bg-indigo-400 " >Jobs</NuxtLink>
          <NuxtLink class="px-4 py-2 text-white hover:bg-indigo-400 ">Companies</NuxtLink>
          <NuxtLink class="px-4 py-2 text-white hover:bg-indigo-400 ">Services</NuxtLink>
          <NuxtLink class="px-4 py-2 text-white hover:bg-indigo-400 "> Signup</NuxtLink>
        </nav>
      </div>
    </header>
    <footer>

    </footer>
    <div>
      <slot/>
    </div>
  </template>
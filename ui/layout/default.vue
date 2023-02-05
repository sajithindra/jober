<template>
    <header class="fixed w-full bg-white shadow-md">
      <div class="container mx-auto flex items-center p-6">
        <NuxtLink class="logo text-lg font-bold">App Name</NuxtLink>
        <nav class="ml-auto">
          <NuxtLink class="px-4 py-2 text-gray-800 hover:bg-gray-200">Home</NuxtLink>
          <NuxtLink class="px-4 py-2 text-gray-800 hover:bg-gray-200">Features</NuxtLink>
        </nav>
      </div>
    </header>
    <div>
      <nuxt/>
    </div>
  </template>
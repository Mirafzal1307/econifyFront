<template>
  <div
    class="flex min-h-screen bg-neutral-1 dark:bg-neutral-9 text-neutral-9 dark:text-neutral-300"
  >
    <!-- Sidebar -->
    <aside class="w-64 bg-neutral-2 dark:bg-neutral-800 p-4 shadow-md">
      <h2 class="text-lg font-semibold mb-4">Admin Panel</h2>
      <nav class="flex flex-col gap-2">
        <NuxtLink
          to="/admin/dashboard"
          class="text-sm py-2 px-3 rounded-lg hover:bg-neutral-3 dark:hover:bg-neutral-700"
        >
          Dashboard
        </NuxtLink>
        <NuxtLink
          to="/admin/users"
          class="text-sm py-2 px-3 rounded-lg hover:bg-neutral-3 dark:hover:bg-neutral-700"
        >
          Users
        </NuxtLink>
        <NuxtLink
          to="/admin/settings"
          class="text-sm py-2 px-3 rounded-lg hover:bg-neutral-3 dark:hover:bg-neutral-700"
        >
          Settings
        </NuxtLink>
      </nav>
    </aside>

    <!-- Main Content -->
    <div class="flex-1 p-8">
      <!-- Header -->
      <header
        class="flex items-center justify-between pb-4 border-b border-neutral-3 dark:border-neutral-700"
      >
        <h1 class="text-2xl font-bold">Welcome to Admin Panel</h1>
        <!-- <button @click="toggleDarkMode" class="text-sm px-4 py-2 bg-emerald-600 text-white rounded-lg hover:bg-emerald-700">
                    Toggle Dark Mode
                </button> -->
      </header>

      <!-- Slot for Content -->
      <main class="mt-8">
        <slot />
      </main>
    </div>
  </div>
</template>

<script setup>
definePageMeta({
  layout: "admin", // Use the admin layout for this page
});
</script>

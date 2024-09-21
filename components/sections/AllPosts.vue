<template>
    <section py-20>
        <div px="5 sm:10 md:12 lg:5" class="max-w-7xl mx-auto flex flex-col items-start gap-10 xl-gap-14">
            <div class="text-center max-w-3xl mx-auto space-y-4">
                <h1 text="4xl neutral-9 dark:white" class="font-semibold">
                    All blog posts
                </h1>
            </div>
            <div class="grid gap-6 sm:grid-cols-2 lg:grid-cols-3">
                <div v-for="index in 6" :key="index"
                    class="p-6 bg-neutral-1 dark:bg-neutral-9 rounded-3xl border border-neutral-2 dark:border-neutral-8 shadow-lg relative overflow-hidden md:flex md:flex-col  ">
                    <!-- Image Section -->
                    <img src="https://img.freepik.com/premium-photo/beautiful-woman-is-seen-holding-camera-while-strolling-sea_969100-393.jpg"
                        alt="UX review presentations" class="w-full md:w-full lg:w-full h-64 md:h-full lg:h-58 object-cover rounded-lg">
                    <div class="flex flex-col md:justify-between">
                        <div>
                            <!-- Date Section -->
                            <div class="text-sm mt-4 text-blue-500 dark:text-blue-400 ">
                                Sunday, 1 Jan 2023
                            </div>

                            <!-- Title Section -->
                            <h2 class="text-2xl font-semibold text-neutral-9 dark:text-white mt-2">
                                UX review presentations
                                <a href="#" class="inline-block align-middle ml-2">
                                    <span class="i-carbon-external-link flex text-lg"></span>
                                </a>
                            </h2>

                            <!-- Description Section -->
                            <p class="text-neutral-7 dark:text-neutral-3 mt-2">
                                How do you create compelling presentations that wow your colleagues and impress your
                                managers?
                            </p>

                        </div>

                        <!-- Tags Section -->
                        <div class="mt-4 flex space-x-2 ">
                            <span
                                class="px-3 py-1 text-sm rounded-full bg-purple-100 text-purple-700 dark:bg-purple-900 dark:text-purple-300">
                                Design
                            </span>
                            <span
                                class="px-3 py-1 text-sm rounded-full bg-blue-100 text-blue-700 dark:bg-blue-900 dark:text-blue-300">
                                Research
                            </span>

                        </div>
                    </div>

                </div>
            </div>
        </div>
    </section>
</template>
<template>
    <section class="py-20">
        <div class="px-5 sm:px-10 md:px-12 lg:px-5 max-w-7xl mx-auto space-y-10">
            <!-- Go Back Button -->
            <nuxt-link to="/"
                class="inline-flex items-center px-6 py-3 bg-emerald-500 dark:bg-emerald-700 text-white dark:text-white font-semibold rounded-lg shadow-md hover:bg-emerald-600 dark:hover:bg-emerald-800 focus:outline-none focus:ring-2 focus:ring-emerald-300 dark:focus:ring-emerald-900 transition-all ease-in-out duration-300 mt-10">
                <span class="i-carbon-arrow-left mr-2 "></span> <!-- Icon for 'back' -->
                Back to Home
            </nuxt-link>

            <!-- Profile Card -->
            <div
                class="relative h-100 w-full bg-neutral-1 dark:bg-neutral-900 rounded-lg  shadow-lg overflow-hidden my-10">
                <img src="https://images.unsplash.com/photo-1472214103451-9374bd1c798e?fm=jpg&q=60&w=3000&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxleHBsb3JlLWZlZWR8N3x8fGVufDB8fHx8fA%3D%3D"
                    alt="John Doe" class="w-full h-72 object-cover">
                <div class="absolute inset-x-0 bottom-0 p-4 bg-neutral-1/70 dark:bg-neutral-900/70">
                    <h1 class="text-5xl font-extrabold text-neutral-9 dark:text-white">John Doe</h1>
                </div>
            </div>

            <!-- About Me Section -->
            <div class="bg-neutral-1 dark:bg-neutral-900 p-6 rounded-lg shadow-md">
                <h2 class="text-3xl font-semibold text-neutral-9 dark:text-white mb-4">About Me</h2>
                <p class="text-neutral-7 dark:text-neutral-3">
                    As a passionate and experienced UI designer, I am dedicated to creating intuitive and engaging user
                    experiences that meet the needs of my clients and their users. I have a strong understanding of
                    design
                    principles and a proficiency in design tools, and I am comfortable working with cross-functional
                    teams to bring
                    projects to fruition.
                </p>
            </div>

            <!-- Grid with Skills and Experience/Education -->
            <div class="grid gap-6 lg:grid-cols-3">

                <!-- Skills Section -->
                <div class="lg:col-span-3 space-y-6">
                    <div class="bg-neutral-1 dark:bg-neutral-900 p-6 rounded-lg shadow-md">
                        <h2 class="text-3xl font-semibold text-neutral-9 dark:text-white mb-4">Skills</h2>
                        <ul class="list-disc pl-6 space-y-2 text-neutral-7 dark:text-neutral-3">
                            <li>Extensive experience in UI design</li>
                            <li>Proficiency in Adobe Creative Suite and Sketch</li>
                            <li>Strong understanding of layout, color theory, and typography</li>
                            <li>Ability to create wireframes and prototypes</li>
                            <li>Experience conducting user research</li>
                        </ul>
                    </div>

                    <div class="bg-neutral-1 dark:bg-neutral-900 p-6 rounded-lg shadow-md">
                        <h2 class="text-3xl font-semibold text-neutral-9 dark:text-white mb-4">Skills</h2>
                        <ul class="list-disc pl-6 space-y-2 text-neutral-7 dark:text-neutral-3">
                            <li>Extensive experience in UI design</li>
                            <li>Proficiency in Adobe Creative Suite and Sketch</li>
                            <li>Strong understanding of layout, color theory, and typography</li>
                            <li>Ability to create wireframes and prototypes</li>
                            <li>Experience conducting user research</li>
                        </ul>
                    </div>
                </div>





                <!-- Experience Section -->
                <div class="lg:col-span-3 space-y-6">
                    <div class="bg-neutral-1 dark:bg-neutral-900 p-6 rounded-lg shadow-md">
                        <h2 class="text-3xl font-semibold text-neutral-9 dark:text-white mb-4">Experience</h2>
                        <ul class="list-disc pl-6 space-y-2 text-neutral-7 dark:text-neutral-3">
                            <li>5 years as a UI designer</li>
                            <li>Led e-commerce redesign project, increasing sales by 25%</li>
                            <li>Created wireframes for a mobile banking app dcsc cs</li>
                        </ul>
                    </div>

                    <!-- Education Section -->
                    <div class="bg-neutral-1 dark:bg-neutral-900 p-6 rounded-lg shadow-md">
                        <h2 class="text-3xl font-semibold text-neutral-9 dark:text-white mb-4">Education</h2>
                        <ul class="list-disc pl-6 space-y-2 text-neutral-7 dark:text-neutral-3">
                            <li>Bachelor's Degree in Graphic Design</li>
                            <li>Certified User Experience Designer (CUED)</li>
                            <li>Certified User Experience Designer (CUED)</li>
                            <li>Certified User Experience Designer (CUED)</li>

                        </ul>
                    </div>
                </div>

            </div>
        </div>
    </section>
</template>

<script lang="ts" setup>
import { useRoute } from 'vue-router'

// Access the dynamic route parameter
const route = useRoute()
const id = route.params.id
</script>
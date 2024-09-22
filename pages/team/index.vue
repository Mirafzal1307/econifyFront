<template>
    <section class="py-20 mt-5">
        <div class="px-5 sm:px-10 md:px-12 lg:px-5 max-w-7xl mx-auto">
            <!-- Section Header -->
            <div class="text-center max-w-3xl mx-auto mb-10">
                <h1 class="text-4xl font-semibold text-neutral-900 dark:text-white mb-4">
                    Meet Our Team
                </h1>
                <p class="text-neutral-700 dark:text-neutral-300">
                    The talented people behind our success
                </p>
            </div>

            <!-- Team Members Grid -->
            <div class="grid gap-10 sm:grid-cols-2 lg:grid-cols-3">
                <div v-for="(member, index) in teamMembers" :key="index"
                    class="p-6 bg-neutral-100 dark:bg-neutral-800 rounded-xl border border-neutral-200 dark:border-neutral-700 shadow-lg">

                    <!-- Team Member Image (Now Circular) -->
                    <img :src="member.image" alt="Team Member" class="w-40 h-40 object-cover rounded-full mx-auto mb-4">

                    <!-- Team Member Details -->
                    <div class="text-center">
                        <h2 class="text-2xl font-semibold text-neutral-900 dark:text-white">
                            {{ member.name }}
                        </h2>
                        <p class="text-emerald-600 dark:text-emerald-400 mt-1">
                            {{ member.role }}
                        </p>
                        <p class="text-neutral-600 dark:text-neutral-400 mt-2">
                            {{ member.bio }}
                        </p>
                    </div>

                    <!-- Social Links (Optional) -->
                    <div class="mt-4 flex justify-center space-x-4">
                        <a v-for="link in member.social" :key="link.platform" :href="link.url" target="_blank"
                            rel="noopener noreferrer">
                            <span
                                :class="`i-carbon-logo-${link.platform} text-neutral-600 dark:text-neutral-300 hover:text-emerald-600 dark:hover:text-emerald-400 text-2xl`"></span>
                        </a>
                    </div>

                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
const teamMembers = [
    {
        name: 'John Doe',
        role: 'UI/UX Designer',
        bio: 'John is a passionate designer with 5 years of experience in creating visually appealing user interfaces.',
        image: 'https://via.placeholder.com/300',
        social: [
            { platform: 'linkedin', url: 'https://linkedin.com' },
            { platform: 'github', url: 'https://github.com' }
        ]
    },
    {
        name: 'Jane Smith',
        role: 'Frontend Developer',
        bio: 'Jane is an expert in Vue.js and loves bringing designs to life with clean and efficient code.',
        image: 'https://via.placeholder.com/300',
        social: [
            { platform: 'linkedin', url: 'https://linkedin.com' },
            { platform: 'github', url: 'https://github.com' }
        ]
    },
    {
        name: 'Mike Johnson',
        role: 'Backend Developer',
        bio: 'Mike specializes in server-side development and has a knack for building scalable backend systems.',
        image: 'https://via.placeholder.com/300',
        social: [
            { platform: 'linkedin', url: 'https://linkedin.com' },
            { platform: 'github', url: 'https://github.com' }
        ]
    }
]
</script>

<style scoped>
/* Ensure responsiveness with grid settings */
@media (min-width: 768px) {
    .grid {
        grid-template-columns: repeat(2, 1fr);
    }
}

@media (min-width: 1024px) {
    .grid {
        grid-template-columns: repeat(3, 1fr);
    }
}
</style>
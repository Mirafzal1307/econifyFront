<template>
    <header class="fixed inset-x-0 top-0 z-50 py-4 backdrop-blur-xl bg-neutral-200/20 dark:bg-neutral-800/20">
        <div class="w-full px-5 sm:px-10 md:px-12 lg:px-5 mx-auto max-w-7xl">
            <nav class="w-full flex justify-between gap-6 relative">
                <div class="min-w-max inline-flex relative">
                    <nuxt-link to="/" class="relative flex items-center gap-3">
                        <span class="flex">
                            <span class="w-3 h-6 rounded-l-full flex bg-emerald-600"></span>
                            <span class="w-3 h-6 rounded-r-full flex bg-teal-400 mt-1.5"></span>
                        </span>
                        <div class="inline-flex text-lg text-neutral-800 dark:text-white font-semibold">
                            Econify
                        </div>
                    </nuxt-link>
                </div>

                <div aria-hidden="true" class="fixed bg-border-neutral-700/50 inset-0 backdrop-filter bg-neutral-800/40"
                    :class="navIsOpen ? 'flex lg:hidden' : 'hidden lg:!hidden'">
                </div>

                <div class="absolute lg:relative w-full flex overflow-hidden duration-300 ease-linear lg:w-full lg:translate-y-0 top-full border lg:border-none border-neutral-200 dark:border-neutral-700 flex-col lg:flex-row gap-y-6 gap-x-4 lg:justify-between lg:items-center bg-white dark:bg-neutral-950 lg:bg-transparent lg:dark:bg-transparent    "
                    :class="navIsOpen ? 'translate-y-0 visible opacity-100' : 'translate-y-10 invisible opacity-0 lg:opacity-100 lg:visible lg:translate-y-0'">
                    <ul
                        class="px-6 lg:px-0 pt-6 lg:pt-0 flex flex-col lg:flex-row gap-y-4 gap-x-3 text-lg text-neutral-700 dark:text-neutral-300 w-full lg:justify-center lg:items-center">
                        <li v-for="navItem in navItems" :key="navItem.id">
                            <nuxt-link :to="navItem.href" class="duration-300 font-medium ease-linear hover:text-emerald-600 py-3">
                                {{ navItem.text }}
                            </nuxt-link>
                        </li>
                    </ul>

                    <div class="lg:min-w-max flex items-center sm:w-max w-full pb-6 lg:pb-0 px-6 lg:px-0">
                        <nuxt-link to="sign-in"
                            class="flex justify-center items-center w-full sm:w-max px-6 h-12 bg-emerald-600 rounded-full relative overflow-hidden border border-transparent hover:border-emerald-700 duration-300 ease-linear">
                            <span class="relative z-10 text-white">
                                Sign in
                            </span>
                        </nuxt-link>
                    </div>
                </div>



                <div class="min-w-max flex items-center gap-x-3">
                    <ui-toggle-theme />
                    <button aria-label="toggle navbar" @click="toggleNavBar()"
                        class="lg:hidden lg:invisible outline-none w-7 h-auto flex flex-col relative bg-transparent">
                        <span
                            class="bg-neutral-700 dark:bg-neutral-300 w-6 h-0.5 rounded-full transition-all duration-300 ease-linear"
                            :class="navIsOpen ? 'translate-y-1.5 rotate-40' : ''"></span>
                        <span
                            class="bg-neutral-700 dark:bg-neutral-300 w-6 origin-center mt-1 h-0.5 rounded-full transition-all duration-300 ease-linear"
                            :class="navIsOpen ? 'opacity-0 scale-x-0' : ''"></span>
                        <span
                            class="bg-neutral-700 dark:bg-neutral-300 w-6 mt-1 h-0.5 rounded-full transition-all duration-300 ease-linear"
                            :class="navIsOpen ? '-translate-y-1.5 -rotate-40' : ''"></span>
                    </button>
                </div>
            </nav>
        </div>
    </header>

</template>
<script setup>
const navIsOpen = useState('navIsOpen', () => false)
const navItems = [
    {
        id: 1,
        text: "Blog",
        href: "/",
    },
    {
        id: 2,
        text: "Team",
        href: "/team",
    },
    {
        id: 3,
        text: "About",
        href: "/",
    },
    {
        id: 4,
        text: "Newsletter",
        href: "/",
    }
]

function toggleNavBar() {
    navIsOpen.value = !navIsOpen.value
    document.body.classList.toggle("overflow-y-auto")
}
function closeNavBar() {
    navIsOpen.value = false
    ocument.body.classList.add("overflow-y-auto")
}
</script>
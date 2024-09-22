<template>
    <div class="min-h-screen flex items-center justify-center bg-neutral-1 dark:bg-neutral-9">
        <div class="w-full max-w-md p-6 bg-white dark:bg-neutral-800 rounded-lg shadow-md mx-4">
            <!-- Title -->
            <h1 class="text-2xl font-semibold text-center text-neutral-9 dark:text-white mb-6">Sign In</h1>

            <!-- Form -->
            <form @submit.prevent="onSubmit">
                <!-- Email Input -->
                <div class="mb-4">
                    <label for="email"
                        class="block text-sm font-medium text-neutral-9 dark:text-neutral-300 mb-2">Email</label>
                    <input v-model="email" type="email" id="email"
                        class="w-full px-4 py-2 border rounded-lg bg-neutral-2 dark:bg-neutral-7 text-neutral-9 dark:text-white border-neutral-3 dark:border-neutral-6 focus:outline-none focus:ring-2 focus:ring-emerald-600"
                        placeholder="Enter your email" />
                    <p v-if="emailError" class="text-sm text-red-500 mt-1">{{ emailError }}</p>
                </div>

                <!-- Password Input -->
                <div class="mb-6">
                    <label for="password"
                        class="block text-sm font-medium text-neutral-9 dark:text-neutral-300 mb-2">Password</label>
                    <input v-model="password" type="password" id="password"
                        class="w-full px-4 py-2 border rounded-lg bg-neutral-2 dark:bg-neutral-7 text-neutral-9 dark:text-white border-neutral-3 dark:border-neutral-6 focus:outline-none focus:ring-2 focus:ring-emerald-600"
                        placeholder="Enter your password" />
                    <p v-if="passwordError" class="text-sm text-red-500 mt-1">{{ passwordError }}</p>
                </div>

                <!-- Sign In Button -->
                <div>
                    <button type="submit"
                        class="w-full px-4 py-2 light:bg-emerald-600 text-white dark:bg-emerald-600 dark:text-white hover:bg-emerald-700 hover:dark:bg-emerald-700 rounded-lg font-medium focus:outline-none focus:ring-2 focus:ring-emerald-500">
                        Sign In
                    </button>

                </div>
            </form>
        </div>
    </div>
</template>

<script setup>
import { ref } from 'vue'

const email = ref('')
const password = ref('')
const emailError = ref('')
const passwordError = ref('')

const onSubmit = () => {
    // Reset error messages
    emailError.value = ''
    passwordError.value = ''

    // Basic Validation
    if (!email.value) {
        emailError.value = 'Email is required'
    } else if (!isValidEmail(email.value)) {
        emailError.value = 'Invalid email format'
    }

    if (!password.value) {
        passwordError.value = 'Password is required'
    } else if (password.value.length < 6) {
        passwordError.value = 'Password must be at least 6 characters'
    }

    // If both email and password are valid, proceed
    if (!emailError.value && !passwordError.value) {
        // Handle successful sign in (add your logic here)
        alert('Sign In successful!')
    }
}

const isValidEmail = (email) => {
    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/
    return emailRegex.test(email)
}
</script>

<style scoped>
/* You can customize the styles further */
</style>
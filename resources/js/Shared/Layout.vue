<template>
    <section class="p-6 bg-gray-200">
        <header class="flex justify-between">
            <div class="flex items-center">
                <h1 class="font-bold text-lg">My App</h1>

                <p class="text-sm ml-4">Welcome Back, {{ username }}!</p>
            </div>

            <Nav/>
        </header>
    </section>

    <section class="p-6">
        <div class="max-w-3xl mx-auto">
            <iframe
                class="mb-6"
                height="200px"
                width="100%"
                frameborder="no"
                scrolling="no"
                seamless
                src="https://player.simplecast.com/8510f7e5-d7b2-4c5b-87de-5193a8b928c3?dark=false"
            />
            <slot/>
        </div>
    </section>
</template>

<script>
import Nav from './Nav';

export default {
    components: {Nav},
    computed: {
        username() {
            return this.$page.props.auth.user.username;
        }
    }
}
</script>

<style scoped>

</style>

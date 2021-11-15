<template>
    <div class="container d-flex flex-column">
        <h2>
            Where to go?
            {{this.$route.params.data}}
        </h2>
        <div class="menu">
            <TheDestinations />
        </div>
    </div>
</template>

<script>
import TheDestinations from '@/components/TheDestinations.vue'

export default {
    name: 'Home',
    components: {TheDestinations}
}
</script>

<style scoped>
    h2 {
        color: #6a89cc;
    }
</style>
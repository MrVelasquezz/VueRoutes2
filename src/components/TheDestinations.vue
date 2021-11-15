<template>
    <div class="container d-flex flex-row justify-content-around align-items-center mt-5">
        <router-link class="destination-card" v-for="item in dastinations" :key="item.id"
            :to="{name: 'FindDestination', params: {id: item.id}}">
            <h4 class="mx-0">{{item.name}}</h4>
            <img :src="require(`@/assets/images/${item.image}`)" alt="item.name" class="img">
        </router-link>
    </div>
</template>

<script>
    import data from '@/database/data.json'

    export default {
        name: 'TheDestinations',
        data() {
            return {
                dastinations: data.destinations
            }
        }
    }
</script>

<style scoped>
    .destination-card {
        margin: 0 10px;
        width: 260px;
        height: 270px;
    }

    img.img {
        width: 250px;
    }

    a h4 {
        color: #1e3799;
        margin: 5px;
    }
</style>
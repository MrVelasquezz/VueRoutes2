<template>
    <div class="container">
        <div class="about-destination mx-auto mt-3">
            <h2 class="mb-3">{{getDestination.name}}</h2>
            <div class="description-container">
                <div>
                    <img :src="require(`@/assets/images/${getDestination.image}`)" alt="">
                </div>
                <div>
                    <p>{{getDestination.description}}</p>
                </div>
            </div>
        </div>

        <div class="container d-flex flex-row align-items-center justify-content-around mt-5">
            <div class="expirience-card" v-for="(item, key) in getDestination.experiences" :key="key">
                <div>
                    <h2>
                        {{item.name}}
                    </h2>
                </div>
                <div>
                    <img :src="require(`@/assets/images/${item.image}`)" alt="">
                </div>
                <a href="#" class="show" @click="toggle">Show description</a>
                <div class="description">
                    {{item.description}}
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import data from '@/database/data.json'

    export default {
        name: 'FindDestination',
        data() {
            return {
                destination: ''
            }
        },
        computed: {
            getDestination() {
                const destId = parseInt(this.$route.params.id)
                return data.destinations.find(destination => destination.id === destId)
            }
        },
        methods: {
            toggle(data){
                data.path[0].nextElementSibling.classList.toggle('des')
            }
        }
    }
</script>

<style scoped>
    img{
        width: 300px;
        margin-right: 20px;
    }
    .about-destination {
        width: 800px;
    }

    .description-container {
        display: flex;
        flex-direction: row;
    }
    .expirience-card{
        position: relative;
        width: 250px;
        height: 400px;
    }
    .expirience-card img{
        width: 250px;
    }
    .description{
        max-height: 0;
        overflow: hidden;
    }
    .des{
        max-height: max-content;
    }
    .show{
        color: #3c6382;
    }
</style>
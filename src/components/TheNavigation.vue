<template>
    <div id="nav" class="container-fluid p-0 m-0">
        <div class="container mx-auto d-flex justify-content-start align-items-enter py-4">
            <router-link to="/">Home</router-link>
            <router-link to="/destination/1">Brazil</router-link>
            <router-link to="/destination/2">Panama</router-link>
            <router-link to="/destination/3">Hawaii</router-link>
            <router-link to="/destination/4">Jamaica</router-link>
        </div>
    </div>
</template>


<style scoped>
    #nav {
        background: #0a3d62;
    }

    #nav a {
        color: #fff;
        font-size: 18px;
        text-decoration: none;
        margin-left: 25px;
    }

</style>
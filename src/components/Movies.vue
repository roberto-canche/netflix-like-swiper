<template>
    <div class="movie" v-bind:style="{ backgroundImage: 'url(' + image + ')' }">
        <div class="content">
            <h1 class="title">{{ title }}</h1>
            <p class="description">{{ description }}</p>
            <p class="duration">{{ duration }}</p>
        </div>
    </div>
</template>

<style scoped>
h1, h2 {
    font-weight:bold;
}
.movie {
    display:flex;
    flex-direction: column;
    align-items: flex-start;
    justify-content: flex-end;
    text-align: left;
    padding: 10px;
    width: 350px;
    height:500px;
    background-color: rgba(255, 255, 255, .4);
    background-repeat: no-repeat;
    background-blend-mode: overlay;
    background-size: cover;
}
</style>


<script>
    export default {
        name: 'Movies',
        props: [
            'image',
            'title',
            'description',
            'duration'
        ],
    }
</script>
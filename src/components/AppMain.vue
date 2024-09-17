<script>
// Imported components 
import AppCardList from "./AppCardsList.vue";

export default {

    data() {
        return {

        };
    },

    components: { AppCardList },

    methods: {

    }
};
</script>

<template>
    <main>
        <div class="jumbotron">
        </div>

        <div class="container">
            <AppCardList />
        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    background-image: url('../assets/img/jumbotron.jpg');
    background-size: cover;

    .jumbotron {
        height: 200px;
    }

    img {
        max-width: 100%;
    }

    .container {
        width: 80%;
        height: 70px;
        margin: 0 auto;
    }
}
</style>
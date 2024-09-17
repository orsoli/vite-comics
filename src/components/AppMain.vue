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
        <div class="card-list">
            <div class="container">
                <button class="btn current-series">Current Series</button>
                <AppCardList />
                <button class="btn learn-more">Learn More</button>
            </div>

        </div>
    </main>
</template>

<style lang="scss" scoped>
main {
    background-image: url('../assets/img/jumbotron.jpg');
    background-size: contain;

    .jumbotron {
        height: 250px;
    }


    img {
        max-width: 100%;
    }

    .container {
        text-align: center;
        width: 80%;
        margin: 0 auto;
        position: relative;

        .btn {
            color: white;
            background-color: #0182F9;
            border: 0;
            padding: 5px 10px;
        }

        .btn.current-series {
            position: absolute;
            top: -40px;
            left: 0;
        }

        .btn.learn-more {
            font-size: 12px;
        }
    }

    .card-list {
        background-color: #1C1C1C;
        padding: 20px;
    }
}
</style>
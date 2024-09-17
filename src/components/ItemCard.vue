<script>
export default {
    data() {
        return {

        };
    },

    props: {
        cardThumb: {
            type: String,
            required: true
        },
        cardTPrice: {
            type: String,
            required: false
        },
        cardSeries: {
            type: String,
            required: true
        },
        cardType: {
            type: String,
            required: false
        }
    },

    methods: {

    }
};
</script>

<template>
    <div class="card">
        <img :src="cardThumb" :alt="cardSeries">
        <p>{{ cardSeries }}</p>
    </div>
</template>

<style lang="scss" scoped>
.card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;

    img {
        height: 100px;
        width: 100%;
    }

    p {
        font-size: 12px;
    }
}
</style>
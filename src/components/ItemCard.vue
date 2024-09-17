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

    </div>
</template>

<style lang="scss" scoped></style>
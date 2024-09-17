<script>
export default {
    data() {
        return {
            logo: [
                {
                    id: 1,
                    name: "DC",
                    src: '../assets/img/dc-logo.png',
                    alt: "DC Logo",
                    link: "#"
                },
            ],
            navBars: [
                {
                    id: 2,
                    name: "character",
                    link: "#"
                },
                {
                    id: 3,
                    name: "comics",
                    link: "#"
                },
                {
                    id: 4,
                    name: "movies",
                    link: "#"
                },
                {
                    id: 5,
                    name: "tv",
                    link: "#"
                },
                {
                    id: 3,
                    name: "game",
                    link: "#"
                },
                {
                    id: 6,
                    name: "collectibles",
                    link: "#"
                },
                {
                    id: 7,
                    name: "video",
                    link: "#"
                },
                {
                    id: 8,
                    name: "fans",
                    link: "#"
                },
                {
                    id: 9,
                    name: "news",
                    link: "#"
                },
                {
                    id: 10,
                    name: "shop",
                    link: "#"
                },
                ", , movies, tv, games, collectibles, videos, fans, news, shop"
            ]
        };
    },
    methods: {

    }
};
</script>

<template>
    <header>

        <div class="container">
            <!-- Dc logo  -->
            <a :href="logo[0].link">
                <img src="../assets/img/dc-logo.png" :alt="logo[0].alt">
            </a>
            <!-- Navigation Bar  -->
            <nav>
                <ul>
                    <li v-for="navBar in navBars" :key="navBar.id">
                        <a href="{{ navBar.link }}">
                            <p> {{ navBar.name }} </p>
                        </a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
img {
    max-width: 100%;
}

header {

    background-color: white;
}

div.container {
    height: 70px;
    width: 80%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 0 auto;
}

ul {
    display: flex;
    gap: 1rem;
    list-style: none;
    line-height: 100%;
}

a {
    text-decoration: none;
    color: black;
}

a:hover {
    color: #0182F9;
}

img {
    width: 50px;
}
</style>
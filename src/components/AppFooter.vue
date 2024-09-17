<script>
export default {
    data() {
        return {
            headerIcons: [
                {
                    id: 1,
                    name: "digital comics",
                    src: "buy-comics-digital-comics.png",
                    alt: "Digital Comics icon",
                    link: "#"
                },
                {
                    id: 2,
                    name: "dc merchandise",
                    src: "buy-comics-merchandise.png",
                    alt: "DC Merchandise icon",
                    link: "#"
                },
                {
                    id: 3,
                    name: "subscriptions",
                    src: "buy-comics-subscriptions.png",
                    alt: "Subscriptions icon",
                    link: "#"
                },
                {
                    id: 4,
                    name: "comic shop locator",
                    src: "buy-comics-shop-locator.png",
                    alt: "Locator icon",
                    link: "#"
                },
                {
                    id: 5,
                    name: "dc power visa",
                    src: "buy-dc-power-visa.svg",
                    alt: "DC Power Visa icon",
                    link: "#"
                },

            ],
            navBarsGroup: [
                {
                    id: 111,
                    title: "dc comics",
                    navBars: [
                        {
                            id: 6,
                            name: "Character",
                            link: "#"
                        },
                        {
                            id: 7,
                            name: "Comics",
                            link: "#"
                        },
                        {
                            id: 8,
                            name: "Movies",
                            link: "#"
                        },
                        {
                            id: 9,
                            name: "Tv",
                            link: "#"
                        },
                        {
                            id: 10,
                            name: "Game",
                            link: "#"
                        },
                        {
                            id: 11,
                            name: "Video",
                            link: "#"
                        },
                        {
                            id: 12,
                            name: "News",
                            link: "#"
                        },
                    ]
                },
                {
                    id: 222,
                    title: "dc",
                    navBars: [
                        {
                            id: 13,
                            name: "Term of Use",
                            link: "#"
                        },
                        {
                            id: 14,
                            name: "Privacy Police (new)",
                            link: "#"
                        },
                        {
                            id: 15,
                            name: "Ad choices",
                            link: "#"
                        },
                        {
                            id: 16,
                            name: "Advertising",
                            link: "#"
                        },
                        {
                            id: 17,
                            name: "Job",
                            link: "#"
                        },
                        {
                            id: 18,
                            name: "Subscriptions",
                            link: "#"
                        },
                        {
                            id: 19,
                            name: "Talent Workshops",
                            link: "#"
                        },
                        {
                            id: 20,
                            name: "Cpsc Cartificates",
                            link: "#"
                        },
                        {
                            id: 21,
                            name: "Ratings",
                            link: "#"
                        },
                        {
                            id: 22,
                            name: "Shop Help",
                            link: "#"
                        },
                        {
                            id: 23,
                            name: "Contact Us",
                            link: "#"
                        },
                    ]
                },
                {
                    id: 333,
                    title: "sites",
                    navBars: [
                        {
                            id: 24,
                            name: "DC",
                            link: "#"
                        },
                        {
                            id: 25,
                            name: "MAD Magazine",
                            link: "#"
                        },
                        {
                            id: 26,
                            name: "DC Kids",
                            link: "#"
                        },
                        {
                            id: 27,
                            name: "DC Universe",
                            link: "#"
                        },
                        {
                            id: 28,
                            name: "DC Power Visa",
                            link: "#"
                        },
                    ]
                },
                {
                    id: 444,
                    title: "shop",
                    navBars: [
                        {
                            id: 29,
                            name: "Shop DC",
                            link: "#"
                        },
                        {
                            id: 30,
                            name: "Shop DC Collections",
                            link: "#"
                        },
                    ]
                },
            ],
            socialIcons: [
                {
                    id: 31,
                    src: "footer-facebook.png",
                    alt: "Facebook Icon",
                    link: "#"
                },
                {
                    id: 32,
                    src: "footer-twitter.png",
                    alt: "Twitter Icon",
                    link: "#"
                },
                {
                    id: 33,
                    src: "footer-youtube.png",
                    alt: "Youtube Icon",
                    link: "#"
                },
                {
                    id: 34,
                    src: "footer-pinterest.png",
                    alt: "Pinterest Icon",
                    link: "#"
                },
                {
                    id: 35,
                    src: "footer-periscope.png",
                    alt: "Periscope Icon",
                    link: "#"
                },
            ]

        };
    },

    methods: {
        getImgUrl(src) {
            return new URL(`../assets/img/${src}`, import.meta.url).href
        }

    },
};
</script>

<template>
    <footer>
        <div class="header">
            <div>
                <ul>
                    <li v-for="icon in headerIcons" :key="icon.id">
                        <img :src=getImgUrl(icon.src) :alt="icon.alt">
                        <p>{{ icon.name.toUpperCase() }}</p>
                    </li>
                </ul>
            </div>
        </div>
        <div class="main">
            <div class="nav-bar">
                <ul>
                    <li v-for="col in navBarsGroup" :key="col.id">
                        <ul class="navbar-list">
                            <h4>{{ col.title.toUpperCase() }}</h4>
                            <li v-for="navBar in col.navBars" :key="navBar.id">
                                <a href="#">{{ navBar.name }}</a>
                            </li>
                        </ul>
                    </li>
                </ul>
            </div>
            <div>
                <img src="../assets/img/dc-logo-bg.png" alt="bg-logo" id="logo-bg">
            </div>
        </div>
        <div class="footer">
            <div class="container">
                <div class="btn">
                    <button id="sign-up">SIGN-UP NOW!</button>
                </div>
                <div class="social">
                    <h4>FOLLOW US</h4>
                    <ul>
                        <li v-for="socialIcon in socialIcons" :key="socialIcon.id">
                            <a href="#">
                                <img :src="getImgUrl(socialIcon.src)" :alt="socialIcon.alt">
                            </a>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
img {
    max-width: 100%;
    max-height: 100%;
}

footer {
    position: relative;
    color: white;
    background-image: url(../assets/img/footer-bg.jpg);
    background-size: cover;

    .header {
        background-color: #0182F9;
        padding: 1rem;
    }

    .main {
        display: flex;
        text-align: start;

        .navbar-list {
            display: flex;
            flex-direction: column;

            h4 {
                margin: 0;
            }
        }

        .navbar>ul {
            flex-wrap: wrap;
        }

        #logo-bg {
            position: absolute;
            top: 0;
            right: 0;
            bottom: 0;
        }

        ul {
            justify-content: start;
        }
    }

    ul {
        list-style: none;
        display: flex;
        justify-content: center;
        gap: 1rem;

    }

    li {
        display: flex;
        gap: 5px;
        font-size: 12px;
    }

    li>img {
        height: 30px;
    }

    a {
        text-decoration: none;
        font-size: 0.6rem;
        color: gray;
        padding: 0;
        margin: 0;
    }

    .footer {
        height: 70px;
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #303030;

        .container {
            width: 80%;
            display: flex;
            justify-content: space-between;
            align-items: center;
            align-self: center;

            #sign-up {
                color: white;
                font-size: 12px;
                background: transparent;
                border: 2px solid #0182F9;
                padding: 10px;
            }

            .social {
                display: flex;
                color: #0182F9;
                gap: 20px;

                ul {
                    padding: 0;
                }

                li img {
                    width: 30px;
                }
            }
        }

    }

}
</style>
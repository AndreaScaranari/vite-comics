<script>
export default {
    name: "AppFooter",
    data: () => ({
        imgName: "dc-logo-bg.png",
        logos: ["footer-facebook.png", "footer-twitter.png", "footer-youtube.png", "footer-pinterest.png", "footer-periscope.png"],
        comicsDCLinks: [
            {
                text: 'Characters',
                url: '#',
            },
            {
                text: 'Comics',
                url: '#',
            },
            {
                text: 'Movies',
                url: '#',
            },
            {
                text: 'TV',
                url: '#',
            },
            {
                text: 'Games',
                url: '#',
            },
            {
                text: 'Collectibles',
                url: '#',
            },
            {
                text: 'Videos',
                url: '#',
            },
            {
                text: 'Fans',
                url: '#',
            },
            {
                text: 'News',
                url: '#',
            }
        ],
        shopLinks: [
            {
                text: 'Shop DC',
                url: '#',
            },
            {
                text: 'Shop DC Collectibles',
                url: '#',
            },
        ],
        dcLinks: [
            {
                text: 'Terms Of Use',
                url: '#',
            },
            {
                text: 'Privacy policy (New)',
                url: '#',
            },
            {
                text: 'Ad Choices',
                url: '#',
            },
            {
                text: 'Advertising',
                url: '#',
            },
            {
                text: 'Jobs',
                url: '#',
            },
            {
                text: 'Subscriptions',
                url: '#',
            },
            {
                text: 'Talent Workshops',
                url: '#',
            },
            {
                text: 'CPSC Certificates',
                url: '#',
            },
            {
                text: 'Ratings',
                url: '#',
            },
            {
                text: 'Shop Help',
                url: '#',
            },
            {
                text: 'Contact Us',
                url: '#',
            },
        ],
        sitesLinks: [
            {
                text: 'DC',
                url: '#',
            },
            {
                text: 'MAD Magazine',
                url: '#',
            },
            {
                text: 'DC Kids',
                url: '#',
            },
            {
                text: 'DC Universe',
                url: '#',
            },
            {
                text: 'DC Power Visa',
                url: '#',
            },
        ],
    }),
    methods: {
        createImagePath(imgName) {
            const url = new URL(`../assets/img/${imgName}`, import.meta.url);
            return url.href
        }
    }
}
</script>

<template>
    <footer>
        <div class="upper">
            <div class="container">
                <div class="nav-bar">
                    <div class="col">
                        <h3>DC COMICS</h3>
                        <nav>
                            <ul>
                                <li v-for="(li, i) in comicsDCLinks" :key="i"><a :href="li.url">{{ li.text }}</a></li>
                            </ul>
                        </nav>
                        <h3>Shop</h3>
                        <nav>
                            <ul>
                                <li v-for="(li, i) in shopLinks" :key="i"><a :href="li.url">{{ li.text }}</a></li>
                            </ul>
                        </nav>
                    </div>
                    <div class="col">
                        <h3>DC</h3>
                        <nav>
                            <ul>
                                <li v-for="(li, i) in dcLinks" :key="i"><a :href="li.url">{{ li.text }}</a></li>
                            </ul>
                        </nav>
                    </div>
                    <div class="col">
                        <h3>SITES</h3>
                        <nav>
                            <ul>
                                <li v-for="(li, i) in sitesLinks" :key="i"><a :href="li.url">{{ li.text }}</a></li>
                            </ul>
                        </nav>
                    </div>
                </div>
                <img :src="createImagePath(imgName)" :alt="imgName">
            </div>
        </div>

        <div class="bottom">
            <div class="container">
                <a class="button" href="">SIGN-UP NOW!</a>
                <div class="social">
                    <H3>FOLLOW US</H3>
                    <nav class="social-icons">
                        <li v-for="(logo, i) in logos" :key="i"><a href="#"><img :src="createImagePath(logo)"
                                    :alt="logo"></a></li>
                    </nav>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
@use "@/scss/variables" as *;

footer {
    .upper {
        height: 400px;
        background-image: url("../assets/img/footer-bg.jpg");
        background-size: cover;
        display: flex;
        justify-content: space-between;
        overflow: hidden;
    }

    h3 {
        color: white;
        padding: 1rem 0;
    }

    .nav-bar {
        display: flex;
        align-self: flex-start;
        margin-top: 1rem;
    }

    .col {
        width: 140px;
    }

    img {
        height: 150%;
        align-self: center;
    }

    .upper a {
        color: #797979;
        font-size: small;
        font-weight: 500;
    }

    .bottom {
        height: 120px;
        background-color: #303030;
        display: flex;
        align-items: center;
        justify-content: space-between;

        h3 {
            color: $blue;
            padding-right: 2rem;
        }

        .button {
            color: white;
            border: 2px solid $blue;
            padding: 1rem;
        }
    }

    .social {
        display: flex;
        align-items: center;
    }

    .social-icons {
        display: flex;
        align-items: center;
        gap: 1rem;
    }
}
</style>

<script>
export default {
    name: "AppFooter",
    data: () => ({
        imgName: "dc-logo-bg.png",
        fbLogo: "footer-facebook.png",
        peLogo: "footer-periscope.png",
        piLogo: "footer-pinterest.png",
        twLogo: "footer-twitter.png",
        ytLogo: "footer-youtube.png"
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
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                            </ul>
                        </nav>
                        <h3>Shop</h3>
                        <nav>
                            <ul>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                            </ul>
                        </nav>
                    </div>
                    <div class="col">
                        <h3>DC</h3>
                        <nav>
                            <ul>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                            </ul>
                        </nav>
                    </div>
                    <div class="col">
                        <h3>SITES</h3>
                        <nav>
                            <ul>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
                                <li><a href="#">Lorem</a></li>
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
                        <li><a href="#"><img :src="createImagePath(fbLogo)" :alt="fbLogo"></a></li>
                        <li><a href="#"><img :src="createImagePath(twLogo)" :alt="twLogo"></a></li>
                        <li><a href="#"><img :src="createImagePath(ytLogo)" :alt="ytLogo"></a></li>
                        <li><a href="#"><img :src="createImagePath(piLogo)" :alt="piLogo"></a></li>
                        <li><a href="#"><img :src="createImagePath(peLogo)" :alt="peLogo"></a></li>
                    </nav>
                </div>
            </div>
        </div>
    </footer>
</template>

<style scoped>
footer .upper {
    height: 400px;
    background-image: url("../assets/img/footer-bg.jpg");
    background-size: cover;
    display: flex;
    justify-content: space-between;
    overflow: hidden;
}

footer .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
}

footer h3 {
    color: white;
    padding: 1rem 0;
}

footer .nav-bar {
    display: flex;
    align-self: flex-start;
    margin-top: 1rem;
}

.upper a {
    color: #797979;
}

footer .col {
    width: 140px;
}

footer img {
    height: 150%;
    align-self: center;
}

footer .bottom {
    height: 120px;
    background-color: #303030;
    display: flex;
    align-items: center;
    justify-content: space-between;
}

.bottom h3 {
    color: #0282F9;
    padding-right: 2rem;
}

footer .social {
    display: flex;
    align-items: center;
}

footer .social-icons {
    display: flex;
    align-items: center;
    gap: 1rem;
}

.bottom .button {
    color: white;
    border: 2px solid #0282F9;
    padding: 1rem;
}
</style>

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

        <div class="bottom">
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
    </footer>
</template>

<style scoped>
footer .upper {
    height: 400px;
    background-image: url("../assets/img/footer-bg.jpg");
    display: flex;
    justify-content: space-between;
    overflow: hidden;
}

footer h3 {
    color: white;
}

footer .nav-bar {
    display: flex;
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
    margin: 0;
    color: #0282F9;
    padding-right: 1rem;
}

footer .social {
    display: flex;
    align-items: center;

}

footer .social-icons {
    display: flex;
    align-items: center;
    gap: 0.4rem;
}

.bottom .button {
    color: white;
    border: 2px solid #0282F9;
    padding: 1rem;
}
</style>

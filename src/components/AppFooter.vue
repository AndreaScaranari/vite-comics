<script>
export default {
    name: "AppFooter",
    data: () => ({
        imgName: "dc-logo-bg.png"
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

            <img :src="createImagePath(imgName)" :alt="imgName">
        </div>
        <div class="bottom">
            <a href=""></a>
            <div class="social"></div>
        </div>
    </footer>
</template>

<style scoped>
footer .upper {
    height: 400px;
    background-image: url("../assets/img/footer-bg.jpg");
    display: flex;
    justify-content: space-between;
}

footer .bottom {
    height: 120px;
    background-color: #303030;
}
</style>

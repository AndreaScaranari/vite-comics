<script>
export default {
    name: "AppBluestripe",
    data: () => ({
        blueStripeObjects: [
            {
                img: "buy-comics-digital-comics.png",
                text: "DIGITAL COMICS",
                href: "#"
            },
            {
                img: "buy-comics-merchandise.png",
                text: "DC MERCHANDISE",
                href: "#"
            },
            {
                img: "buy-comics-subscriptions.png",
                text: "SUBSCRIPTION",
                href: "#"
            },
            {
                img: "buy-comics-shop-locator.png",
                text: "COMIC SHOP LOCATOR",
                href: "#"
            },
            {
                img: "buy-dc-power-visa.svg",
                text: "DC POWER VISA",
                href: "#"
            },
        ]
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
    <div class="blue-stripe">
        <ul class="container">
            <li v-for="(obj, i) in blueStripeObjects" :key="i">
                <a :href="obj.href">
                    <img :src="createImagePath(obj.img)" :alt="obj.text">
                    <p>{{ obj.text }}</p>
                </a>
            </li>
        </ul>
    </div>
</template>

<style lang="scss" scoped>
@use "@/scss/variables" as *;

.blue-stripe {
    background-color: $blue;
    width: 100%;
    height: 150px;

    ul {
        justify-content: space-evenly;
    }

    li {
        height: 50%;
        width: 20%;
    }

    a {
        color: white;
        display: flex;
        height: 100%;
        align-items: center;
        justify-content: center;
        gap: 1rem;


        img {
            max-height: 70%;
            max-width: 50px;
        }

    }

}
</style>
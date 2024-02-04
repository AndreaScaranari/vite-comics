<script>
export default {
    name: "AppHeader",
    data: () => ({
        imageName: "dc-logo.png",
        headerUL: [
            {
                text: 'Characters',
                url: '#',
                current: false,
            },
            {
                text: 'Comics',
                url: '#',
                current: true,
            },
            {
                text: 'Movies',
                url: '#',
                current: false,
            },
            {
                text: 'TV',
                url: '#',
                current: false,
            },
            {
                text: 'Games',
                url: '#',
                current: false,
            },
            {
                text: 'Collectibles',
                url: '#',
                current: false,
            },
            {
                text: 'Videos',
                url: '#',
                current: false,
            },
            {
                text: 'Fans',
                url: '#',
                current: false,
            },
            {
                text: 'News',
                url: '#',
                current: false,
            },
            {
                text: 'Shop',
                url: '#',
                current: false,
            },
        ]
    }),
    methods: {
        createImaginePath(imageName) {
            const url = new URL(`../assets/img/${imageName}`, import.meta.url);
            return url.href
        }
    }
}
</script>

<template>
    <header>
        <div class="container">
            <img :src="createImaginePath(imageName)" :alt="imageName">
            <ul>
                <li v-for="(li, i) in headerUL" :key="i"><a :href="li.url" :class="{ active: li.current }">{{ li.text }}</a>
                </li>
            </ul>
        </div>
    </header>
</template>

<style scoped lang="scss">
@use "@/scss/variables" as *;

header {
    height: 120px;
    background-color: white;
    margin-top: 1rem;

    img {
        max-height: 70%;
    }

    ul {
        list-style: none;
        display: flex;
        align-items: center;
    }

    a {
        display: block;
        padding: 0 1rem;
        color: #303030;
        line-height: 116px;
        border-bottom: 4px solid transparent;
        font-size: small;
        font-weight: 700;
        text-transform: uppercase;
    }

    a:hover {
        color: $blue;
    }

    .active {
        color: $blue;
        border-bottom: 4px solid $blue;
    }
}
</style>

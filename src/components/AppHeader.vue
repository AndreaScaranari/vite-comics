<script>
export default {
    name: "AppHeader",
    data: () => ({
        imageName: "dc-logo.png"
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
        <img :src="createImaginePath(imageName)" :alt="imageName">
        <ul>
            <li><a href="#">CHARACTERS</a></li>
            <li><a href="#">CHARACTERS</a></li>
            <li><a href="#">CHARACTERS</a></li>
            <li><a href="#">CHARACTERS</a></li>
            <li><a href="#">CHARACTERS</a></li>
            <li><a href="#">CHARACTERS</a></li>
            <li><a href="#">CHARACTERS</a></li>
            <li><a href="#">CHARACTERS</a></li>
            <li><a href="#">CHARACTERS</a></li>
            <li><a href="#">CHARACTERS</a></li>
        </ul>
    </header>
</template>

<style scoped>
header {
    height: 120px;
    background-color: white;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

header img {
    max-height: 70%;
}

header ul {
    list-style: none;
    display: flex;
    align-items: center;
    margin: 0;
}

header a {
    display: block;
    padding: 0 0.4rem;
    color: #303030;
    line-height: 116px;
    border-bottom: 4px solid transparent;
}

header a:hover {
    color: #0282F9;
    border-bottom: 4px solid #0282F9;
}
</style>

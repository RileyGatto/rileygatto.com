<template>
    <footer>
        <h3><a href="https://github.com/RileyGatto" target="blank">Github</a></h3>
        <h3><a href="https://www.linkedin.com/in/riley-gatto" target="blank">LinkedIn</a></h3>
        <h3><a href="https://youtube.com/@RileyGatto" target="blank">Youtube</a></h3>
    </footer>
</template>

<script></script>

<style scoped>
    footer {
        gap: 10px;
        display: flex;
        justify-content: space-between;
        border-top: 3px solid rgba(255, 255, 255, 0.87);
        padding-left: 20px;
        padding-right: 20px;
    }

    a {
        text-decoration: none;
    }

    @media (max-width: 500px) {
        footer {
            display: block;
        }
    }
</style>

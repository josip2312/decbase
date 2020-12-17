<template>
    <nav class="nav">
        <a class="nav-link" href="#">Home </a>
        <a class="nav-link" href="#services">Services </a>
        <a class="nav-link" href="#about">About </a>
        <a class="nav-link" href="#testimonials">Testimonials </a>
        <a class="nav-link" href="#blog">Blog </a>
        <a class="nav-link" href="#contact">Contact </a>
    </nav>
</template>

<script>
export default {
    name: 'Navigation',
};
</script>

<style scoped lang="scss">
.nav {
    position: absolute;
    right: 0;
    top: 0;

    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;

    height: 100vh;
    width: 70vw;
    z-index: -1;
    background-color: var(--secondary-400);
    transform: translateX(70vw);
    padding-left: 15%;

    opacity: 0;
    transition: opacity 350ms ease-in-out, transform 350ms ease-in-out;

    @include mq-min($v-8) {
        transform: translateX(0);
        opacity: 1;
        background-color: var(--white);

        position: relative;
        z-index: 0;
        height: auto;
        width: auto;

        padding-left: 0;
        align-items: center;

        flex-direction: row;
        & > * + * {
            margin-left: 2.5rem;
        }
    }

    .nav-link {
        padding: 2.5rem 0;
        font-size: 2.25rem;
        text-transform: uppercase;
        font-weight: 600;
        color: #3a3a3b;
        @media only screen and(min-width:$v-8) {
            font-weight: 400;
            font-size: 1.6rem;
            padding: 0;
        }
    }
}
.nav.visible {
    transform: translateX(0);
    opacity: 1;
}
</style>

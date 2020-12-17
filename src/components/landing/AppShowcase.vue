<template>
    <section class="showcase">
        <div class="container">
            <div class="showcase-content">
                <div class="section-intro">Modern Interior</div>
                <h1 class="heading-1">Create Your Interior Design</h1>
                <p class="showcase-paragraph">
                    Lorem ipsum, dolor sit amet consectetur adipisicing elit.
                    Iure nemo quas consequatur excepturi quidem molestiae?
                    Distinctio excepturi pariatur quaerat quae!
                </p>
                <button class="btn">Contact</button>
            </div>
            <div class="showcase-image after-right">
                <img
                    src="@/assets/images/roomShowcase.jpg"
                    alt="Home interior"
                />
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'AppShowcase',
};
</script>

<style lang="scss" scoped>
.showcase {
    padding: 7.5rem 0;
    @include mq-min($v-12) {
        padding: 20rem 0;
    }
}
.container {
    display: flex;
    flex-direction: column;

    @include mq-min($v-12) {
        & > * + * {
            margin-left: 3rem;
        }
        flex-direction: row;
        align-items: center;
    }
}
.showcase-content {
    flex: 1;
    padding-top: 7.5em;
    padding-bottom: 5em;
    max-width: 60rem;
    text-align: center;
    margin: 0 auto;
    @include mq-min($v-12) {
        text-align: left;

        padding-top: 0;
        padding-bottom: 0;
    }

    .heading-1 {
        margin-bottom: 2.5rem;
    }
    .showcase-paragraph {
        color: var(--font-paragraph);
        margin-bottom: 3.5rem;
        max-width: 50rem;
        margin-left: auto;
        margin-right: auto;
        @include mq-min($v-12) {
            margin-left: 0;
        }
    }
}
.showcase-image {
    flex: 1.2;
    position: relative;

    img {
        border-radius: 10rem 0;
    }
}
</style>

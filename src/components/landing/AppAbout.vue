<template>
    <section id="about" class="about">
        <div class="container">
            <div class="about-image after-left">
                <img src="@/assets/images/roomAbout.jpg" alt="Furniture" />
            </div>
            <div class="about-content">
                <div class="section-intro">About us</div>
                <h2 class="heading-2">We Offer High Quality Interiors</h2>
                <p class="about-paragraph">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Fugiat porro vel ex delectus? Quis dignissimos autem et
                    doloremque harum aut.
                </p>
                <button class="btn">Learn more</button>
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'About',
};
</script>

<style lang="scss" scoped>
.about {
    padding: 5rem 0;
    @include mq-min($v-12) {
        padding: 7.5rem 0;
    }
}

.container {
    display: flex;
    flex-direction: column;

    @include mq-min($v-12) {
        flex-direction: row;
        align-items: center;
    }
}

.about-image {
    flex: 1.2;

    position: relative;

    img {
        border-radius: 10rem 0;
    }
}

.about-content {
    flex: 1;
    max-width: 60rem;
    text-align: center;
    margin-left: auto;
    margin-right: auto;
    margin-top: 5rem;

    @include mq-min($v-12) {
        margin-top: 0rem;
        margin-left: 5rem;
        text-align: left;
    }
    .heading-2 {
        margin-bottom: 2.5rem;
    }
    .about-paragraph {
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
</style>

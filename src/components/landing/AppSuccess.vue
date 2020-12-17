<template>
    <section id="success" class="success">
        <div class="container">
            <div class="success-content">
                <div class="success-number">20</div>
                <h2 class="heading-2">Years successfuly working the market</h2>
                <button class="btn">Read more</button>
            </div>
            <div class="success-image after-right">
                <img src="@/assets/images/roomAbout2.jpg" alt="Furniture" />
            </div>
        </div>
    </section>
</template>

<script>
export default {
    name: 'AppSuccess',
};
</script>

<style lang="scss" scoped>
.success {
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
.success-image {
    flex: 1.2;
    position: relative;

    img {
        border-radius: 10rem 0;
    }
}

.success-content {
    flex: 1;
    max-width: 60rem;
    margin-bottom: 5rem;
    text-align: center;
    margin-left: auto;
    margin-right: auto;
    @include mq-min($v-12) {
        text-align: left;
        margin-right: 5rem;
        margin-bottom: 0;
    }
    .success-number {
        font-size: 15rem;
        line-height: 1.25;
    }

    .heading-2 {
        margin-bottom: 2.5rem;
    }
}
</style>

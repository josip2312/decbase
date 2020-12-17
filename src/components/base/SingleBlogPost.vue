<template>
    <div class="blog-post">
        <div class="blog-post-image after-right">
            <img :src="blogPost.image" alt="" />
        </div>
        <h3 class="heading-3">{{ blogPost.title }}</h3>
        <p class="blog-post-paragraph">
            {{ blogPost.paragraph }}
        </p>
        <button class="btn">Continue reading</button>
    </div>
</template>

<script>
export default {
    name: 'SingleBlogPost',
    props: {
        blogPost: {
            type: Object,
            required: true,
        },
    },
};
</script>

<style lang="scss" scoped>
.blog-post {
    display: flex;
    flex-direction: column;
    align-items: center;
    @include mq-min($v-12) {
        align-items: flex-start;
    }
    .heading-3 {
        margin-bottom: 1.25rem;
    }
    &-paragraph {
        margin-bottom: 3rem;
        color: var(--font-paragraph);
        max-width: 40rem;
        @include mq-min($v-12) {
            text-align: left;
        }
    }
    &-image {
        position: relative;
        margin-bottom: 4rem;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
            border-radius: 10rem 0;
        }
    }
}
</style>

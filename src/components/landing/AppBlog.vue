<template>
    <section id="blog" class="blog">
        <div class="container">
            <div class="section-intro">Latest news</div>
            <h2 class="heading-2">Check out our blog</h2>
            <div class="blog-posts">
                <SingleBlogPost
                    v-for="blogPost in blogPosts"
                    :key="blogPost.title"
                    :blogPost="blogPost"
                />
            </div>
        </div>
    </section>
</template>

<script>
import { blogPosts } from '@/data/blogPosts';
import SingleBlogPost from '@/components/base/SingleBlogPost';
export default {
    name: 'AppBlog',
    components: {
        SingleBlogPost,
    },
    data() {
        return {
            blogPosts: blogPosts,
        };
    },
};
</script>

<style lang="scss" scoped>
.blog {
    text-align: center;
    padding: 5rem 0;
    @include mq-min($v-12) {
        padding: 7.5rem 0;
    }
}
.heading-2 {
    margin-bottom: 3rem;
    @include mq-min($v-12) {
        margin-bottom: 5rem;
    }
}
.blog-posts {
    display: flex;
    flex-direction: column;
    & > * + * {
        margin-top: 7.5rem;
    }
    @include mq-min($v-12) {
        flex-direction: row;

        & > * + * {
            margin-top: 0;
            margin-left: 7.5rem;
        }
    }
}
</style>

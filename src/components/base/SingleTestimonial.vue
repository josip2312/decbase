<template>
    <div class="testimonial">
        <div class="wrapper spacing">
            <div class="testimonial-image">
                <img :src="testimonial.image" alt="" />
            </div>
            <div class="testimonial-content">
                <h3 class="heading-3">{{ testimonial.name }}</h3>
                <span>{{ testimonial.occupation }}</span>
                <p class="testimonial-paragraph">
                    {{ testimonial.paragraph }}
                </p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SingleTestimonial',
    props: {
        testimonial: {
            type: Object,
            required: true,
        },
    },
};
</script>

<style lang="scss" scoped>
.testimonial {
    box-shadow: var(--box-shadow);
    padding: 3.5rem 2.5rem;
    border-radius: 6rem 0;
}

.wrapper {
    margin: 0 auto;
    display: flex;
    flex-direction: column;
    align-items: center;
    @include mq-min($v-12) {
        flex-direction: row;
        justify-content: space-between;
    }
    .testimonial-image {
        max-width: 10rem;
        @include mq-min($v-12) {
            margin-right: 5rem;
        }
        img {
            border-radius: 3.5rem 0;
        }
    }
}
.testimonial-content {
    display: flex;
    flex-direction: column;
    align-items: center;
    @include mq-min($v-12) {
        align-items: flex-start;
    }
    .heading-4 {
        margin-bottom: 0.5rem;
    }
    span {
        color: var(--font-paragraph);
        margin-bottom: 1.5rem;
    }
    .testimonial-paragraph {
        text-align: left;
        max-width: 35rem;
        color: var(--font-paragraph);
    }
}
</style>

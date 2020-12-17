<template>
    <section id="testimonials" class="testimonials">
        <div class="container">
            <div class="section-intro">Testimonials</div>
            <h2 class="heading-2">What our clients say</h2>
            <div class="testimonials-container">
                <SingleTestimonial
                    v-for="testimonial in testimonials"
                    :key="testimonial.name"
                    :testimonial="testimonial"
                />
            </div>
        </div>
    </section>
</template>

<script>
import { testimonials } from '@/data/testimonials';
import SingleTestimonial from '@/components/base/SingleTestimonial';
export default {
    name: 'AppTestimonials',
    components: {
        SingleTestimonial,
    },
    data() {
        return {
            testimonials: testimonials,
        };
    },
};
</script>

<style lang="scss" scoped>
.testimonials {
    text-align: center;
    padding: 5rem 0;
    @include mq-min($v-12) {
        padding: 7.5rem 0;
    }
}
.heading-2 {
    margin-bottom: 5rem;
}
.testimonials-container {
    display: flex;
    flex-direction: column;
    & > * + * {
        margin-top: 5rem;
    }
    @include mq-min($v-12) {
        flex-direction: row;
        justify-content: space-between;

        & > * + * {
            margin-top: 0;
        }
    }
}
</style>

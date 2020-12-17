<template>
    <section class="services">
        <div class="container">
            <div class="section-intro">What we do</div>
            <h2 class="heading-2">Our services</h2>
            <div class="services-container">
                <SingleService
                    v-for="service in services"
                    :key="service.heading"
                    :service="service"
                />
            </div>
        </div>
    </section>
</template>

<script>
import { services } from '@/data/services';
import SingleService from '@/components/base/SingleService';
export default {
    name: 'AppServices',
    components: {
        SingleService,
    },
    data() {
        return {
            services: services,
        };
    },
};
</script>

<style lang="scss" scoped>
.services {
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
.section-intro,
.heading-2 {
    text-align: center;
    @include mq-min($v-12) {
        text-align: left;
    }
}
.services-container {
    display: flex;
    flex-direction: column;
    & > * + * {
        margin-top: 5rem;
    }
    @include mq-min($v-12) {
        flex-direction: row;
        & > * + * {
            margin-top: 0;
            margin-left: 3.5rem;
        }
    }
}
</style>

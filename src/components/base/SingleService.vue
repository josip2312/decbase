<template>
    <div class="service">
        <div class="wrapper spacing">
            <div class="service-heading">
                <div class="service-logo">
                    <div v-html="service.logo"></div>
                </div>
                <h3 class="heading-3">{{ service.heading }}</h3>
            </div>
            <p class="service-paragraph">
                {{ service.paragraph }}
            </p>
        </div>
    </div>
</template>

<script>
export default {
    name: 'SingleService',
    props: {
        service: {
            type: Object,
            required: true,
        },
    },
};
</script>

<style lang="scss" scoped>
.service {
    box-shadow: var(--box-shadow);
    padding: 5rem 2.5rem;
    border-radius: 6rem 0;

    display: flex;
    flex-direction: column;
    align-items: flex-start;

    transition: background-color 250ms ease-in-out, color 250ms ease-in-out;

    &-logo {
        width: 4.5rem;
    }

    &-paragraph {
        max-width: 40rem;
        color: var(--font-paragraph);
    }
}
.service:hover {
    --tertiary: #92724e;
    background-color: var(--tertiary);
    color: var(--white);

    .service-paragraph {
        color: var(--font-secondary);
    }
}

.wrapper {
    margin: 0 auto;
}
.service-heading {
    display: flex;
    align-items: center;
    .service-logo {
        margin-right: 2.5rem;
    }
}
</style>

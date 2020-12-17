<template>
    <header class="header">
        <div class="container">
            <a class="logo">Decbase</a>

            <button class="nav-toggle" @click="toggleNavigation">
                <img
                    v-if="!isNavigationVisible"
                    src="@/assets/icons/menu.svg"
                    alt=""
                />

                <img
                    v-if="isNavigationVisible"
                    src="@/assets/icons/x.svg"
                    alt=""
                />
            </button>
            <Navigation :class="{ visible: isNavigationVisible }" />
        </div>
    </header>
</template>

<script>
import Navigation from '@/components/layout/Navigation';
export default {
    name: 'TheHeader',
    components: {
        Navigation,
    },
    data() {
        return {
            isNavigationVisible: false,
        };
    },
    methods: {
        toggleNavigation() {
            this.isNavigationVisible = !this.isNavigationVisible;
        },
        hideNavigation() {
            this.isNavigationVisible = false;
        },
    },
};
</script>

<style lang="scss" scoped>
.header {
    position: fixed;
    z-index: 100;
    top: 0;
    left: 0;
    right: 0;
    background-color: var(--white);
}
.container {
    display: flex;
    justify-content: space-between;

    .logo {
        padding: 1.25rem 0;
        font-size: 2rem;
        font-weight: bold;
        color: var(--accent-dark);
        cursor: pointer;
        &:hover {
            opacity: 1;
        }
    }

    .nav-toggle {
        align-self: center;
        cursor: pointer;
        @media only screen and(min-width:$v-8) {
            display: none;
        }
        img {
            width: 3.5rem;
        }
    }
}
</style>

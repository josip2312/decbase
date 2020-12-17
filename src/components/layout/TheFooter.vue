<template>
    <footer class="footer">
        <div class="container">
            <div class="footer-brands">
                <div class="footer-logo">Logo</div>
                <p class="footer-paragraph">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit.
                    Cum, consectetur.
                </p>
            </div>
            <div class="footer-links">
                <h4 class="footer-heading heading-4">Links</h4>
                <a href="#">About</a>
                <a href="#">Services</a>
                <a href="#">Career</a>
                <a href="#">Privacy</a>
            </div>
            <div class="footer-contact">
                <h4 class="footer-heading heading-4">Contact</h4>

                <div class="address">Addres this and that</div>
                <div class="email">decbase@gmail.com</div>
                <div class="contact">000222000</div>
            </div>
            <div class="footer-social">
                <h4 class="footer-heading heading-4">Follow us</h4>

                <div class="footer-social-links">
                    <a href="#">
                        <img src="@/assets/icons/facebook.svg" alt="" />
                    </a>
                    <a href="#">
                        <img src="@/assets/icons/instagram.svg" alt="" />
                    </a>
                    <a href="#">
                        <img src="@/assets/icons/twitter.svg" alt="" />
                    </a>
                    <a href="#">
                        <img src="@/assets/icons/github.svg" alt="" />
                    </a>
                </div>
            </div>
        </div>
    </footer>
</template>

<style lang="scss" scoped>
.footer {
    padding: 5em 0;
    background-color: var(--secondary-400);
    color: var(--font-paragraph);
    @include mq-min($v-10) {
        padding: 7.5em 0;
    }
}
.footer-heading {
    margin-bottom: 2.5rem;
}
.container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(25rem, 1fr));
    gap: 7.5rem 5rem;
}
.footer-brands {
    font-size: 1.8rem;
    .footer-logo {
        margin-bottom: 1.5rem;
    }
    .footer-paragraph {
        max-width: 35rem;
        margin-right: 2.5rem;
    }
}
.footer-links {
    display: flex;
    flex-direction: column;
    line-height: 2;
    font-size: 1.8rem;
    a {
        color: var(--font-paragraph);

        &:hover {
            text-decoration: underline;
        }
    }
}
.footer-contact {
    line-height: 2;

    font-size: 1.8rem;
}
.footer-social {
    &-links {
        display: flex;
        align-items: center;
        img {
            width: 2.5rem;
        }
        & > * + * {
            margin-left: 2rem;
        }
    }
}
</style>

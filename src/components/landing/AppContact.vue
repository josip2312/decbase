<template>
    <section class="contact">
        <div class="container">
            <h2 class="heading-2">Don't forget to sign up!</h2>
            <p class="contact-paragraph">
                Find out early about all upcoming promotions and new product
                releases with our newsletter.
            </p>
            <form class="form">
                <input
                    type="text"
                    placeholder="Enter your email address..."
                    id="newsletter"
                />
                <button class="btn">Subscribe</button>
            </form>
        </div>
    </section>
</template>

<script>
export default {
    name: 'AppContact',
};
</script>

<style lang="scss" scoped>
.contact {
    padding: 7.5rem 0;
    @include mq-min($v-12) {
        padding: 10rem 0;
    }
}
.container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}
.heading-2 {
    margin-bottom: 5rem;
}
.contact-paragraph {
    text-align: center;
    color: var(--font-paragraph);
    margin-bottom: 3.5rem;
    max-width: 40rem;
}
.form {
    display: flex;
    align-items: center;
    width: 100%;
    max-width: 70rem;
    input {
        border: none;
        outline: none;
        width: 100%;
        background-color: var(--secondary-500);
        border-radius: 2rem 0 0 0;
        padding: 1.5rem 2rem;
    }
    input:focus {
        outline: 2px solid var(--accent);
    }
    .btn {
        border-radius: 0 0 2rem 0;
    }
}
</style>

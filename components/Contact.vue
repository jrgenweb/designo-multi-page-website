<template>
    <div>
        <section class="contact-section">
            <div>
                <h2>Let's talk about your project</h2>
                <p>
                    Ready to take it to the
                    next level? Contact us today and find out how our expertise can help your
                    business grow.
                </p>
            </div>
            <div>
                <a href="/about" class="btn-dark">Get in touch</a>
            </div>
        </section>
    </div>
</template>

<style scoped>
.contact-section {
    position: relative;
    bottom: calc(72px + 160px * -1);
    margin-block-start: -72px;

    background-color: var(--clr-primary-peach);
    background-image: url('../assets/img/shared/desktop/bg-pattern-call-to-action.svg');
    background-size: 70%;
    background-position: 340px;
    background-repeat: no-repeat;
    border-radius: 15px;

    display: flex;
    align-items: center;
    justify-content: space-between;
    padding: 72px 95px;

    div:first-child {
        width: 50%;
    }

}

div {}

h2 {
    line-height: 40px;
}

h2,
p {
    color: var(--clr-primary-white);

}

p {
    margin-top: 2rem;
}


@media screen and (max-width:1100px) {
    .contact-section {
        flex-direction: column;
        text-align: center;
        background-size: 150%;
        background-position: -150px;

        p {
            margin-bottom: 48px;
        }
    }


}
</style>
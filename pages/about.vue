<script setup>
useHead({
    title: 'Designo - About'
})
</script>
<template>
    <div>
        <header>
            <div>
                <h1>About Us</h1>
                <p>Founded in 2010, we are a creative agency that produces lasting results for our clients. We’ve partnered
                    with many startups, corporations, and nonprofits alike to craft designs that make real impact. We’re
                    always looking forward to creating brands, products, and digital experiences that connect with our
                    clients’ audiences.</p>
            </div>
            <NuxtImg src="../public/img/image-about-hero.jpg"></NuxtImg>
        </header>
        <section class="left-radius">
            <NuxtImg src="../public/img/image-world-class-talent.jpg"></NuxtImg>
            <div>
                <h2>World-class talent</h2>
                <p>We are a crew of strategists, problem-solvers, and technologists. Every design is thoughtfully crafted
                    from concept to launch, ensuring success in its given market. We are constantly updating our skills in a
                    myriad of platforms.
                </p>
                <p>
                    Our team is multi-disciplinary and we are not merely interested in form — content and meaning are just
                    as important. We give great importance to craftsmanship, service, and prompt delivery. Clients have
                    always been impressed with our high-quality outcomes that encapsulates their brand’s story and mission.
                </p>
            </div>

        </section>

        <Countries></Countries>




        <section class="right-radius">

            <div>
                <h2>The real deal</h2>
                <p>As strategic partners in our clients’ businesses, we are ready to take on any challenge as our own.
                    Solving real problems require empathy and collaboration, and we strive to bring a fresh perspective to
                    every opportunity. We make design and technology more accessible and give you tools to measure success.

                </p>
                <p>

                    We are visual storytellers in appealing and captivating ways. By combining business and marketing
                    strategies, we inspire audiences to take action and drive real results.
                </p>
            </div>
            <NuxtImg src="../public/img/image-real-deal.jpg"></NuxtImg>

        </section>
        <Contact></Contact>
    </div>
</template>


<style scoped>
header,
section {
    display: flex;
    border-radius: 15px;
    background-color: #FDF3F0;

    h2 {
        color: var(--clr-primary-peach);
    }

    div {
        padding: 95px;
        width: 60%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        gap: 1rem;
    }

    img {
        width: 600px;
    }
}

section.left-radius {
    img {
        border-top-left-radius: 15px;
        border-bottom-left-radius: 15px;
    }
}

section.right-radius {
    img {
        border-top-right-radius: 15px;
        border-bottom-right-radius: 15px;
    }

}

header {
    background-color: var(--clr-primary-peach);
    color: var(--clr-primary-white);

    img {

        border-top-right-radius: 15px;
        border-bottom-right-radius: 15px;
    }
}


@media screen and (max-width:1100px) {

    header,
    section.right-radius {
        flex-direction: column-reverse;
    }

    header,
    section.right-radius,
    section.left-radius {


        >img {
            width: 100%;
            height: 320px;
            object-fit: cover;
            border-bottom-right-radius: 0;
            border-bottom-left-radius: 0;
            border-top-left-radius: 15px;
            border-top-right-radius: 15px;
        }

        >div {
            text-align: center;
            width: 100%;
        }
    }

    section.left-radius {
        flex-direction: column;
    }


}
</style>
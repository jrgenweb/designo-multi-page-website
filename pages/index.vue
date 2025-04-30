<script setup>

</script>

<template>
    <div>
        <Hero></Hero>
        <ProjectSelector></ProjectSelector>
        <section>
            <div>
                <NuxtImg src="../public/img/illustration-passionate.svg" alt="Passionate illustration picture"></NuxtImg>
                <div>
                    <h3>Passionate</h3>
                    <p>Each project starts with an
                        in-depth brand research to ensure we only create products that serve a
                        purpose. We merge art, design, and technology into exciting new solutions.</p>
                </div>
            </div>
            <div>
                <NuxtImg src="../public/img/illustration-resourceful.svg" alt="Passionate illustration picture"></NuxtImg>
                <div>
                    <h3>Resourceful</h3>
                    <p>Everything that we do has a strategic purpose. We use an agile
                        approach in all of our projects and value customer collaboration. It
                        guarantees superior results that fulfill our clients’ needs.</p>
                </div>
            </div>
            <div>
                <NuxtImg src="../public/img/illustration-friendly.svg" alt="Passionate illustration picture"></NuxtImg>
                <div>
                    <h3> Friendly</h3>
                    <p>We are
                        a group of enthusiastic folks who know how to put people first. Our success
                        depends on our customers, and we strive to give them the best experience a
                        company can provide.</p>
                </div>
            </div>
        </section>

        <Contact></Contact>
    </div>
</template>

<style scoped>
section {
    display: flex;

    text-align: center;
    row-gap: 30px;

    >div {
        background-image: url('../assets/img/home/desktop/bg-pattern-hero-home.svg');
        background-size: 240px 240px;
        background-repeat: no-repeat;
        background-position: top center;
    }

}



/*flow */

img {
    margin-bottom: 48px;
    width: 200px;
    position: relative;
}



h3 {
    margin-bottom: 32px;
}



@media screen and (max-width:1100px) {
    section {
        flex-direction: column;

        img {
            width: 200px;
            height: 200px;
            margin-right: 40px;
            margin-bottom: 0;
        }

        >div {
            display: flex;
            background-position: top left;
            background-size: 200px 200px;
        }

        img+div {
            text-align: left;

            display: flex;
            flex-direction: column;
            justify-content: center;

        }
    }
}

@media screen and (max-width:7680px) {

    section {

        img {
            width: 200px;
            height: 200px;
            margin-right: 40px;
            margin-bottom: 0;
        }

        >div {
            flex-direction: column;
            align-items: center;
            background-position: top center;
            background-size: 200px 200px;
        }

        img+div {
            text-align: center;
        }
    }
}
</style>
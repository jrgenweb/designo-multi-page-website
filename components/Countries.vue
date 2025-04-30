<template>
    <div>

        <section class="countries">
            <div class="country">
                <NuxtImg width="200" src="../public/img/illustration-canada.svg"></NuxtImg>
                <p>CANADA</p>
                <a href="/locations" class="btn-light">see location</a>
            </div>
            <div class="country">
                <NuxtImg width="200" src="../public/img/illustration-australia.svg"></NuxtImg>
                <p>australia</p>
                <a href="/locations" class="btn-light">
                    see location</a>
            </div>
            <div class="country">
                <NuxtImg width="200" src="../public/img/illustration-united-kingdom.svg"></NuxtImg>
                <p>united kingdom</p><a href="/locations" class="btn-light">see location</a>
            </div>
        </section>
    </div>
</template>

<style scoped>
section {
    display: flex;
    padding-inline: 72px;

    justify-content: space-between;

    div>* {
        display: block;
        margin-inline: auto;
    }
}

.country {
    background-image: url(../assets/img/shared/desktop/bg-pattern-small-circle.svg);
    background-repeat: no-repeat;
    background-position: center 0;
}



p {
    text-transform: uppercase;
    font-size: 20px;

    text-align: center;


    /*flow*/
    margin-top: 48px;
    padding-bottom: 32px;
}

a {
    text-align: center;
}

@media screen and (max-width:1100px) {
    section {
        flex-direction: column;

        a {
            width: fit-content;

        }
    }

    .country:not(:last-child) {
        margin-bottom: 72px;
    }
}
</style>
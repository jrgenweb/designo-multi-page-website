<script setup>
const visible = ref(false)
</script>
<template>
    <div>
        <nav :class="visible ? 'active' : ''">
            <NuxtImg src="img/logo-dark.png" alt="Logo" sizes="180px sm:180px md:180px"></NuxtImg>
            <ul :class="visible ? 'active' : ''">
                <li><a href="/">Our company</a></li>
                <li><a href="/locations">Locations</a></li>
                <li><a href="/contact">Contact</a></li>
            </ul>
            <a href="#" id="menu" @click="visible = !visible">
                <img src="../assets/img/shared/mobile/icon-hamburger.svg" alt="" srcset="">
            </a>


        </nav>
    </div>
</template>


<style scoped>
nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 64px 0;
}

ul {
    display: inline;

}

ul li {
    display: inline-block;
    margin-left: 42px;
}

a {
    font-size: 14px;
    color: var(--clr-primary-black);
    letter-spacing: 2px;
    text-transform: uppercase;

    transition: 0.3s ease-in-out;
}

a:hover {
    text-decoration: underline;
}

#menu {
    display: none;
}


@media screen and (max-width:768px) {
    nav {
        height: 96px;
        background-color: var(--clr-primary-white);
        margin: 0;
        margin-inline: -24px;
        padding-inline: 24px;
        position: fixed;
        top: 0;
        z-index: 9999;
        width: 100%;

    }

    nav::after {
        content: '';
        width: 100%;
        height: 100vh;
        top: 96px;
        left: 0;
        position: fixed;
        background-color: rgba(0, 0, 0, 0.638);
        z-index: 2;
        visibility: hidden;
        opacity: 0;
        transition: 0.3s ease-in-out;

    }

    nav.active::after {

        opacity: 1;
        visibility: visible;
    }

    ul {
        position: absolute;
        bottom: -182px;
        left: 0px;
        width: 100%;
        padding-block: 2rem;

        background-color: var(--clr-primary-black);

        display: flex;
        flex-direction: column;
        gap: 1rem;
        z-index: 1000;
        visibility: hidden;
        transform: translateX(100vw);
        transition: 0.3s ease-in-out;

        a {
            color: var(--clr-primary-white);
            font-size: 24px;

        }
    }

    ul.active {
        visibility: visible;
        transform: translateX(0);
    }

    ul.active {}

    #menu {
        position: absolute;
        right: 24px;

        display: block;
    }



}
</style>
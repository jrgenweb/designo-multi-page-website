<script setup>
useHead({
    title: 'Designo - App Design'
})
</script>
<template>
    <div>

        <header :class="'contact-header'">
            <h2>App Design</h2>
            <p>
                Our mobile designs bring intuitive digital solutions
                to your customers right at their fingertips.
            </p>
        </header>

        <Projects></Projects>
        <ProjectSelector></ProjectSelector>
        <Contact></Contact>
    </div>
</template>  
<style scoped>
header {
    background-color: var(--clr-primary-peach);
    background-image: url('../assets/img/web-design/desktop/bg-pattern-intro-web.svg');
    background-size: 70%;
    background-position: 340px;
    background-repeat: no-repeat;
    border-radius: 15px;
    text-align: center;
    padding: 64px 95px;
}

h2,
p {
    color: var(--clr-primary-white);
}

p {
    margin-top: 2rem;
}

@media screen and (max-width:768px) {

    header {
        margin-inline: -24px;
        border-radius: 0;

        background-image: url('../assets/img/shared/desktop/bg-pattern-small-circle.svg');
        background-size: 38%;
        background-position: top right;
    }

}
</style>
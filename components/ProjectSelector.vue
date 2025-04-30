<script setup>
const router = useRouter()
/* const props = defineProps({
    selectors: Array
}) */

const path = router.currentRoute.value.path;
const projectSelectors = [
    {
        name: 'web design',
        image: '',
        route: '/webdesign'
    },
    {
        name: 'app design',
        route: '/appdesign'
    },
    {
        name: 'graphic design',
        route: '/graphicdesign'
    }
];


function getSelectors() {
    if (path === '/') {
        return projectSelectors;
    }
    return projectSelectors.filter(selector => {
        return selector.route != path;
    })
}




</script>

<template>
    <div>
        <section :class="path === '/' ? 'grid_three_layout' : 'grid_two_layout'">
            <NuxtLink :to="selector.route" :class="'project-selector ' + selector.route.substring(1)"
                v-for="selector in getSelectors()">

                <h2>{{ selector.name }}</h2>
                <p>view project</p>

            </NuxtLink>



        </section>
    </div>
</template>
<style scoped>
section {
    display: grid;
    gap: 30px;

    a {
        position: relative;

    }


    a {

        h2,
        p {
            position: relative;
            z-index: 2;
        }
    }

    a:hover {
        cursor: pointer;


    }

    a::after {

        content: '';
        inset: 0;
        background-color: var(--clr-primary-peach);
        opacity: 0;
        position: absolute;
        border-radius: 15px;
        transition: 0.3s ease-in-out;
    }

    a:hover::after {
        opacity: 0.7;
    }


}


.grid_three_layout,
.grid_two_layout {
    a {
        display: flex;
        align-items: center;
        justify-content: center;
        flex-direction: column;
        padding: 3.8rem;
        background-size: cover;
        border-radius: 15px;
    }
}

.grid_three_layout {

    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;

    height: 640px;



    a:nth-child(1) {
        grid-row: 1 / 3;
        grid-column: 1 / 2;
    }

    a:nth-child(2) {
        grid-row: 1 / 2;
        grid-column: 2 / 3;
    }

    a:nth-child(3) {
        grid-row: 2 / 3;
        grid-column: 2 / 3;
    }
}

.grid_two_layout {
    grid-template-columns: 50% 50%;
    grid-template-rows: 1fr;


    a:nth-child(1) {
        grid-row: 1 / 2;
        grid-column: 1 / 2;
        width: 100%;
    }

    a:nth-child(2) {
        grid-row: 1 / 2;
        grid-column: 2 / 3;
        width: 100%;
    }
}

.appdesign {
    background-image: url('../assets/img/home/desktop/image-app-design.jpg');
}

.grid_three_layout .webdesign {
    background-image: url('../assets/img/home/desktop/image-web-design-large.jpg');
}

.grid_two_layout .webdesign {
    background-image: url('../assets/img/home/desktop/image-web-design-small.jpg');
}

.graphicdesign {
    background-image: url('../assets/img/home/desktop/image-graphic-design.jpg');
}

h2,
p {
    color: var(--clr-primary-white);
    text-transform: uppercase;

}

p {
    letter-spacing: 5px;
    position: relative;
}

p::after {
    content: url('../assets/img/shared/desktop/icon-right-arrow.svg');
    position: absolute;
    top: 0;
    right: -16px;
}




@media screen and (max-width:1100px) {

    .grid_three_layout,
    .grid_two_layout {

        grid-template-columns: 1fr;
        grid-template-rows: 1fr 1fr 1fr;

        height: 640px;



        /**  */
        a:nth-child(1),
        a:nth-child(2),
        a:nth-child(3) {
            grid-row: auto;
            grid-column: 1;
        }


    }
}
</style>
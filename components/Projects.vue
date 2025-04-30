<script setup>
const router = useRoute();
const path = router.path;
const projectsData = {
    'webdesign': [
        {
            img: 'image-express.jpg',
            title: 'express',
            description: 'A multi-carrier shipping website for ecommerce businesses'
        },
        {
            img: 'image-transfer.jpg',
            title: 'transfer',
            description: 'Site for low-cost money transfers and sending money within seconds'
        },
        {
            img: 'image-photon.jpg',
            title: 'photon',
            description: 'A state-of-the-art music player with high-resolution audio and DSP effects'
        },
        {
            img: 'image-builder.jpg',
            title: 'builder',
            description: 'Connects users with local contractors based on their location'
        },
        {
            img: 'image-blogr.jpg',
            title: 'blogr',
            description: 'Blogr is a platform for creating an online blog or publication'
        },
        {
            img: 'image-camp.jpg',
            title: 'camp',
            description: 'Get expert training in coding, data, design, and digital marketing'
        },


    ],
    'appdesign': [
        {
            img: 'image-airfilter.jpg',
            title: 'airfilter',
            description: 'Solving the problem of poor indoor air quality by filtering the air'
        },
        {
            img: 'image-eyecam.jpg',
            title: 'eyecam',
            description: 'Product that lets you edit your favorite photos and videos at any time'
        },
        {
            img: 'image-faceit.jpg',
            title: 'faceit',
            description: 'Get to meet your favorite internet superstar with the faceit app'
        },
        {
            img: 'image-todo.jpg',
            title: 'todo',
            description: 'A todo app that features cloud sync with light and dark mode'
        },
        {
            img: 'image-loopstudios.jpg',
            title: 'loopstudios',
            description: 'A VR experience app made for Loopstudios'
        },

    ],
    'graphicdesign': [
        {
            img: 'image-change.jpg',
            title: 'tim brown',
            description: 'A book cover designed for Tim Brown’s new release, ‘Change’'
        },
        {
            img: 'image-boxed-water.jpg',
            title: 'boxed water',
            description: 'A simple packaging concept made for Boxed Water'
        },
        {
            img: 'image-science.jpg',
            title: 'science',
            description: 'A poster made in collaboration with the Federal Art Project'
        },

    ]
};

function getProjects() {
    return projectsData[path.substring(1)];
}

</script>


<template>
    <div>

        <section>

            <div class="card" v-for="project in getProjects()">
                <NuxtImg :src="'../public/img/' + project.img"></NuxtImg>
                <div>
                    <h3>{{ project.title }}</h3>
                    <p>{{ project.description }}</p>
                </div>
            </div>



        </section>

    </div>
</template>

<style scoped>
section {
    --br-radius: 15px;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: auto;
    gap: 32px;
}

.card {
    border-radius: var(--br-radius);
    background-color: #FDF3F0;
    text-align: center;
    transition: 0.3s ease-in-out;
}

.card:hover {
    cursor: pointer;
    background-color: var(--clr-primary-peach);

    h3,
    p {
        color: var(--clr-primary-white);
    }
}

h3 {
    color: var(--clr-primary-peach);
    padding-top: 32px;
}


p {
    padding: 16px 32px 32px 32px;
}

img {
    width: 100%;
    border-top-right-radius: var(--br-radius);
    border-top-left-radius: var(--br-radius);
}


@media screen and (max-width:1100px) {
    img {
        width: 50%;
        border-top-right-radius: 0;
        border-top-left-radius: var(--br-radius);
        border-bottom-left-radius: var(--br-radius);
    }

    section {
        grid-template-columns: 1fr;
    }

    .card {
        display: flex;

        >div {
            display: flex;
            flex-direction: column;
            justify-content: center;
        }
    }
}

@media screen and (max-width:1100px) {
    .card {
        flex-direction: column;

    }

    img {
        width: 100%;
        border-top-right-radius: var(--br-radius);
        border-top-left-radius: var(--br-radius);
        border-bottom-left-radius: 0;
    }
}
</style>
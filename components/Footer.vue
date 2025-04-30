<template>
    <div>
        <footer>
            <div class="container">
                <nav>
                    <NuxtImg src="img/logo-light.png" alt="Logo" sizes="180px sm:180px md:180px"></NuxtImg>

                    <ul>
                        <li><a href="/">Our company</a></li>
                        <li><a href="/locations">Locations</a></li>
                        <li><a href="/contact">Contact</a></li>
                    </ul>

                </nav>
                <hr>
                <div>
                    <ul>
                        <li>Designo Central Office</li>
                        <li>3886 Wellington Street</li>
                        <li>Toronto, Ontario M9C 3J5</li>
                    </ul>
                    <ul>
                        <li>Contact Us (Central)</li>
                        <li>P : +1 253-863-8967</li>
                        <li>M : contact@designo.co</li>
                    </ul>

                    <ul class="social-links">
                        <li><a href="/">
                                <NuxtImg src="../public/img/icon-facebook.svg" width="24" height="24"></NuxtImg>
                            </a></li>
                        <li><a href="/">
                                <NuxtImg src="../public/img/icon-youtube.svg" width="24" height="24"></NuxtImg>
                            </a></li>
                        <li><a href="/">
                                <NuxtImg src="../public/img/icon-twitter.svg" width="24" height="24"></NuxtImg>
                            </a></li>
                        <li><a href="/">
                                <NuxtImg src="../public/img/icon-pinterest.svg" width="24" height="24"></NuxtImg>
                            </a></li>
                        <li><a href="/">
                                <NuxtImg src="../public/img/icon-instagram.svg" width="24" height="24"></NuxtImg>
                            </a></li>

                    </ul>
                </div>
            </div>
        </footer>

    </div>
</template>


<style scoped>
.container {
    max-width: 1190px;
    padding-inline: 40px;
    margin-inline: auto;
}

footer {
    background-color: var(--clr-primary-black);
    color: var(--clr-primary-white);
    padding-top: 145px;
    padding-bottom: 72px;
}

nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 64px 0;
}

nav ul {
    display: inline;

}

nav ul li {
    display: inline-block;
    margin-left: 42px;

}

nav ul li a {
    font-size: 14px;
    color: var(--clr-primary-white);
    letter-spacing: 2px;
    text-transform: uppercase;
}

nav ul li a:hover {
    text-decoration: underline;
}



hr {
    margin-block: 40px;
    height: 1px;
    background-color: var(--clr-primary-white);
    border: 0;
}

hr+div {
    display: flex;
    justify-content: flex-start;
    align-items: flex-end;
    position: relative;

    ul {
        width: 350px;
    }
}



hr+div ul:not(.social-links) {
    opacity: 0.535;
}

hr+div ul:nth-child(1) li:first-child {
    font-weight: bold;
}

hr+div ul:nth-child(2) {
    font-weight: bold;
}

.social-links {
    margin-inline-start: 60px;
    text-align: right;
}



.social-links li {
    display: inline-block;
    margin-left: 1rem;

}


@media screen and (max-width:768px) {
    .container {
        display: flex;
        flex-direction: column;



        >nav {
            flex-direction: column;



            >ul {
                display: flex;
                flex-direction: column;
                align-items: center;
                gap: 2rem;

                margin-top: 72px;

                width: 100%;
                position: relative;

                li {


                    padding: 0;
                    margin: 0;
                }


            }

            ul::before {
                content: '';
                width: 100%;
                height: 1px;
                background-color: var(--clr-primary-white);
                opacity: 0.1;
                position: absolute;
                top: -36px;

            }
        }

        hr {
            display: none;
        }

        >div {


            flex-direction: column;
            align-items: center;

            ul:not(.social-links) {
                display: flex;
                flex-direction: column;

                align-items: center;
                margin-bottom: 40px;

            }


            .social-links {
                margin: 0;

                text-align: center;
                margin-inline-start: auto;
                margin-inline-end: auto;
                width: auto;
            }
        }

    }
}
</style>
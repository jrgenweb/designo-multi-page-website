<template>
    <div>
        <header>
            <div>
                <h1> Award-winning custom designs and digital branding solutions</h1>
                <p>
                    With over 10 years in the industry, we are experienced in creating fully responsive websites, app
                    design,
                    and engaging brand experiences. Find out more about our services.
                </p>
                <a href="/" class="btn-dark">Learn more</a>

            </div>

        </header>
    </div>
</template>


<style scoped>
header {
    background-image: url('../assets/img/home/desktop/bg-pattern-hero-home.svg'), url('../assets/img/home/desktop/image-hero-phone.png');
    display: flex;
    background-repeat: no-repeat;
    background-position: top right;
    background-color: var(--clr-primary-peach);
    border-radius: 15px;
    color: white;

    >div {
        padding: 145px 95px;
        max-width: 65%;



    }
}

/* flow */
h1,
p {
    margin-bottom: 34px;

}


@media screen and (max-width:1100px) {
    header {
        background-position: 140% 100px, center 300px;

        >div {
            padding: 60px;
            max-width: 100%;
            text-align: center;
            padding-bottom: 450px;
        }
    }
}


@media screen and (max-width:768px) {
    header {


        margin-inline: -24px;
        border-radius: 0;
        background-position: 140% 100px, center 300px;

        >div {
            padding: 60px;
            max-width: 100%;
            text-align: center;
            padding-bottom: 450px;
        }
    }
}
</style>
<script setup>
useHead({
    title: 'Designo - Contact'
})
</script>
<template>
    <div>
        <header class="header-contact">
            <div>
                <h1>Contat Us</h1>
                <p>
                    Ready to take it to the next level? Let’s talk about your project or idea and find out how we can help
                    your business grow. If you are looking for unique digital experiences that’s relatable to your users,
                    drop us a line.
                </p>
            </div>
            <div>
                <div class="form-control">
                    <label for="name">Name</label>
                    <input type="text" name="name" id="name" placeholder="Name">
                </div>
                <div class="form-control">
                    <label for="email">Email Address</label>
                    <input type="email" name="email" id="email" placeholder="Name">
                </div>
                <div class="form-control">
                    <label for="phone">Phone</label>
                    <input type="number" name="phone" id="phone" placeholder="Name">
                </div>
                <div class="form-control">
                    <label for="message">Your Message</label>
                    <textarea name="message" id="message" cols="30" rows="10" placeholder="Your Message"></textarea>
                </div>
                <button class="btn-dark">Submit</button>
            </div>
        </header>

        <Countries></Countries>
    </div>
</template>

<style scoped>
.header-contact {
    background-color: var(--clr-primary-peach);
    background-image: url(../assets/img/contact/desktop/bg-pattern-hero-desktop.svg);
    background-position: bottom left;
    background-repeat: no-repeat;
    border-radius: 15px;
    padding: 55px 95px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 95px;
    color: var(--clr-primary-white);




    >div:first-child {
        display: flex;
        flex-direction: column;
        justify-content: center;

        h1 {
            margin-bottom: 32px;
        }
    }

    >div:last-child {}
}





.form-control {
    display: flex;

    position: relative;
    margin-bottom: 1.5rem;
}

label {
    position: absolute;
    opacity: 0.5;
    cursor: pointer;
    transition: 0.3s ease-in-out;
}


input,
textarea {
    background: transparent;
    width: 100%;
    padding: 12px 16px;
    border: 0;
    outline: 0;
    border-bottom: 1px solid var(--clr-primary-white);
    font-size: 15px;
    font-weight: bold;
    color: var(--clr-primary-white);

    transition: 0.3s ease-in-out;
}

input:hover,
textarea:hover {
    cursor: pointer;
    box-shadow: 0px 2px 0px white;
}

label:has(+input:focus),
label:has(+input:not(:placeholder-shown)),
label:has(+textarea:focus),
label:has(+textarea:not(:placeholder-shown)) {
    font-size: 0.75rem;
    transform: translateY(-1rem);
    opacity: 1;
}


label:has(+input:hover),
label:has(+textarea:hover) {
    opacity: 1;
}



input::placeholder,
textarea::placeholder {
    color: transparent;
}

button {
    float: right;

}



@media screen and (max-width:1100px) {

    .header-contact {
        grid-template-columns: 1fr;
        padding: 70px 58px;


        >div {

            grid-row: auto;
        }
    }
}


@media screen and (max-width:768px) {

    .header-contact {
        grid-template-columns: 1fr;
        padding: 70px 58px;
        margin-inline: -24px;
        border-radius: 0;
        padding-top: 96px;


        >div {

            grid-row: auto;
        }
    }
}
</style>
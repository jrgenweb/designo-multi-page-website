<script setup>
useHead({
    title: 'Designo - Locations'
})
</script>
<template>
    <div>

        <div class="locations">
            <section class="location">
                <div class="description">
                    <h2>Canada</h2>
                    <div>
                        <ul>
                            <li>Designo Central Office</li>
                            <li>
                                3886 Wellington Street </li>
                            <li>Toronto, Ontario M9C 3J5</li>
                        </ul>
                        <ul>
                            <li>Contact
                            </li>
                            <li>
                                P : +1 253-863-8967</li>
                            <li>M : contact@designo.co</li>
                        </ul>
                    </div>
                </div>

                <LMap style="height: 350px" :zoom="10" :center="[43.6460885, -79.3955164]" :use-global-leaflet="false"
                    class="map">
                    <LTileLayer url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
                        attribution="&amp;copy; <a href=&quot;https://www.openstreetmap.org/&quot;>OpenStreetMap</a> contributors"
                        layer-type="base" name="OpenStreetMap" />
                </LMap>

            </section>
            <section class="location">

                <LMap style="height: 350px" :zoom="6" :center="[47.21322, -1.559482]" :use-global-leaflet="false"
                    class="map">
                    <LTileLayer url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
                        attribution="&amp;copy; <a href=&quot;https://www.openstreetmap.org/&quot;>OpenStreetMap</a> contributors"
                        layer-type="base" name="OpenStreetMap" />
                </LMap>

                <div class="description">
                    <h2>Australia</h2>
                    <div>
                        <ul>
                            <li>Designo AU Office</li>
                            <li>

                                19 Balonne Street </li>
                            <li>New South Wales 2443</li>
                        </ul>
                        <ul>
                            <li>Contact
                            </li>
                            <li>
                                P : (02) 6720 9092</li>
                            <li>M : contact@designo.au</li>
                        </ul>
                    </div>
                </div>

            </section>

            <section class="location">
                <div class="description">
                    <h2>United Kingdom</h2>
                    <div>
                        <ul>
                            <li>Designo UK Office</li>
                            <li>
                                13 Colorado Way </li>
                            <li>Rhyd-y-fro SA8 9GA</li>
                        </ul>
                        <ul>
                            <li>Contact
                            </li>
                            <li>
                                P : 078 3115 1400</li>
                            <li>M : contact@designo.uk</li>
                        </ul>
                    </div>
                </div>

                <LMap style="height: 350px;" :zoom="6" :center="[43.21322, -1.559482]" :use-global-leaflet="false"
                    class="map">
                    <LTileLayer url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
                        attribution="&amp;copy; <a href=&quot;https://www.openstreetmap.org/&quot;>OpenStreetMap</a> contributors"
                        layer-type="base" name="OpenStreetMap" />
                </LMap>

            </section>

        </div>

        <Contact></Contact>
    </div>
</template>



<style scoped>
h2 {
    color: var(--clr-primary-peach);

    margin-bottom: 24px;
}

.location {
    display: flex;
    flex-direction: row;
    gap: 30px;

    .description {
        border-radius: 15px;
        width: 100%;
        background-color: #FDF3F0;
        padding: 88px 95px;
        background-image: url(../assets/img/shared/desktop/bg-pattern-two-circles.svg);
        background-position: bottom left;
        background-repeat: no-repeat;



        ul {
            display: inline-block;
            width: 255px;

            li:first-child {
                font-weight: bold;
            }

        }

    }


}

.map {
    border-radius: 15px;
    overflow: hidden;
    max-width: 350px;

}

@media screen and (max-width:1100px) {
    .location:nth-child(2) {
        flex-direction: column;
    }

    .location:nth-child(1),
    .location:nth-child(3) {
        flex-direction: column-reverse;
    }


    .map {
        max-width: 100% !important;


    }
}


@media screen and (max-width:768px) {
    .location {
        margin-inline: -24px;
        gap: 0;

        .map,
        .description {
            border-radius: 0;
        }

        .description {
            background-image: url(../assets/img/shared/desktop/bg-pattern-small-circle.svg);
            background-size: 65%;
            background-position: center center;

            text-align: center;
        }
    }

}
</style>
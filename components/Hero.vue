<template>
    <section class="c-hero">
        <div class="c-hero__content" v-if="typeHero === 'homepage'">
            <video autoplay class="c-hero__video">
                <source src="sport-health-intro.webm" type="video/webm">
                <source src="sport-health-intro.mp4" type="video/mp4">
            </video>
            <div class="c-hero__overlay flex flex-col items-center justify-center">
                <figure class="mb-8">
                    <img class="c-hero__logo" src="logo-sporthealth.png" alt="Sport Health Logo" />
                </figure>
                <p class="px-4 text-center w-1/2">Solo con un approccio multidisciplinare è possibile curare davvero il paziente e farlo tornare a condurre una vita piena e soddisfacente.<br>
                <span>(Riccardo Torquati)</span></p>
                <div class="c-hero_cta">
                    <button class="o-button o-button--hero">
                        <nuxt-link to="/centri-sporthealth">Scegli il centro più vicino a te</nuxt-link>
                    </button>
                    <button class="o-button o-button--hero-alt">
                        <nuxt-link to="/centri-sporthealth">Prenota una valutazione specialistica</nuxt-link>
                    </button>
                </div>
            </div>
        </div>

        <div class="c-hero__content" v-else-if="typeHero === 'basic'">
            <h1>Content without video</h1>
        </div>

        <div class="c-hero__content" v-else>
            <h1>Splitted content</h1>
        </div>
    </section>
</template>
<template v-else-if="hero === 'full'">
    <h1>Hero with full width</h1>
</template>
<template v-else>
    <h1>Hero for other page</h1>
</template>
<script>
    export default {
        props: {
            typeHero: {
                type: String
            }
        }
    }
</script>
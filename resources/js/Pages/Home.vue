<template>

    <Header />

    <div class="u-container">

        <div class="c-presentation">

            <div class="c-presentation-wrapper">

                <h1 class="c-presentation__title">
                    Olá, sou o Yuri, um desenvolvedor Full Stack
                    com paixão por aprender
                </h1>

                <ul class="c-presentation__list">
                    <li class="c-presentation__item">
                        Experiência em <strong class="c-presentation__highlight">Front-end</strong> e <strong class="c-presentation__highlight">Back-end</strong>
                    </li>
                    <li class="c-presentation__item">
                        Design web <strong class="c-presentation__highlight">responsivo</strong>
                    </li>
                    <li class="c-presentation__item">
                        Desenvolvedor Full Stack na <a href="https://rgb.com.br" class="c-presentation__highlight">RGB Comunicação</a>
                    </li>
                    <li class="c-presentation__item">
                        Formado em <strong class="c-presentation__highlight">Análise e Desenvolvimento de Sistemas</strong>
                    </li>
                </ul>


            </div>

            <img src="images/presentation.gif" alt="3D Example" class="c-presentation__image">

        </div>

    </div>

    <CardList :cards="cards" />

</template>

<script setup>

import Header from '../Components/Header.vue';
import CardList from '../Components/CardList.vue'

const cards = [
    {
        image: 'images/duolingo.webp',
        title: 'Duolingo',
        description: "Launched multiple designs that enhanced Super Duolingo's subscription metrics",
        tags: [
            {
                name: 'Product Designer'
            }
        ]
    }
];

</script>

<style scoped>

.c-presentation {
    width: 100%;
    display: grid;
    grid-template-columns: 1.4fr 1fr;
    align-items: center;
    gap: 2rem;
    padding: 4rem 0;

    .c-presentation-wrapper {
        
        .c-presentation__title {
            margin-bottom: var(--space-xl);
            font-weight: 500;
            font-size: var(--gb-font-size-xl);
            line-height: 3.4rem;
        }

        .c-presentation__list {
            .c-presentation__item {
                font-weight: 400;
                margin-bottom: var(--space-sm);
                font-size: var(--gb-font-size-md);
                color: rgba(var(--color-gray), .7);

                .c-presentation__highlight {
                    color: black;
                }
            }
        }
    }

    .c-presentation__image {
        width: 100%;
    }

}

</style>
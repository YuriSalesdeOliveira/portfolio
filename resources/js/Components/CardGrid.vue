<template>
    <section class="c-card-grid" :style="{ backgroundColor }">

        <div class="u-container">

            <h3 class="c-card-grid__title">{{ title }}</h3>
            <p class="c-card-grid__subtitle" v-if="subtitle">{{ subtitle }}</p>

            <div class="c-card-grid__wrapper" :style="{ gridTemplateColumns: `repeat(${columns}, 1fr)` }">

                <figure class="c-card-grid__card" v-for="card of cards">

                    <img :src="card.image" :alt="card.title" class="c-card-grid__image">

                    <figcaption class="c-card-grid__text">

                        <h4 class="c-card-grid__card-title">{{ card.title }}</h4>

                        <span class="c-card-grid__tag" v-for="tag of card.tags">{{ tag.name }}</span>
                        
                        <p class="c-card-grid__description">{{ card.description }}</p>

                    </figcaption>

                </figure>

            </div>

        </div>

    </section>
</template>

<script setup>

import { ref } from 'vue';

const props = defineProps({
    title: String,
    subtitle: String,
    cards: Array,
    columns: {
        type: Number,
        default: 3
    },
    backgroundColor: {
        type: String,
        default: 'rgb(var(--color-overlay-primary))'
    }
});

</script>

<style scoped>
.c-card-grid {
    width: 100%;
    padding: var(--space-xl) 0;

    &:not(:has(.c-card-grid__subtitle)) {
        .c-card-grid__title {
            margin-bottom: var(--space-xl);
        }
    }

    .c-card-grid__title {
        margin-bottom: var(--space-xs);
        font-weight: 500;
        font-size: var(--gb-font-size-xl);
        line-height: 3.4rem;
    }

    .c-card-grid__subtitle {
        margin-bottom: var(--space-xl);
        font-weight: 300;
        font-size: var(--gb-font-size-md);
        text-shadow: 0 0 0 rgba(var(--color-text-secondary), .6);
        color: rgba(var(--color-text-secondary), .6);
    }

    .c-card-grid__wrapper {
        display: grid;
        gap: 4rem;

        .c-card-grid__card {
            width: 100%;

            .c-card-grid__image {
                width: 100%;
                object-fit: cover;
                margin-bottom: var(--space-lg);
            }
    
            .c-card-grid__text {
                display: flex;
                flex-direction: column;
                gap: var(--space-md);
    
                .c-card-grid__card-title {
                    font-weight: 500;
                    font-size: var(--gb-font-size-lg);
                }
    
                .c-card-grid__tag {
                    font-weight: 300;
                    font-size: var(--gb-font-size-sm);
                    color: rgba(var(--color-text-secondary), .8);
                }
    
                .c-card-grid__description {
                    font-size: var(--gb-font-size-sm);
                    line-height: var(--gb-font-size-lg);
                }
            }
        }
    }
}
</style>
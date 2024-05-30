<template>

    <footer class="l-footer">

        <div class="u-container">

            <div class="l-footer__wrapper">

                <div class="l-footer__thank-you">

                    <p class="l-footer__phrase">Nice to see you here!</p>

                    <a href="mailto:yusadeol@gmail.com" class="l-footer__link">yusadeol@gmail.com</a>

                    <p class="l-footer__paragraph">Made with love © 2024 Yuri Sales de Oliveira</p>

                </div>

                <div class="l-footer__contacts">

                    <nav class="l-footer__menu">

                        <menu class="l-footer__list">

                            <li class="l-footer__item">
                                <a href="mailto:yusadeol@gmail.com">
                                    Email
                                </a>
                            </li>

                            <li class="l-footer__item">
                                <a href="https://www.linkedin.com/in/yuri-sales-de-oliveira/" target="_blank">
                                    LinkedIn
                                </a>
                            </li>

                            <li class="l-footer__item">
                                <a href="https://github.com/YuriSalesdeOliveira" target="_blank">
                                    Github
                                </a>
                            </li>

                        </menu>

                    </nav>

                </div>

            </div>

        </div>

    </footer>

</template>

<script setup>
</script>

<style scoped>
.l-footer {
    padding: calc(var(--space-xl) * 2) 0;
    font-size: var(--gb-font-size-sm);
    color: rgb(var(--color-text-tertiary));
    background-color: rgb(var(--color-overlay-secondary));

    .l-footer__wrapper {
        display: flex;
        justify-content: space-between;
        align-items: end;

        .l-footer__thank-you {

            .l-footer__phrase {
                margin-bottom: var(--space-xl);
                font-weight: 500;
                font-size: var(--gb-font-size-xl);
                line-height: 3.4rem;
                color: white;
            }

            .l-footer__link {
                display: block;
                margin-bottom: var(--space-sm);
            }

            .l-footer__paragraph {
                display: block;
                margin-bottom: var(--space-sm);
            }
        }

        .l-footer__contacts {

            .l-footer__menu {

                .l-footer__list {
                    display: flex;
                    gap: 4rem;

                    .l-footer__item {
                        transition: all linear .2s;

                        &:hover {
                            color: white;
                        }
                    }
                }
            }
        }

    }
}
</style>
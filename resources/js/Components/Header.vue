<template>

    <header class="l-header">
        
        <div class="l-header__logo">
            <a :href="route('home')" aria-label="Home Page" class="l-header__link">
                Yuri Oliveira
            </a>
        </div>

        <nav class="l-header__menu">

            <menu class="l-header__list">

                <li class="l-header__item --active">
                    <a href="">
                        Trabalho
                    </a>
                </li>

                <li class="l-header__item">
                    <a href="">
                        Veja
                    </a>
                </li>

                <li class="l-header__item">
                    <a href="">
                        Sobre
                    </a>
                </li>

                <li class="l-header__item">
                    <a href="">
                        Resumo
                    </a>
                </li>

            </menu>

        </nav>

    </header>
    
</template>

<style scoped>

.l-header {
    width: 100%;
    height: 15rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 8rem;

    .l-header__logo {
        .l-header__link {
            font-weight: 500;
            font-size: var(--gb-font-size-xl);
            color: rgb(var(--color-text-primary));
        }
    }

    .l-header__menu {
        .l-header__list {
            display: flex;
            gap: 2.8rem;

            .l-header__item {
                font-size: var(--gb-font-size-md);
                color: rgba(var(--color-text-secondary), .7);

                transition: all linear .2s;

                &.--active {
                    color: rgb(var(--color-text-primary));
                }

                &:hover {
                    color: rgb(var(--color-text-primary));
                }
            }
        }
    }
}

</style>
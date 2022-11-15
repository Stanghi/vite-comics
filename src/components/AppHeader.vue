<script>
export default {
    name: 'AppHeader',
    data() {
        return {
            menu: [
                {
                    text: 'Characters',
                    href: '#',
                    current: false,
                },
                {
                    text: 'Comics',
                    href: '#',
                    current: true,
                },
                {
                    text: 'Movies',
                    href: '#',
                    current: false,
                },
                {
                    text: 'Tv',
                    href: '#',
                    current: false,
                },
                {
                    text: 'Games',
                    href: '#',
                    current: false,
                },
                {
                    text: 'Collectibles',
                    href: '#',
                    current: false,
                },
                {
                    text: 'Videos',
                    href: '#',
                    current: false,
                },
                {
                    text: 'Fans',
                    href: '#',
                    current: false,
                },
                {
                    text: 'News',
                    href: '#',
                    current: false,
                },
                {
                    text: 'Shop',
                    href: '#',
                    current: false,
                },
            ],
        };
    },
};
</script>

<template>
    <header>
        <div class="container">
            <img src="/dc-logo.png" alt="DC logo" />
            <nav>
                <ul>
                    <li v-for="(link, index) in menu" :key="index">
                        <a :href="link.href" :class="link.current && 'active'">{{ link.text }}</a>
                    </li>
                </ul>
            </nav>
        </div>
    </header>
</template>

<style lang="scss" scoped>
@use '../style/partial/variables' as *;

header {
    line-height: 120px;
    background-color: $header-color;
}

.container {
    display: flex;
    justify-content: space-between;
    align-items: center;

    img {
        width: 80px;
    }

    ul {
        display: flex;
        list-style: none;

        li {
            display: flex;
            margin: 0 10px 0 10px;

            a {
                font-size: 0.75rem;
                font-weight: bolder;
                text-transform: uppercase;
                text-decoration: none;
                color: $dark;
                &:hover {
                    color: $dc-blue;
                }
                &.active {
                    color: $dc-blue;
                    border-bottom: 5px solid $dc-blue;
                }
            }
        }
    }
}
</style>

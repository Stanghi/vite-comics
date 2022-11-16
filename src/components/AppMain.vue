<script>
import CardSeries from './CardSeries.vue';
import seriesDataBase from '../data/dc-comics.js';

export default {
    name: 'AppMain',
    components: {
        CardSeries,
    },
    data() {
        return {
            seriesDataBase,
        };
    },
};
</script>

<template>
    <main>
        <div class="jumbotron"></div>
        <div class="container">
            <div class="current-serie">
                <p>Current series</p>
            </div>
            <CardSeries v-for="(serie, index) in seriesDataBase" :key="index" :serie="serie" />
            <div>
                <button>Load more</button>
            </div>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../style/partial/variables' as *;

main {
    background-color: $dark;

    .jumbotron {
        height: 400px;
        background-size: cover;
        background-repeat: no-repeat;
        background-image: url(../assets/img/jumbotron.jpg);
        margin-bottom: 55px;
    }
    .container {
        position: relative;
        display: flex;
        flex-wrap: wrap;

        .current-serie {
            position: absolute;
            display: flex;
            justify-content: center;
            align-items: center;
            top: -80px;
            width: 250px;
            height: 50px;
            background-color: $dc-blue;

            p {
                text-transform: uppercase;
                font-size: 1.4rem;
                color: $text-white;
                font-weight: bold;
            }
        }

        & div:last-child {
            display: flex;
            justify-content: center;
            width: 100%;

            button {
                cursor: pointer;
                text-transform: uppercase;
                margin-bottom: 20px;
                font-weight: bold;
                font-size: 0.7rem;
                color: $text-white;
                width: 180px;
                height: 35px;
                border: none;
                background-color: $dc-blue;
            }
        }
    }
}
</style>

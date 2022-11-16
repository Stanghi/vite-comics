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
        <div class="container">
            <CardSeries v-for="(serie, index) in seriesDataBase" :key="index" :serie="serie" />
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../style/partial/variables' as *;

main {
    background-color: $dark;

    .container {
        display: flex;
        flex-wrap: wrap;
    }
}
</style>

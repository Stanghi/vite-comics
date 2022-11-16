<script>
export default {
    name: 'CardSeries',
    props: {
        serie: Object,
    },
};
</script>

<template>
    <div class="card">
        <div class="thumb">
            <img :src="serie.thumb" alt="serie.series" />
        </div>
        <p>{{ serie.series }}</p>
    </div>
</template>

<style lang="scss" scoped>
@use '../style/partial/variables' as *;

.card {
    overflow-wrap: break-word;
    inline-size: 209px;
    padding: 12px;

    .thumb {
        overflow: hidden;
        width: 185px;
        height: 185px;
        margin-bottom: 15px;

        img {
            width: 100%;
        }
    }

    p {
        font-size: 0.9rem;
        text-transform: uppercase;
        color: $text-white;
    }
}
</style>

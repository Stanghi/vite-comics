<script>
export default {
    name: 'AppMain',
};
</script>

<template>
    <main>
        <div class="container">
            <p>Content goes here</p>
        </div>
    </main>
</template>

<style lang="scss" scoped>
@use '../style/partial/variables' as *;

main {
    padding: 60px;
    color: $text-white;
    background-color: $dark;

    p {
        font-size: 1.8rem;
    }
}
</style>

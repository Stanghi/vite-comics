<script>
import AppHeader from './components/AppHeader.vue';
import AppMain from './components/AppMain.vue';
import AppFooter from './components/AppFooter.vue';
import AppBlueBand from './components/AppBlueBand.vue';

export default {
    name: 'App',
    components: {
        AppHeader,
        AppMain,
        AppFooter,
        AppBlueBand,
    },
};
</script>

<template>
    <AppHeader />
    <AppMain />
    <AppBlueBand />
    <AppFooter />
</template>

<style lang="scss">
@use './style/general';
</style>

<template>
    <div>
        <app-toolbar></app-toolbar>
        <app-footer></app-footer>
    </div>
</template>

<script>
    import AppFooter from './AppFooter'
    import AppToolbar from './AppToolbar'

    export default {
        name: "AppHome",
        components: {
            AppFooter, AppToolbar
        }
    }
</script>

<style scoped>

</style>
<template>
    <div id="app">
        <app-toolbar></app-toolbar>
        <app-footer style="position: absolute; z-index: -1"></app-footer>
        <router-view/>
    </div>
</template>

<script>
    import AppFooter from './components/AppFooter'
    import AppToolbar from './components/AppToolbar'

    export default {
        name: 'App',
        components: {
            AppFooter, AppToolbar
        }

    }
</script>

<style>
    #app {
        font-family: 'Avenir', Helvetica, Arial, sans-serif;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        text-align: center;
        color: #2c3e50;
    }
</style>

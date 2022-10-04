<template>
    <div class="content">
       <AppHeader :title="title"/> 
    </div>
</template>

<script>
    import AppHeader from './AppHeader.vue';
    export default {
    name: "App",
    data() {
        return {
            title: "Boolpress"
        };
    },
    components: { AppHeader }
};
</script>
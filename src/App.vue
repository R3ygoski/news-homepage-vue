<script setup>
    import HeaderComponent from './components/HeaderComponent.vue'
    import MainArticleComponent from './components/MainArticleComponent.vue'
    import SidebarComponent from './components/SidebarComponent.vue'
    import FooterArticleComponent from './components/FooterArticleComponent.vue'
    import AttributionComponent from './components/AttributionComponent.vue'
</script>

<template>
    <main class="page">
        <HeaderComponent/>
        <MainArticleComponent/>
        <SidebarComponent/>
        <FooterArticleComponent/>
    </main>
    <AttributionComponent/>
</template>
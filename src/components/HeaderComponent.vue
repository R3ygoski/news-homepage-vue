<script setup>
    import { ref, onMounted } from 'vue'

    const links = [
        { id: 1, link: '#', name: 'Home', },
        { id: 2, link: '#', name: 'New', },
        { id: 3, link: '#', name: 'Popular', },
        { id: 4, link: '#', name: 'Trending', },
        { id: 5, link: '#', name: 'Categories', },
    ]

    let isMenuOpen = ref(false)
    let windowDesktop = ref(false)
    let windowWidth = ref(window.innerWidth)

    const updateWidth = () => {
        windowWidth.value = window.innerWidth
        if (windowWidth.value >= 1024){
            windowDesktop.value = true
        } else {
            windowDesktop.value = false
        }
    }
    const clickHandler = () => {
        isMenuOpen.value = !isMenuOpen.value
    }
    onMounted(() => {
        updateWidth()
        window.addEventListener('resize', updateWidth)
    })

</script>
<template>
    <header id="header" class="header">
        <img class="header__logo" src="../assets/images/logo.svg" alt=""/>
        <nav :class="isMenuOpen == true || windowDesktop == true?'header__nav':'header__nav--hidden'">
            <ul>
                <li v-for="link in links" :key="link.id">
                    <a :href="link.link">{{ link.name }}</a>
                </li>
            </ul>
        </nav>
        <button v-if="windowDesktop == false" class="header__menu" type="button" role="menu" aria-label="hamburguer menu" @click="clickHandler">
            <img v-if="isMenuOpen == false && windowDesktop == false " src="../assets/images/icon-menu.svg" alt="Hamburguer Menu"/>
            <img v-else class="header__menu-close" src="../assets/images/icon-menu-close.svg" alt="Hamburguer Menu"/>
        </button>
    </header>
</template>
<script setup>
    // Images
    import retroPc from '../assets/images/image-retro-pcs.jpg'
    import keyboard from '../assets/images/image-top-laptops.jpg'
    import joystick from '../assets/images/image-gaming-growth.jpg'

    const footerArticles = [
        {
            id: 1,
            number: '01',
            title: 'Reviving Retro PCs',
            desc: 'What happens when old PCs are given modern upgrades?',
            img: retroPc,
            alt: 'Three Retro PC'
        },
        {
            id: 2,
            number: '02',
            title: 'Top 10 Laptops of 2022',
            desc: 'Our best picks for various need and budgets.',
            img: keyboard,
            alt: 'A Gamer Keyboard'
        },
        {
            id: 3,
            number: '03',
            title: 'The Growth of Gaming',
            desc: 'How the pandemic has sparked fresh opportunities.',
            img: joystick,
            alt: 'A PlayStration 4 Joystick falling in a Hand'
        },
    ]
</script>
<template>
    <footer id="footer" class="footer">
        <article class="footer__article" v-for="article in footerArticles" :key="article.id">
            <img :src="article.img" :alt="article.alt" />
            <h3>{{ article.number }}</h3>
            <h4>{{ article.title }}</h4>
            <p>{{ article.desc }}</p>
        </article>
    </footer>
</template>
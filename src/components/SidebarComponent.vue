<script setup>
    const sidebarArticles = [
        {   id: 1, 
            title: 'Hydrogen VS Eletric Cars', 
            desc: 'Will hydrogen-fueled cars ever catch up to EVs?',
            link: '#',
        },
        {   id: 2, 
            title: 'The Downsides of AI Artistry', 
            desc: 'What are the possible adverse effects of on-demand AI image generation?',
            link: '#',
        },
        {   id: 3, 
            title: 'Is VC Funding Drying Up?', 
            desc: 'Private funding by VC firms is down 50% YOY. We take a look at what that means.',
            link: '#',
        }
    ]
</script>
<template>
    <aside id="sidebar" class="sidebar">
        <h2 class="sidebar__title">New</h2>
        <article class="sidebar__article" v-for="article in sidebarArticles" :key="article.id">
            <a :href="article.link" class="sidebar__article-title">{{ article.title }}</a>
            <p class="sidebar__article-desc">{{ article.desc }}</p>
        </article>
    </aside>
</template>
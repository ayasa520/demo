<script setup>
import ShowCard from './components/ShowCard.vue'

const relatedShows = [
  {
    title: 'Silent Voice',
    image: '/shows/anime-card-4.png',
    meta: 'Movie 1hr 45m',
    href: '#',
    tags: [
      { label: 'New', accent: true },
      { label: '18+' },
      { label: 'HD', accent: true },
      { label: 'CC' },
    ],
  },
  {
    title: 'Arcane',
    image: '/shows/anime-card-5.png',
    meta: 'Series 9 Episodes',
    href: '#',
    tags: [
      { label: 'New', accent: true },
      { label: '16+' },
      { label: 'HD', accent: true },
      { label: 'CC' },
    ],
  },
  {
    title: 'Hero Academia',
    image: '/shows/anime-card-6.png',
    meta: 'Anime 24 Episodes',
    href: '#',
    tags: [
      { label: 'New', accent: true },
      { label: '12+' },
      { label: 'HD', accent: true },
      { label: 'SUB' },
    ],
  },
  {
    title: 'Fate Stay Night',
    image: '/shows/anime-card-8.png',
    meta: 'Movie 1hr 58m',
    href: '#',
    tags: [
      { label: 'New', accent: true },
      { label: '18+' },
      { label: 'HD', accent: true },
      { label: 'CC' },
    ],
  },
]
</script>

<template>
  <main class="page-shell">
    <section class="shows-section" aria-labelledby="related-title">
      <h1 id="related-title">Related Shows</h1>

      <div class="shows-grid">
        <ShowCard v-for="show in relatedShows" :key="show.title" :show="show" />
      </div>
    </section>

    <section class="shows-section shows-section--next" aria-labelledby="recommended-title">
      <h2 id="recommended-title">Recommended Shows</h2>
    </section>
  </main>
</template>

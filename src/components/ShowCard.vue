<script setup>
import { Info, Play } from 'lucide-vue-next'

defineProps({
  show: {
    type: Object,
    required: true,
  },
})
</script>

<template>
  <article class="show-card" tabindex="0" :aria-label="`${show.title} details`">
    <img class="show-card__poster" :src="show.image" :alt="show.title" />

    <div class="show-card__details">
      <h3>{{ show.title }}</h3>

      <ul class="show-card__tags" aria-label="Show tags">
        <li v-for="tag in show.tags" :key="tag.label" :class="{ 'show-card__tag--accent': tag.accent }">
          {{ tag.label }}
        </li>
      </ul>

      <p>{{ show.meta }}</p>

      <div class="show-card__actions">
        <a class="show-card__button show-card__button--filled" :href="show.href">
          <Play :size="22" stroke-width="2.4" />
          Play
        </a>
        <a class="show-card__button show-card__button--outlined" :href="show.href">
          <Info :size="22" stroke-width="2.2" />
          More Info
        </a>
      </div>
    </div>
  </article>
</template>

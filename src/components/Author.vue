<template>
  <div class="author">
    <h1 v-if="showTitle" class="author__site-title">{{ $static.metadata.siteName }}</h1>

    <p
      class="author__intro"
    >We aim to generate awareness and empower a generation of young people to take effective action against climate change and to ensure a clean, bright future</p>

    <p class="author__links">
      <a target="_blank" href="https://twitter.com/iycn">Follow on Twitter</a>
      <a target="_blank" href="https://www.facebook.com/iycngroup/">Facebook</a>
      <a target="_blank" href="https://www.instagram.com/indianyouthclimatenetwork/">Instagram</a>
    </p>
  </div>
</template>

<static-query>
query {
  metadata {
    siteName
  }
}
</static-query>

<script>
export default {
  props: ["showTitle"]
};
</script>

<style lang="scss">
.author {
  margin: 0 auto;
  max-width: 500px;
  text-align: center;
  padding-bottom: calc(var(--space) / 2);

  &__image {
    border-radius: 100%;
    width: 90px;
    height: 90px;
    margin-bottom: 1em;
  }

  &__intro {
    opacity: 0.8;
  }

  &__site-title {
    margin: 0 auto;
    font-size: 1.5em;
    max-width: 400px;
  }

  &__links {
    margin-top: -0.5em;
    a {
      margin: 0 0.5em;
    }
  }
}
</style>

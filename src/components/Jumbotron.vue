<template>
    <section class="hero has-text-centered">
      <div class="hero-body">
        <div class="w-50-lg">
          <h2 class="title is-2">{{title}}</h2>
          <p class="m-5">{{description}}</p>
        </div>
      </div>
    </section>
</template>

<script>
export default {
    props: ['title','description']
}
</script>
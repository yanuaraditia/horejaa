<template>
  <Layout>
    <section class="section">
      <div class="container is-fluid">
        <div class="columns">
          <div class="column is-6-desktop">
            <g-image alt="Example image" src="~/favicon.png" width="135" />
            <h1 class="title is-1"><span class="has-text-weight-normal">Permudah bisnis anda dengan aplikasi</span> Horejaa</h1>
            <p class="subtitle font-primary">
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Pariatur excepturi labore tempore expedita, et iste tenetur suscipit explicabo! Dolores, aperiam non officia eos quod asperiores
            </p>
            <p class="home-links">
              <a href="#" target="_blank" class="button is-primary is-rounded" rel="noopener">About Us</a>
              <a href="#" target="_blank" rel="noopener" class="button is-primary is-outlined is-rounded">GitHub</a>
            </p>
          </div>
        </div>
      </div>
    </section>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Hello, world!'
  }
}
</script>

<style>
.home-links a {
  margin-right: 1rem;
}
</style>

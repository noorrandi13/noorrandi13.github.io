<template>
  <article>
    <section>
      <h1>Get API Result</h1>
      <div>
        <p>{{ title }}</p>
      </div>
    </section>
  </article>
</template>

<script>
// import axios from '@nuxtjs/axios'
import axios from 'axios'

export default {
  async asyncData() {
    const { data } = await axios.get(
      'http://localhost/coba-yii-integration/web/index.php?r=site/hello-world'
    )

    return { title: data.text }
  }
}
</script>

<style></style>

<template>
  <div class="columns is-mobile is-multiline is-centered">
    <div class="column is-one-third-desktop" v-for="post in posts" :key="post.id">
      <nuxt-link :to="post._id">
        <div class="card">
          <header class="card-header">
            <div class="card-header-title is-centered">
                {{ post.title }}
            </div>
          </header>
          <div class="card-image is-200x200">
            <img v-if="post.cover" :src="post.cover.url" alt="">
            <img v-else src="http://via.placeholder.com/200x200" alt="">
          </div>
          <div class="card-content">
            <div class="content">
              <!--{{ post.Summary }}-->
            </div>
          </div>
          <div class="card-footer is-centered">
            Published by: {{post.author.authorName}}
          </div>
        </div>
      </nuxt-link>
    </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
  
  async asyncData ({env, params}) {
    let {data} = await axios.get(`${env.strapi.apiUrl}/article`)
      .catch(e => {
        error({statusCode: 404, message: 'Posts not found'})
      })
    
    let posts = await Promise.all(await data.map(async (p) => {
      if (p.cover !== null){
        p.cover.url = `${env.strapi.apiUrl}${p.cover.url}`
      }
      
      return p
    }))


    return {
      posts
    }
  }
}
</script>

<style>

.title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif; /* 1 */
  display: block;
  font-weight: 300;
  font-size: 100px;
  color: #35495e;
  letter-spacing: 1px;
}

.subtitle {
  font-weight: 300;
  font-size: 42px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.card {
  margin-top: 20px;
  height: 350px;
  width: 340px;
}

.card-image {
  height: 200px;
  margin: auto;
}
img {
  display:block;
  margin:auto;
}
</style>

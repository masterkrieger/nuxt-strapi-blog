<template>
  <div class="section" id="blog-post">
    <div class="container center">
      <hr>
      <h1 class="is-size-2">{{post.title}}</h1>
      
      <h2 class="is-size-3">{{post.author.authorName}}</h2>
      
      <div class="content" v-html="body"></div>
    </div>
  </div>
</template>

<script>
import axios from 'axios'
import marked from 'marked'
import env from '../nuxt.config.js'

export default {
  computed: {
    body () {
      return marked(this.post.content)
    }
  },
  async asyncData({env, params,error}) {
    let post = await axios.get(`${env.strapi.apiUrl}/article/${params.id}`)
      .then(res => {
        return res.data
      })
      .catch(e => {
        error({statusCode: 404, message: 'Posts not found'})
      })
    
    return {
      post
    }
  }
}

</script>

<style>
  
</style>
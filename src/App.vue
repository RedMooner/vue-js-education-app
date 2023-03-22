<template>
  <div>
    <div class="app">
      <post-form @create='createPost'></post-form>
      <post-list :posts="posts">
      </post-list>
    </div>

  </div>
</template>
<script>
import PostForm from '@/components/PostForm.vue'
import PostList from '@/components/PostList.vue'
export default {
  components: {
    PostForm, PostList
  },
  data() {
    return {
      posts: [
        { id: 1, title: 'js1', body: 'Описание1' },
        { id: 2, title: 'js2', body: 'Описание2' },
        { id: 3, title: 'js3', body: 'Описание3' },
      ],
    }
  },
  methods: {
    createPost(post) {
      this.posts.push(post)
      console.log('tst')
    },

  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.app {
  padding: 20px;
}
</style>
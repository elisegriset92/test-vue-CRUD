<template>
  <div class="posts">
    <h1>Add Post</h1>
      <div class="form">
        <div>
          <input type="text" name="title" placeholder="TITLE" v-model="title">
        </div>
        <div>
          <textarea rows="15" cols="15" placeholder="DESCRIPTION" v-model="description"></textarea>
        </div>
        <div>
          <button class="app_post_btn" @click="addPost">Add</button>
        </div>
        <div>
          <router-link v-bind:to="{ name: 'Posts' }"><button class="app_post_btn"> Back</button></router-link>
        </div>
      </div>
  </div>
</template>

<script>
import PostsService from '@/services/PostsService.js';
export default {
  name: 'NewPost',
  data() {
    return {
      title: '',
      description: '',
    };
  },
  methods: {
    async addPost() {
      await PostsService.addPost({
        title: this.title,
        description: this.description,
      });
      if (this.title == '') {
        return alert('Please enter a title first');
      } else {
        this.$router.push({name: 'Posts'});
      }
    },
  },
};
</script>
<style type="text/css">
.form input,
.form textarea {
  width: 500px;
  padding: 10px;
  border: 1px solid #e0dede;
  outline: none;
  font-size: 12px;
}
.form div {
  margin: 20px;
}
.app_post_btn {
  background: #e9bf00;
  color: #fff;
  padding: 10px 80px;
  text-transform: uppercase;
  font-size: 12px;
  font-weight: bold;
  width: 520px;
  border: none;
  cursor: pointer;
}
</style>
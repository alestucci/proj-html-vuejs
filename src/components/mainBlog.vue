<template>
  <div id="blog" class="container">
    <h1>From Our Blog</h1>
    <h2>The latest Classic Shop news</h2>
    <div class="posts">
      <div v-for="post in posts" :key="post.id" class="post" >
        <img :src="getUrlImg(post.img)" alt="post.img" />
        <h5>{{ post.title }}</h5>
        <h6>{{ post.date }} | {{ post.comments }} Comments</h6>
        <p>{{ post.text }}</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "mainBlog",
  data() {
    return {
      posts: [
        {
          img: "post_img_12-300x188",
          title: "Aenean lobortis sapien enim viverra",
          date: "September 9th, 2015",
          comments: 0,
          text: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla,",
        },
        {
          img: "post_img_11-300x188",
          title: "Duis ac massa semper maximus",
          date: "September 9th, 2015",
          comments: 0,
          text: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla,",
        },
        {
          img: "post_img_10-300x188",
          title: "Nunc fermint nulla eu justo sem id",
          date: "September 9th, 2015",
          comments: 0,
          text: "Donec finibus sit amet orci eget ultricies. Praesent posuere ante ut erat fringilla,",
        },
      ],
    };
  },
  methods: {
    getUrlImg(img) {
      return require("../assets/img/" + img + ".jpg");
    },
  },
};
</script>

<style lang="scss" scoped>
#blog {
  text-align: center;
}
.posts {
	display: flex;
	justify-content: space-between;
}
.post {
  width: 30%;
	text-align: left;
}
</style>
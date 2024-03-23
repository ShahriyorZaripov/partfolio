<template>
  <div class="link news">
       <Header  class="none" />
   <h1>MY WORKS</h1>
    <div class="news-cardis">
      <!-- card == start -->
      <div
        class="card"
        v-for="(item, index) of news"
        :key="index"
      >
      <div class="news-a-img">
          <img
            :src="`https://api.termizseo.uz/${item.file[0]}`"
            class="news-img"
          />
      </div>
        <h4>
          <div class="news-clamp clamp">
            <b> {{ item.title }}</b>
          </div>
        </h4>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      news: null,
    };
  },
  created() {
    this.$axios
      .get("https://api.termizseo.uz/api/news/all")
      .then((res) => {
        this.news = res.data;
        console.log(res.data);
      })
      .catch((err) => {
        console.log(err);
      });
  },
};
</script>

<style scoped>
.card .news-a-img img{
  transition: all .6s;
  }
.card .news-a-img{
  overflow: hidden;
}
.card:hover .news-a-img img{
  transform: scale(1.1) rotate(-6deg);

}

/* sss */
.news h1 {

  font-family: cursive;
  margin: 40px auto;
  text-align: center;
  font-weight: 900;
  font-size: 30px;  
  color: #00094b;
  margin-top: 60px;
}
.news .news-cardis {
  font-family: sans-serif;
  display: flex;
  width: 95%;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
  margin: 0 auto;
}
.news .news-cardis .card {
  margin: 10px;
  cursor: pointer;
  max-width: 450px;
  padding-bottom: 30px;
  border-bottom: 2px solid #00094b;
  border-left: 2px solid #00094b;
  border-right: 2px solid #00094b;
  padding: 0 5px ;
}
.news .news-cardis .card .news-a-img {
  display: block;
  width: 100%;
  margin: 0 auto;
  height: 350px;
}
.news .news-cardis .card .news-a-img img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  overflow: hidden;
}
.news .news-cardis .card h4 {
  margin: 10px 0;
  text-align: start;
  padding: 8px;
  font-weight: 300;
  font-size: 18px;
  letter-spacing: 0.5px;
}
.news .news-cardis .card h4 .news-clamp {
  color: #000000;
}
.clamp {
  list-style: none;
  text-decoration: none;
  display: -webkit-box;
  -webkit-line-clamp: 1;
  -webkit-box-orient: vertical;
  overflow: hidden;
}
/* media */
@media(max-width:450px){
  .news .news-cardis .card .news-a-img {
  height: 280px;
}
.news-clamp{
font-size: 15px;
}
}

/* header */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  list-style: none;
  text-decoration: none;
}
</style>
<template>
  <div>
    <div class="add">
      <ul>
        <li ref="myDiv1"><a href="#"></a></li>
        <li ref="myDiv3"><a href="/#Section"></a></li>
        <li ref="myDiv2"><a href="/#Contact"></a></li>
        <li ref="myDiv4"><a href="/#About"></a></li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
   mounted() {
    window.addEventListener('scroll', this.handleScroll);
  },
  methods: {
    handleScroll() {
      // scroll y koordinatasini olish
      var scrolled = window.scrollY;
      // Bizga kerakli divlarni olamiz
      var myDiv1 = this.$refs.myDiv1;
      var myDiv2 = this.$refs.myDiv2;
      var myDiv3 = this.$refs.myDiv3;
      var myDiv4 = this.$refs.myDiv4;
      // Rangni scroll bo'yicha o'zgartiramiz
      if (scrolled >= 2350 && scrolled <= 3475) {
        myDiv1.style.backgroundColor = "#ccf381"; 
        myDiv2.style.backgroundColor = "#ccf381";
        myDiv3.style.backgroundColor = "#ccf381";
        myDiv4.style.backgroundColor = "#ccf381";
      } else {
        myDiv1.style.backgroundColor = "#4831d4"; 
        myDiv2.style.backgroundColor = "#4831d4"; 
        myDiv3.style.backgroundColor = "#4831d4"; 
        myDiv4.style.backgroundColor = "#4831d4"; 
      }
    }
  },
  beforeDestroy() {
    window.removeEventListener('scroll', this.handleScroll);
  }
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  list-style: none;
  text-decoration: none;
}
.add {
  position: fixed;
  bottom: 50px;
  right: 140px;
  transition: all 1s;
  z-index: 10;
}
ul li {
  width: 10px;
  margin: 25px 0;
  height: 10px;
  background: #4831d4;
  transform: rotate(45deg);
  transition: all .5s;
}
li:active {
  transform: scale(1.2) rotate(45deg);
}
a {
  display: block;
  width: 100%;
  height: 100%;
}

/* media */
@media (max-width: 1288px) {
.add {
   bottom: 30px;
    right: 20px;
  z-index: 10;
}
}

@media (max-width: 938px) {
  .add {
    bottom: 5px;
    right: 2px;
    width: 33%;
  }
  .add ul {
    width: 100%;
    align-items: center;
    justify-content: space-around;
    display: flex;
  }
}
</style>
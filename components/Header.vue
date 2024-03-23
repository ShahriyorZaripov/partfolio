<template>
  <div class="header">
    <header>
      <a href="/">
        <h1 ref="myLogo1" class="logo">Shakh</h1>
      </a>
      <nav :class="{ 'd-none': isActive }">
        <ul>
          <li><nuxt-link id="c-dark" to="/myWork">My Works</nuxt-link></li>
          <li><nuxt-link id="c-dark" to="/">HOME</nuxt-link></li>
          <br />
          <li class="salom">Say hello</li>
          <li>
            <a id="c-dark" href="https://zaripovshahriyorbek@gmail.com"
              >Gmail</a
            >
          </li>
          <li>
            <a id="c-dark" href="https://t.me/Programmer_devoloping"
              >Telegram</a
            >
          </li>
        </ul>
      </nav>
      <div class="burger-wrap">
        <div ref="myDiv" class="burger" @click="isActive = !isActive">
          <span
            ref="myDiv1"
            class="span_color"
            :class="{ 'span-x': isActive }"
          ></span>
          <span
            ref="myDiv2"
            class="span_color"
            :class="{ 'span-y': isActive }"
          ></span>
        </div>
      </div>
    </header>
  </div>
</template>


<script>
export default {
  data() {
    return {
      isActive: true,
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
    window.addEventListener("scroll", this.logoleScroll);
  },
  methods: {
    handleScroll() {
      // scroll y koordinatasini olish
      var scrolled = window.scrollY;
      // Bizga kerakli divlarni olamiz
      var myDiv1 = this.$refs.myDiv1;
      var myDiv2 = this.$refs.myDiv2;
      // Rangni scroll bo'yicha o'zgartiramiz
      if (scrolled >= 2350 && scrolled <= 3475) {
        myDiv1.style.backgroundColor = "#ccf381";
        myDiv2.style.backgroundColor = "#ccf381";
      } else {
        myDiv1.style.backgroundColor = "#4831d4";
        myDiv2.style.backgroundColor = "#4831d4";
      }
    },
    logoleScroll() {
      // scroll y koordinatasini olish
      var scrolled = window.scrollY;
      // Bizga kerakli divlarni olamiz
      var myLogo1 = this.$refs.myLogo1;
      // Rangni scroll bo'yicha o'zgartiramiz
      if (scrolled >= 550 && scrolled <= 2350) {
        myLogo1.style.color = "#4831d4";
      } else {
        myLogo1.style.color = "#ccf381";
      }
    },
  },
  beforeDestroy() {
    window.removeEventListener("scroll", this.handleScroll);
    window.removeEventListener("scroll", this.logoleScroll);
  },
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: sans-serif;
  list-style: none;
}
.salom {
  color: #4731d458;
  letter-spacing: 4px;
  font-weight: 800;
}
#c-dark {
  color: #4831d4;
  cursor: pointer;
}
.d-none {
  right: -800px;
}
/* header */
.header {
  width: 100%;
  position: fixed;
  top: 50px;
  padding: 0 40px;
}
header {
  max-width: 1250px;
  margin: 0 auto;
  display: flex;
  align-items: center;
  justify-content: space-between;
  position: relative;
}
header h1 {
  color: #ccf381;
  font-weight: 900;
  font-family: cursive;
  transition: all 0.5s;
}
/* nav */
nav {
  width: 400px;
  padding: 10px;
  text-align: center;
  background: #ffffff;
  position: absolute;
  right: -35.5px;
  top: -11px;
  transition: all 1s;
  z-index: 20;
  cursor: pointer;
}
ul {
  padding-left: 30%;
}
ul li {
  margin: 30px auto;
  text-align: start;
  font-size: 18px;
}
.bkg {
  background: red !important;
}
/* burger */
span {
  display: block;
  background: #4831d4;
  height: 2.4px;
  position: absolute;
  transition: all 1s;
}
.burger-wrap {
  position: absolute;
  right: 0;
  z-index: 50;
}
.burger {
  cursor: pointer;
  position: relative;
  width: 60px;
  height: 22px;
}
.burger :nth-child(1) {
  width: 25px;
  margin: 2px 0 0 auto;
  right: 0;
}
.burger :nth-child(2) {
  width: 55px;
  margin: 19px 0 auto auto;
  right: 0;
}

/* active */
.span-x {
  width: 55px !important;
}
.span-y {
  width: 25px !important;
}

/* media */
@media (max-width: 938px) {
  span {
    background: #ccf381;
  }
}

@media (max-width: 570px) {
  /* header */
  .header {
    top: 20px;
  }
  header h1 {
    font-size: 26px;
    font-weight: 900;
  }
  /* nav */
  nav {
    width: 100%;
    right: 0;
    top: 50px;
  }
}
</style>


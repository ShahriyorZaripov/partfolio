<template>
  <div class="container">
    <div class="home">
      <div class="left">
        <h1>Hello, I am Zaripov Shahriyor Frontend Programmer▿</h1>
        <div class="text">
          <span class="text_left"
            >Highly skilled in progressive improvement, design systems.</span
          >
          <span class="text_right">
            Proven track record of building successful products for clients in
            multiple countries.
          </span>
        </div>
      </div>
      <div class="right">
        <div class="border">
          <span></span>

        </div>
        <div class="img"><img src="/images/image.png" alt="" /></div>
      </div>
    </div>
    <!-- <div class="udar"></div> -->
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
.udar{
  position: absolute;
  width: 10px;
  height: 3475px;
  top: 0;
  background: red;
}
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.container {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 100%;
  min-height: 100vh;
  background: linear-gradient(90deg, #4831d4 67%, #ccf381 33%);
}
.home {
  display: flex;
  max-width: 1200px;
  margin: 0 auto;
  padding: 30px;
  align-items: center;
  flex-wrap: wrap;
  gap: 200px;
}
/* left start */
.left {
  flex: 1 1 5rem;
}
.left h1 {
  color: #ccf381;
  font-size: 54px;
  font-family: serif;
}
.left .text {
  display: flex;
  margin-top: 20px;
  align-items: flex-start;
  justify-content: space-between;
  color: #e7fcbf;
  gap: 20px;
  font-size: 17px;
  line-height: 25px;
}

.right {
  flex: 1 1 5rem;
}
.right .border {
  position: relative;
}
.right .border span {
  border-bottom: 4px solid rgb(255, 255, 255);
  border-right: 4px solid rgb(255, 255, 255);
  width: 350px;
  height: 350px;
  position: absolute;
  top: 30px;
  left: 30px;
}
.right .img {
  width: 350px;
  height: auto;
}
.right .img img {
  width: 100%;
  height: auto;
  overflow: hidden;
}
/* right end */

/* media 1200px */
@media (max-width: 1200px) {
  .home {
    gap: 50px;
  }
  /* left start */
  .left {
    flex: 1 1 5rem;
  }
  .left h1 {
    font-size: 50px;
  }
  .left .text {
    display: flex;
    margin-top: 10px;
    gap: 15px;
    font-size: 15px;
    line-height: 20px;
  }

  .right {
    flex: 1 1 5rem;
  }
  .right .border {
    position: relative;
    display: none;
  }
  /* right end */
}
@media (max-width: 938px) {
  .container {
    background: linear-gradient(180deg, #4831d4 67%, #ccf381 33%);
  }
  .home {
    margin-top: 5.5rem;
    gap: 40px;
    flex-direction: column;
  }
  /* left start */
  .left {
    max-width: 600px;
  }

  .right {
    flex: 1 1 5rem;
  }
  .right .border {
    display: block;
  }
  .right .img {
    max-width: 350px;
  }
  .right .img img {
    border-top-left-radius: 30px;
  }
  /* right end */
}

@media (max-width: 505px) {
  .home {
    padding: 20px 40px;
  }
  /* left start */
  .left {
    max-width: 600px;
  }
  .left h1 {
    font-size: 34px;
  }
  .left .text {
    display: flex;
    flex-direction: column;
  }
  .right .border{
    display: none;
  }

  .right .img {
  width: 300px;
  height: auto;
}
  .right .img img {
    border-top-left-radius: 30px;
  }
  /* right end */
}
@media (max-width: 404px) {
  .home {
    width: 90%;
    padding: 0;
  }
   .right .img {
    max-width: 240px;
  }
  }
</style>
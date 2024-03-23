<template>
  <div class="container">
    <span id="Section"></span>
    <div class="section">
      <div class="section-flex top">
        <div class="text">
          <h1>Design</h1>
          <span
            >I'm probably not the typical designer positioned behind an
            Illustrator artboard adjusting pixels, but I design. Immersed in
            stylesheets tweaking font sizes and contemplating layouts is where
            you'll find me (~_^). I'm committed to creating fluent user
            experiences while staying fashionable.
          </span>
        </div>
        <div class="img">
          <div class="images">
            <img src="images/fr.jpg" alt="" />
          </div>
        </div>
      </div>
      <div class="section-flex row-reverse bottom">
        <div class="text">
          <h1>Engineering</h1>
          <span
            >In building JavaScript applications, I'm equipped with just the
            right tools, and can absolutely function independently of them to
            deliver fast, resilient solutions optimized for scale — performance
            and scalabilty are priorities on my radar.</span
          >
        </div>
        <div class="img">
          <div class="images">
            <img src="images/be.jpg" alt="" />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
.container {
  width: 100%;
  height: auto;
  background: white;
}
.section {
  max-width: 1200px;
  margin: 0 auto;
  padding: 30px;
}
/* top */
.section-flex {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
}
.text {
  max-width: 550px;
  padding: 20px;
}
.text h1 {
  font-size: 50px;
  color: #4831d4;
  font-weight: 800;
}
.text span {
  display: block;
  margin-top: 30px;
  font-size: 18px;
  color: #3d155f;
  line-height: 30px;
}
.images {
  width: 440px;
}
img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
.top {
  margin-top: 100px;
}
.bottom {
  margin-top: 50px;
}
.row-reverse {
  flex-direction: row-reverse;
}

/* media */
@media(max-width:425px){
  .section-flex {
  flex-direction: column;
}
.text {
  max-width: 550px;
  padding: 10px;
}
.text h1 {
  font-size: 40px;
  font-weight: 800;
}
.text span {
  font-size: 14px;
  line-height: 25px;
}
.images {
  width: 330px;
  margin: 0 auto;
}
.top {
  margin-top: 30px;
}
.bottom {
  margin-top: 30px;
}
}
/* media */
@media(max-width:375px){

.text {
  padding: 5px;
}
.text h1 {
  font-size: 40px;
  font-weight: 800;
}
.text span {
  font-size: 14px;
  line-height: 25px;
}
.images {
  max-width: 260px;
  margin: 0 auto;
}
.top {
  margin-top: 30px;
}
.bottom {
  margin-top: 30px;
}
.section {
  padding: 5px;
}
}
</style>
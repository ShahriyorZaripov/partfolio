<template>
  <div class="container">
    <span id="About"></span>
    <div class="locatsia">
      <div class="men">
        <h1>ABOUT ME</h1>
        <div class="address">
          ADRESS🏠
          <span> Uzbekistan, Kashkadarya region, Mirishkor district.</span>
        </div>
        <div class="brithday">BIRTHDAY 🥳 <span>November 12, 2003.</span></div>
        <div class="phone">
          PHONE 📲 <span>My phone number +998 91 451 08 17.</span>
        </div>
      </div>
      <div class="xarita">
        <h1>LOCATION</h1>
        <iframe
          class="ifrem"
          src="https://www.google.com/maps/embed?pb=!1m14!1m12!1m3!1d1868.6214933071885!2d65.80956101945904!3d38.82116875812052!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!5e1!3m2!1sru!2s!4v1711008106492!5m2!1sru!2s"
          style="border: 0"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        ></iframe>
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
  /* background:linear-gradient( #4731d433 , #cbf38146 ); */
}

.locatsia {
  max-width: 1200px;
  margin: 0 auto;
  padding: 30px;
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: 10px;
  flex-wrap: wrap;
}
h1{
  font-family: fantasy;
  margin-bottom: 20px;
  color: #4731d4;
  text-shadow: 10px 10px 10px rgba(0, 0, 0, 0.363);
}
/* men */
.men {
  flex: 2 1 10rem;
}
.men div{
  font-weight: 700;
  margin-top: 100px;
  font-family: cursive;
  text-shadow: 10px 10px 10px rgba(0, 0, 0, 0.363);
}
.men span{
  color:rgba(0, 0, 0, 0.646) ;
  font-weight: 400;
  font-family: cursive;
}
.adress{
  font-size: 20px;
}

/* xarita */
.xarita {
  flex: 3 1 10rem;
  width: 100%;
  text-align: end;
}
.ifrem {
  border-radius: 15px;
  display: block;
  width: 100%;
  margin: auto 0 auto auto;
  height: 450px;
  box-shadow: 10px 10px 10px rgba(0, 0, 0, 0.363);
}
/* media */
@media (max-width:768px){
  .locatsia {
  gap: 50px;
  flex-direction: column;
}
h1{
  margin: 20px;
}
/* men */
.men {
  flex: none;
}
.men div{
  margin-top: 50px;
}
.xarita {
  flex: none;
}
.ifrem {
  width: 100%;
  margin:0;
  height: 350px;
}
}
@media (max-width:426px){
  .locatsia {
  gap: 50px;
  flex-direction: column;
}
h1{
  margin: 10px 0;
  font-size: 25px;
}

.ifrem {
  height: 300px;
}
}
</style>
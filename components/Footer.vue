<template>
  <div class="container">
    <span id="Footer"></span>
    <div class="footer_top">
      <div class="left">
        <span>Say hello to the Programmer</span>
        <ul>
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
      </div>
      <div class="right">
        <ul>
          <li><nuxt-link id="c-dark" to="/myWork">My Works</nuxt-link></li>
          <li><a id="c-dark" href="#">HOME</a></li>
        </ul>
      </div>
    </div>
    <div class="footer_bottom">
      <div class="left">
        <span>︻╦╤─— ̸̇̎/̸̄ ̅̎̎̅͆ ͆͆͆͆̔͞ ͆̅͞ ̄ ̄̇̚ ̎ ̎͆ Zaripov Shahriyor</span>
      </div>
      <div class="right">
        <ul>
          <li><a href="https://github.com/ShahriyorZaripov">G/h</a></li>
          <li><a href="https://t.me/Programmer_devoloping">T/m</a></li>
          <li><a href="https://www.youtube.com/channel/UCWTvQKpAhHpmT5ncwP13Jfw">Y/t</a></li>
          <li><a href="https://www.facebook.com/profile.php?id=100075472795634">F/b</a></li>
        </ul>
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
  height: 100vh;
  background: #3D155F;
}
.footer_top{
  display: flex;
  max-width: 1200px;
  margin: 0 auto;
  padding: 150px 30px;
  align-items: center;
  flex-wrap: wrap;
  gap: 200px;
  font-size: 22px;
  line-height: 3rem;
}
.footer_top .left span{
  color: #cccccc;
  font-family: cursive;
}
.footer_top .left ul li a{
  color:  #ccf381;
  font-family: monospace;
}
.footer_top .right ul li a{
  font-family: monospace;
  color:  #ccf381;
}

.footer_top .right{
padding-top: 50px;
}
/* footer bottom */
.footer_bottom{
    display: flex;
    padding: 30px;
  max-width: 1200px;
  margin: 0 auto;
  /* padding: 150px 30px; */
  align-items: center;
  flex-wrap: wrap;
  gap: 200px;
  font-size: 22px;
  line-height: 3rem;
  border-top: 1px solid white;
}
.footer_bottom .left{
  color: #ccf381;
}
.footer_bottom .right ul{
  display: flex;
  gap: 40px;
}
.footer_bottom .right ul li a{
 color: #ccf381;

}
/* /media 800 px  */
@media(max-width:800px){
.footer_top{
  padding:100px 30px;
  gap: 90px;
  font-size: 22px;
  line-height: 3rem;
}
.footer_top .right{
padding-top: 50px;
}
/* footer bottom */
.footer_bottom{
  gap: 100px;
  font-size: 22px;
  line-height: 3rem;
}
}
/* /media 550 px  */
@media(max-width:600px){
.footer_top{
  flex-direction: column;
  padding:120px 30px 50px 30px;
  gap: 10px;
  align-items: flex-start;
  font-size: 22px;
  line-height: 3rem;
}
.footer_top .right{
  padding-top: 50px;
}
/* footer bottom */
.footer_bottom{
  flex-direction: column;
  align-items: flex-start;
  gap: 10px;
  font-size: 22px;
  line-height: 3rem;
}
.footer_bottom .right ul{
  display: flex;
  gap: 14px;
}
}
/* /media 550 px  */
@media(max-width:550px){
.footer_top{
  flex-direction: column;
  padding:90px 30px 30px 30px;
  gap: 10px;
  align-items: flex-start;
  font-size: 18px;
  line-height: 2rem;
}
.footer_top .right{
  padding-top: 50px;
}
/* footer bottom */
.footer_bottom{
  gap: 10px;
  font-size: 18px;
  line-height: 2rem;
}
}
</style>
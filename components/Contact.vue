<template>
  <div class="container">
    <span id="Contact"></span>
    <div class="contact">
      <h1>Send me a message</h1>
      <span>Write to me if you have any questions or suggestions.</span>
      <div class="form">
        <form @submit.prevent>
          <div class="name">
            <label for="exampleFormControlInput1" class="form-label"
              >Your Name</label
            >
            <input
              type="text"
              class="form-control input-field"
              placeholder=" Enter your name"
              v-model="data.name"
            />
          </div>
          <div class="email">
            <label for="exampleFormControlInput1" class="form-label"
              >Email Address</label
            >
            <input
              type="email"
              class="form-control input-field"
              placeholder=" Enter your email address"
              v-model="data.phone"
            />
          </div>
          <div class="message">
            <label for="exampleFormControlTextarea1" class="form-label"
              >Your Message
            </label>
            <textarea
              class="form-control input-field"
              v-model="data.message"
              placeholder="Hello, could you write a brief description of what to do?"
              id="exampleFormControlTextarea1"
              rows="4" 
              cols="50"
            ></textarea>

          </div>
        </form>
        <div class="btn" @click="Submit">︻╦╤─— Shoot</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      data: {
        name: null,
        email: null,
        message: null,
      },
      token: "6979367142:AAEpWxDSh_0ZLVAkbcCrzZ9_tTAivVaPink",
      myId: "1394289473",
    };
  },

  methods: {
      Submit() {
      let data = `Ism: ${this.data.name}, Email: ${this.data.email}, Xabar: ${this.data.message}`;
      this.$axios
        .post("https://api.telegram.org/bot" + this.token + "/sendMessage", {
          chat_id: this.myId,
          parse_mode: "html",
          text: data,
        })
        .then((res) => {
          if (res.data.ok) {
            // this.success = true;
            this.data = {
              name: "",
              email: "",
              message: "",
            };
            setTimeout(()=>{
              this.success = false;
            },2000)
          }
        })
        .catch((err) => {
          console.log(err);
        });
    }, 
  },
};
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
  background: white;
}
.contact {
  max-width: 1200px;
  margin: 0 auto;
  padding: 30px;
}
.contact h1 {
  padding-top: 100px;
  text-align: center;
  color: #4831d4;
  font-size: 44px;
  font-family: "Lucida Sans Regular", sans-serif;
}
.contact span {
  max-width: 500px;
  margin: 15px auto;
  font-size: 22px;
  display: block;
  text-align: center;
  color: #150476;
}
form {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  gap: 50px;
  margin-top: 50px;
}
label {
  font-size: 15px;
  color: #4831d4;
}
.name,
.email {
  width: 500px;
}
textarea {
  overflow-y: scroll; /* Yoki auto, agar matn o'lchami kerak bo'lsa */
}
.message {
  width: 100%;
  padding: 0 45px;
}
::placeholder {
  font-size: 17px;
  color: rgba(0, 0, 0, 0.511);
}

input,
textarea {
  height: 50px;
  font-size: 17px;
  padding-left: 10px;
  padding-top: 5px;
  margin: 5px auto;
  border: none;
  width: 100%;
}
/*  */
.input-field {
    outline: none; 
    border-bottom: 1.5px solid #4831d4; /* Faqat pastki chiziqli border qo'shamiz */
}

.input-field:focus {
    border-bottom: 1.5px solid #ff0000; /* Cilikga focus bo'lganda rangni o'zgartiramiz */
}
/*  */
.btn {
  margin: 30px auto;
  max-width: 300px;
  height: 60px;
  border: 1.5px solid #4831d4;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #4831d4;
  cursor: pointer;
}
.btn:active{
  transform: scale(1.1);
}

/* media */
@media (max-width: 1112px) {
  .contact h1 {
    padding-top: 50px;
  }
  form {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    gap: 10px;
  }
  .name,
  .email {
    width: 100%;
    padding: 0 45px;
  }
}
@media (max-width: 500px) {
  form{
    margin-top: 2px;
  }
  .contact h1 {
    margin-top: 0px;
    font-size: 35px;
  }
  .contact span {
    max-width: 100%;
    font-size: 18px;
  }
}
@media (max-width: 425px) {
  .contact h1 {
    font-size: 30px;
  }
  .contact span {
    max-width: 100%;
    font-size: 16px;
  }
  .name,
  .email,
  .message {
    width: 100%;
    padding: 0;
  }
}
/* .border_danger{
  border: none;
} */
textarea{
  resize: none;
}
</style>
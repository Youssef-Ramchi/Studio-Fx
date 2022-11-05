<template>
  <div class="header-section">
    <form action="align" class="align">
      <input
        @focus="inputFocus()"
        @blur="inputBlur()"
        ref="text"
        type="text"
        class="quation"
        value="Are you a brand ? how to use stodio for brands"
      />
      <img class="flesh" src="@/assets/flesh1.png" />
    </form>
    <h1>
      The <i>Platform<img src="@/assets/greenlign.png" /></i> <br />
      for Content Creators
    </h1>
    <p class="paragraphe">Contralize your creator business with studio</p>
    <form action="sign-in">
      <input
        @focus="EmailFocus()"
        @blur="EmailBlur()"
        ref="email"
        type="text"
        class="text"
        value="your email adress"
      />
      <input type="submit" class="submit" value="submit" />
    </form>
  </div>
</template>

<script>
export default {
  methods: {
    inputFocus: function () {
      this.$refs["text"].value = "";
    },
    inputBlur: function () {
      if (this.$refs["text"].value === "") {
        return (this.$refs["text"].value =
          "Are you a brand ? how to use stodio for brands");
      }
    },
    EmailFocus: function () {
      this.$refs["email"].value = "";
    },
    EmailBlur: function () {
      if (this.$refs["email"].value === "") {
        return (this.$refs["email"].value = "your email adress");
      }
    },
  },
};
</script>

<style scoped lang="scss">
div {
  font-family: poppins;
  margin: 60px 0 50px;
  .align {
    position: relative;
    width: 30%;
    .quation {
      color: rgb(209, 209, 209);
      font-size: 12px;
      padding: 14px 15px;
      width: calc(100% - 40px);
      border: 1px solid rgb(242, 242, 242, 0.5);
      border-radius: 50px;
      margin: auto auto;
      background-color: black;
    }
    .flesh {
      padding: 12px;
      background-color: #fbf07a;
      border-radius: 27px;
      width: 12px;
      transform: translateX(15px);
      position: absolute;
      right: 12px;
      top: 50%;
      transform: translateY(-50%);
      cursor: pointer;
    }
  }
  h1 {
    font-size: 55px;
    color: rgb(243, 255, 246);
    font-weight: 550;
    text-align: center;
    line-height: 65px;
    margin: 25px 0 20px;
    i {
      position: relative;
      z-index: 1;
      img {
        position: absolute;
        left: 0px;
        top: 40px;
        z-index: -1;
        opacity: 40%;
        width: 100%;
      }
    }
  }
  .paragraphe {
    font-size: 16px;
    color: white;
    opacity: 70%;
    font-weight: 100;
  }
  form {
    margin: 40px auto 0;
    position: relative;
    width: 30%;
    .text {
      background-color: rgb(56, 56, 56);
      color: rgb(209, 209, 209);
      font-size: 12px;
      padding: 17px 20px;
      width: calc(100% - 40px);
      border: 0;
      border-radius: 50px;
      margin: auto auto;
    }
    .submit {
      background-color: rgb(62, 191, 52);
      color: rgb(255, 255, 255);
      font-size: 12px;
      padding: 12px 15px;
      width: fit-content;
      border: 0;
      border-radius: 50px;
      position: absolute;
      top: 5px;
      right: 5px;
      cursor: pointer;
    }
  }
}
@media (max-width: 500px) {
  div {
    margin: 60px 0 65px;
    .align {
      width: 80%;

      .quation {
        font-size: 10px;
      }
      .flesh {
        right: 9px;
      }
    }
    h1 {
      font-size: 32px;
      margin: 20px 0 20px;
      line-height: 45px;
      i {
        img {
          width: 100%;
          top: 25px;
        }
      }
    }
    .paragraphe {
      font-size: 13px;
      margin-bottom: 25px;
    }
    form {
      margin-top: 25px;
      width: 75%;
      .text {
        font-weight: 100;
      }
    }
  }
}
</style>

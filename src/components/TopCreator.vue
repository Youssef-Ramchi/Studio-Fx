<template>
    <div class="father">
      <div class="align">
        <h2>
          Top
          <span>Creator<img src="@/assets/greenlign.png" /></span>
        </h2>
        <h4>View All</h4>
      </div>
      <div class="creator">
        <button @click="switchMe()" ref="drag" class="drag">
          Drag<img class="sahm" src="@/assets/flesh.svg" />
        </button>
        <button @click="backTo()" ref="back" class="back">
          <img class="opossit-sahm" src="@/assets/flesh.svg" /> back
        </button>
        <div ref="image" class="images">
          <div ref="image" class="images">
            <div class="show" v-for="creator in creators" :key="creator">
              <div ref="deta" class="data">
                <span class="span">
                  {{ creator.date }}
                </span>
                <p>
                  {{ creator.name }}
                </p>
              </div>
              <img :src="creator.img" />
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  data() {
    return {
      creators: [
        {
          img: require("@/assets/baywe.jpg"),
          name: "Baywe.we",
          date: "Actore",
        },
        {
          img: require("@/assets/One.png"),
          name: "Alex.Mo",
          date: "Creator",
        },
        {
          img: require("@/assets/suns.jpg"),
          name: "Alima.M",
          date: "Singer",
        },
        {
          img: require("@/assets/One.png"),
          name: "Thom.Ro",
          date: "Creator",
        },
        {
          img: require("@/assets/girl.jpg"),
          name: "Amanda.L",
          date: "Actore",
        },
        {
          img: require("@/assets/di-caprio.jpg"),
          name: "Di.caprio",
          date: "Actore",
        },
        {
          img: require("@/assets/emineme.jpg"),
          name: "Eminem",
          date: "Singer",
        },
      ],
    };
  },
  methods: {
    switchMe() {
      return (
        (this.$refs["image"].style.transform = "translateX(-27%)"),
        (this.$refs["back"].style.display = "inline"),
        (this.$refs["drag"].style.display = "none")
      );
    },
    backTo() {
      return (
        (this.$refs["image"].style.transform = "translateX(0)"),
        (this.$refs["drag"].style.display = "inline"),
        (this.$refs["back"].style.display = "none")
      );
    },
  },
};
</script>

<style scoped lang="scss">
.father {
  text-align: start;
  margin: 0 0 40px 0px;
  color: white;
  .align {
    h2 {
      float: left;
      width: 50%;
      margin-bottom: 40px;
      margin-left: 100px;
      span {
        position: relative;
        img {
          position: absolute;
          top: 30px;
          left: 0;
          width: 86px;
        }
      }
    }
    h4 {
      float: right;
      text-align: end;
      margin-right: 100px;
      font-weight: 100;
      opacity: 70%;
    }
    h4:hover {
      opacity: 100%;
      cursor: pointer;
    }
  }
  .creator {
    width: 155%;
    overflow: hidden;
    margin-top: 20px;
    position: relative;
    .drag {
      background-color: rgba(0, 0, 0, 0.7);
      padding: 20px 35px 20px 25px;
      color: white;
      border: 1.5px solid rgba(255, 255, 255, 0.8);
      border-radius: 50px;
      font-size: 17px;
      position: absolute;
      font-weight: 100;
      top: 50%;
      right: 100px;
      width: -moz-fit-content;
      width: fit-content;
      left: 54%;
      cursor: pointer;
      z-index: 1;
      transform: translateY(-50%);
    }
    .sahm {
      width: 20px;
      position: relative;
      left: 12px;
      top: 1px;
    }
    .back {
      background-color: rgb(0, 0, 0, 0.7);
      padding: 20px 25px 20px 35px;
      color: white;
      border: 1px solid rgb(255, 255, 255, 0.6);
      border-radius: 50px;
      font-size: 17px;
      position: absolute;
      top: 50%;
      left: 100px;
      cursor: pointer;
      z-index: 1;
      display: none;
      transform: translateY(-50%);
    }
    .opossit-sahm {
      width: 20px;
      position: relative;
      right: 12px;
      transform: scaleX(-1);
    }
    .images {
      margin-left: 10px;
      transition: 0.5s ease;
      .show {
        display: inline-block;
        position: relative;
        transition: 0.3s ease;
        padding: 10px 0;
        margin-right: 20px;
        .data {
          position: absolute;
          top: 75%;
          left: 50%;
          transform: translate(-50%, -50%);
          text-align: center;
          .span {
            background-color: rgba(143, 143, 143, 0.3);
            padding: 3px 10px;
            color: white;
            border: 1px solid rgb(255, 255, 255, 0.6);
            border-radius: 50px;
            font-size: 13px;
            cursor: pointer;
            font-family: outfit;
            font-weight: 300;
          }
          p {
            font-size: 25px;
            margin: 10px;
            font-family: outfit;
            font-weight: 200;
          }
        }
        img {
          width: 250px;
          height: 250px;
          border-radius: 50%;
          cursor: pointer;
        }
      }
      .show:hover {
        transform: translateY(-5px);
      }
    }
  }
}
@media (max-width: 500px) {
  .father {
    text-align: start;
    margin: 60px 0 40px 0px;
    justify-items: center;
    .align {
      align-items: center;
      h2 {
        float: left;
        width: fit-content;
        text-align: start;
        margin: 0 20px 25px;
        font-size: 23px;
        font-weight: 550;
        span {
          img {
            top: 27px;
            width: 100%;
          }
        }
      }
      h4 {
        float: none;
        text-align: end;
        margin-right: 25px;
        font-weight: 100;
        opacity: 70%;
      }
    }
    .creator {
      width: 100%;
      overflow: hidden;
      text-align: center;
      .drag {
        display: none;
      }
      .back {
        display: none;
      }
      .images {
        margin: 0;
        .show {
          margin: 0 10px;
          .data {
            .span {
              font-size: 10px;
            }
            p {
              font-size: 18px;
              margin: 5px;
            }
          }
          img {
            width: 165px;
            height: 165px;
            border-radius: 50%;
          }
        }
      }
    }
  }
}
</style>

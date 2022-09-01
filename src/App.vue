<script setup lang="ts"></script>

<template>
  <header class="flex justify-between items-center box-border z-[5] h-[90px]">
    <div class="cursor-pointer z-[5] overflow-hidden">
      <div class="flex items-center header__logo__wrapper">
        <svg
          data-v-a9044cc0=""
          width="151"
          height="24"
          xmlns="http://www.w3.org/2000/svg"
          class="overflow-hidden"
        >
          <path
            data-v-a9044cc0=""
            d="M0 0s1.201.356 3.1.902l.512.147.821.235.582.165a511.29 511.29 0 006.478 1.795l.742.2 1.494.396.748.195c4.235 1.103 8.371 2.085 10.784 2.412.236.032.623.11 1.035.155l.155.015c1.455.125 3.015-.273-.747-4.58L36.19 5.752a10.242 10.242 0 015.3 4.288L50.088 24s-4.186-2.33-8.83-4.874l-.637-.348-.96-.524c-3.525-1.924-7.071-3.834-9.064-4.837a14.056 14.056 0 00-1.44-.617l-.174-.062a9.401 9.401 0 00-.447-.142l-.18-.05c-1.887-.493-3.632-.127.204 5.168L0 0zm67.07 5.265c.195-.01 4.696-.197 4.696 3.489v.059c-.003.372-.116 2.384-2.082 2.962 0 0 2.368.745 2.36 3.197l-.003.9v.534l-.001.154v.85l.001.065v.152l.001.037v.078l.001.016v.025h-4.37v-2.09c-.004-.115-.098-1.844-2.238-1.844h-7.613v3.934h-4.561V5.266H67.07zm24.8-.004V8.66h-7.135v9.123h-4.5V8.66h-7.148v-3.4H91.87zm58.434 0V8.66h-7.135v9.123h-4.5V8.66h-7.147v-3.4h18.782zm-40.695 0v3.402h-12.33v1.825h8.043v3.182h-8.043v4.113h-4.366V5.266h1.925V5.26h14.77zm5.58 0v4.21l7.13-4.21 7.303.023-9.626 5.665 10.482 6.834h-7.273l-8.016-5.246v5.246h-4.537V5.26h4.537zM59.646 8.664h-1.824v2.145h8.162s1.313.13 1.313-1.14c0-.672-.405-.97-1.181-.988-.317-.007-1.763-.012-3.36-.014h-.538l-.27-.001h-.539l-.266-.001-1.265-.001h-.232z"
            fill="#FFF"
            fill-rule="nonzero"
          ></path>
        </svg>

        <svg
          data-v-a9044cc0=""
          width="12"
          height="12"
          xmlns="http://www.w3.org/2000/svg"
          class="ml-3 mr-3"
        >
          <path
            data-v-a9044cc0=""
            d="M12.01.697L6.708 5.999l5.302 5.304-.707.707-5.302-5.304L.697 12.01l-.707-.707L5.294 6-.01.697.697-.01 6 5.292 11.303-.01l.707.707z"
            fill="#D8D8D8"
            fill-rule="evenodd"
            fill-opacity=".32"
          ></path>
        </svg>

        <svg
          class="md:h-[20.87px] h-[24px] overflow-hidden"
          data-v-a9044cc0=""
          data-name="Layer 1"
          xmlns="http://www.w3.org/2000/svg"
          viewBox="0 0 413.62 144.78"
        >
          <path
            class="fill-white"
            data-v-a9044cc0=""
            d="M413.62 0l-302.6 128.86q-37.64 15.92-63.21 15.92-29 0-42-20.27-8.2-13-4.83-33.06t17.83-42.71Q30.91 30.39 58.42.48a105.53 105.53 0 00-13.51 31.85q-7.24 30.89 13 45.37 9.65 6.76 26.54 6.76a123.37 123.37 0 0030.4-4.34z"
            fill="#111"
          ></path>
        </svg>
      </div>
    </div>
  </header>
  <div v-if="isDesktop" class="absolute top-0 right-0 bottom-0 left-0">
    <video
      id="myVideo"
      autoplay
      loop
      preload=""
      src="/home.mp4"
      type="video/mp4"
      muted
      class="w-full h-full object-cover"
    >
      Your browser does not support the video tag.
    </video>
  </div>
  <div
    v-if="isDesktop"
    class="absolute top-0 right-0 w-1/2 h-full text-white flex justify-center flex-col items-center"
  >
    <div
      class="text-[80px] leading-[80px] text-center mt-4 mb-6 uppercase overflow-hidden"
    >
      <div class="inline-block overflow-hidden">
        <div class="inline-block word___meet">meet</div>
      </div>
      <div class="overflow-hidden block word___hpplt" id="hpplt">hpplt</div>
    </div>
    <button @click="gotoLinkedin()">
      <span class="z-[2]">Connect Linkedin</span>
    </button>
    <p
      class="inline-block overflow-hidden leading-8 tracking-[0.2px] text-[14px]"
    >
      <span class="block">
        Follow hippolyte on
        <a target="_blank" href="https://github.com/hippolyte42">github</a>
      </span>
    </p>
  </div>
  <div
    v-else
    class="flex justify-center items-center w-full h-[calc(100%-90px)]"
  >
    <div class="text-center">
      <img
        src="/2212.png"
        class="mx-0 my-auto w-[252px] h-auto mb-12 touch-pan-x image___penguin"
      />
      <span class="text-[28px] text___mobile">Desktop only</span>
      <p
        class="mx-0 my-auto text-[#777] w-[252px] text-[16px] leading-[23px] text___mobile"
      >
        HPPLT experience is too much to handle for your phone. Get on a LINUX to
        Connect with HPPLT.
      </p>
    </div>
  </div>
</template>

<script>
import gsap from "gsap";
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
  data() {
    return {
      isDesktop:
        !navigator.userAgent.match(/Android/i) &&
        !navigator.userAgent.match(/webOS/i) &&
        !navigator.userAgent.match(/iPhone/i) &&
        !navigator.userAgent.match(/iPad/i) &&
        !navigator.userAgent.match(/iPod/i) &&
        !navigator.userAgent.match(/BlackBerry/i) &&
        !navigator.userAgent.match(/Windows Phone/i),
    };
  },
  methods: {
    gotoLinkedin() {
      window.open("https://www.linkedin.com/in/hippolyte-jacque/");
    },
  },
  mounted() {
    const tl = gsap.timeline({
      defaults: { ease: "power4.inOut", duration: 0 },
    });

    if (this.$data.isDesktop) {
      tl.to(".header__logo__wrapper", { y: "0px", duration: 0.5 })
        .to(".word___meet", {
          y: "0px",
          duration: 0.75,
        })
        .to(
          ".word___hpplt",
          {
            y: "0px",
            duration: 0.75,
          },
          0.7
        )
        .to("button", {
          opacity: 1,
          duration: 0.5,
        })
        .to("span", {
          y: "0px",
          duration: 0.5,
        });
    } else {
      tl.to(".image___penguin", { opacity: 1, duration: 1 })
        .to(".text___mobile", {
          opacity: 1,
          duration: 1.25,
        })
        .to(".header__logo__wrapper", { y: "0px", duration: 0.25 });
    }
  },
});
</script>

<style scoped>
@font-face {
  font-family: "TT_Alientz_Var_Serif";
  src: local("TT_Alientz_Var_Serif"),
    url(./assets/TT_Alientz_Var_Serif.ttf) format("truetype");
}

@font-face {
  font-family: "Sohne-Buch";
  src: local("Sohne-Buch"), url(./assets/Sohne-Buch.otf) format("truetype");
}

.text___mobile,
.image___penguin {
  opacity: 0;
}

.word___meet,
.word___hpplt {
  transform: translateY(80px);
}

.header__logo__wrapper,
p span {
  transform: translateY(25px);
}

#hpplt {
  font-family: "TT_Alientz_Var_Serif", Helvetica, Arial;
}

button {
  -webkit-font-smoothing: antialiased;
  position: relative;
  border: none;
  border-radius: 4px;
  color: #fff;
  background: #5b1eff;
  padding: 16px;
  height: 56px;
  box-sizing: border-box;
  cursor: pointer;
  font-size: 16px;
  letter-spacing: 0.4px;
  display: flex;
  justify-content: center;
  align-items: center;
  backdrop-filter: blur(4px);
  width: 200px;
  margin-bottom: 16px;
  opacity: 0;
}

button:hover {
  color: #000;
}

button:before {
  display: block;
  position: absolute;
  border-radius: 4px;
  left: 0px;
  top: 0px;
  height: 0px;
  width: 100%;
  z-index: 1;
  content: "";
  background: #fff;
  transition: all 0.2s cubic-bezier(0.42, 0, 0.58, 1);
}

button:hover::before {
  bottom: 0%;
  top: auto;
  height: 100%;
}

a::after {
  content: "";
  position: absolute;
  width: 100%;
  transform: scaleX(0);
  height: 2px;
  top: 100%;
  left: 0;
  background-color: #5b1eff;
  transform-origin: bottom right;
  transition: transform 0.25s ease-out;
}

a:hover:after {
  transform: scaleX(1);
  transform-origin: bottom left;
}

#myVideo {
  position: fixed;
  right: 0;
  bottom: 0;
  min-width: 100%;
  min-height: 100%;
  opacity: 1;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}
</style>

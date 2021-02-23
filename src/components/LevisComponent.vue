<template>
  <section class="levis">
    <div class="levis__left"></div>
    <div class="levis__right"></div>
    <div class="levis__nav">
      <div class="logo">Levi's<span class="reg">&reg;</span></div>

      <div class="menu"><i class="fa fa-bars"></i></div>

      <div class="categories">
        <span>Men</span>
        <span>Women</span>
        <span>Kids</span>
      </div>

      <div class="search"><i class="fa fa-search"></i></div>

      <div class="bag"><i class="fa fa-shopping-bag"></i></div>
    </div>
    <div class="levis__media">
        <span>Facebook</span>
        <span>Instagram</span>
        <span>Twitter</span>
    </div>

    <div class="levis__product">
      <img class="levis__product-img"  src="/img/levi-shirt.png" alt="">

      <div class="levis__product-text">
        <h1 class="product-title">colorblock</h1>
        <p class="product-subtitle">Full sleeve t-shirt</p>
      </div>
    </div>

    <div class="levis__dots">
      <span class="dot"></span>
      <span class="dot"></span>
      <span class="dot"></span>
      <span class="dot"></span>
    </div>
  </section>
</template>

<script>
import gsap from 'gsap';
let masterTL = gsap.timeline();
export default {
  mounted() {
      masterTL.add(this.left());
      masterTL.add(this.topMenu());
      masterTL.add(this.media());
      masterTL.add(this.dots());
      masterTL.add(this.productImg());
      //masterTL.add(this.productTitle());
      //masterTL.add(this.upDownImg());
      masterTL.play();
  },

  methods: {
    left() {
        let tl = gsap.timeline();
        tl.from('.levis__left', 1.6, {
          delay: 0.6,
          width: 0,
          ease: 'expo.inOut'
        });

        tl.from('.levis__right', 1.6, {
          delay: 0,
          width: 0,
          ease: 'expo.inOut'
        }, '< 0');

      return tl;
    },

    topMenu() {
      let tl = gsap.timeline();
      tl.from(".logo", 1, {
        opacity: 0,
        x: -20,
        ease: "expo.easeInOut"
      });

      tl.from(".menu", 1, {
        opacity: 0,
        x: -20,
        ease: "expo.easeInOut"
      }, '< .2');

      tl.from(".categories", 1, {
        opacity: 0,
        x: -150,
        ease: "expo.easeInOut"
      }, '< .2');

      tl.from(".search", 1, {
        opacity: 0,
        x: -20,
        ease: "expo.easeInOut"
      }, '< .2');

      tl.from(".bag", 1, {
        opacity: 0,
        x: -20,
        ease: "expo.easeInOut"
      }, '< .2');

      return tl;
    },

    media() {
      let tl = gsap.timeline();
      tl.staggerFrom(".levis__media span", 1, {
        opacity: 0,
        y: 40,
        ease: "power3.easeInOut"
      }, 0.08);

      return tl;
    },

    dots() {
      let tl = gsap.timeline();
      tl.staggerFrom(".levis__dots span", 1, {
        opacity: 0,
        y: -40,
        ease: "power3.easeInOut"
      }, 0.08);

      return tl;
    },

    productImg() {
      let tl = gsap.timeline();
      tl.from(".levis__product-img", 3, {
        opacity: 0,
        y: -20,
        ease: "expo.easeInOut"
      });

      tl.to(".levis__product-img", 2, {
        y: 30,
        repeat: -1,
        yoyo: true,
        ease: "power1.inOut",
      }, '< 0');

      tl.from(".product-title", 3, {
        opacity: 0,
        y: 50,
        ease: "expo.easeInOut",
      }, '< 0');

      tl.from(".product-subtitle", 3, {
        opacity: 0,
        y: 50,
        ease: "expo.easeInOut"
      }, '< .2');

      // tl.to(".levis__product-img", 2, {
      //   y: 20,
      //   repeat: -1,
      //   yoyo: true,
      //   ease: "circ.easeInOut"
      // }, '< 0');

      return tl;
    },

    productTitle() {
      let tl = gsap.timeline();
      tl.from(".product-title", 3, {
        opacity: 0,
        y: 50,
        ease: "expo.easeInOut",
      });

      tl.from(".product-subtitle", 3, {
        opacity: 0,
        y: 50,
        ease: "expo.easeInOut"
      }, '< .2');

      return tl;
    },

    upDownImg() {
      let tl = gsap.timeline();
      tl.from(".levis__product-img", 3, {
        y: -20,
        repeat: -1,
        ease: "expo.easeInOut",
        delay:0,
        stagger: {
          from: "0"
        }
      });

      return tl;
    }
  }
};
</script>

<style></style>

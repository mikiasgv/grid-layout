<template>
  <section class="features">
            <div class="feature">
                <svg class="feature__icon">
                    <use xlink:href="img/sprite.svg#icon-global"></use>
                </svg>
                <h4 class="heading-4 heading-4--dark">World's best luxury homes</h4>
                <p class="feature__text">Lorem, ipsum dolor sit amet consectetur adipisicing elit. Tenetur distinctio necessitatibus pariatur voluptatibus.</p>
            </div>

            <div class="feature">
                <svg class="feature__icon">
                    <use xlink:href="img/sprite.svg#icon-trophy"></use>
                </svg>
                <h4 class="heading-4 heading-4--dark">Only the best properties</h4>
                <p class="feature__text">Voluptatum mollitia quae. Vero ipsum sapiente molestias accusamus rerum sed a eligendi aut quia.</p>
            </div>

            <div class="feature">
                <svg class="feature__icon">
                    <use xlink:href="img/sprite.svg#icon-map-pin"></use>
                </svg>
                <h4 class="heading-4 heading-4--dark">All homes in in top locations</h4>
                <p class="feature__text">Tenetur distinctio necessitatibus pariatur voluptatibus quidem consequatur harum.</p>
            </div>

            <div class="feature">
                <svg class="feature__icon">
                    <use xlink:href="img/sprite.svg#icon-key"></use>
                </svg>
                <h4 class="heading-4 heading-4--dark">New home in one week</h4>
                <p class="feature__text">Vero ipsum sapiente molestias accusamus rerum. Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
            </div>

            <div class="feature">
                <svg class="feature__icon">
                    <use xlink:href="img/sprite.svg#icon-presentation"></use>
                </svg>
                <h4 class="heading-4 heading-4--dark">Top 1% realtors</h4>
                <p class="feature__text">Quidem consequatur harum, voluptatum mollitia quae. Tenetur distinctio necessitatibus pariatur voluptatibus.</p>
            </div>

            <div class="feature">
                <svg class="feature__icon">
                    <use xlink:href="img/sprite.svg#icon-lock"></use>
                </svg>
                <h4 class="heading-4 heading-4--dark">Secure payments on nexter</h4>
                <p class="feature__text">Pariatur voluptatibus quidem consequatur harum, voluptatum mollitia quae.</p>
            </div>
        </section>
</template>

<script>
import gsap from 'gsap';
import { ScrollTrigger } from "gsap/dist/ScrollTrigger";
export default {
  mounted() {
    gsap.registerPlugin(ScrollTrigger);
    gsap.to(".feature", {
    scrollTrigger: {
        trigger: '.feature',
        toggleActions: "restart none none none"
    },
    x: 30,
    yoyo: true, 
    repeat: 1, 
    ease: "power1.inOut",
    delay:1,
    stagger: {
      grid: "auto",
      from: "left"
    }
  });
  }
};
</script>

<style lang="scss" scoped>
</style>
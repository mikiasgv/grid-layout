<template>
  <div class="realtors">
            <h3 class="heading-3">Top 3 Realtors</h3>
            <div class="realtors__list">
                <img src="img/realtor-1.jpeg" alt="Realtor 1" class="realtors__img first--img">
                <div class="realtors__details realtors__details--first">
                    <h4 class="heading-4 heading-4--light">Erik Feinman</h4>
                    <p class="realtors__sold">245 houses sold</p>
                </div>

                <img src="img/realtor-2.jpeg" alt="Realtor 2" class="realtors__img second--img">
                <div class="realtors__details realtors__details--second">
                    <h4 class="heading-4 heading-4--light">Kim Brown</h4>
                    <p class="realtors__sold">212 houses sold</p>
                </div>

                <img src="img/realtor-3.jpeg" alt="Realtor 3" class="realtors__img third--img">
                <div class="realtors__details realtors__details--third">
                    <h4 class="heading-4 heading-4--light">Toby Ramsey</h4>
                    <p class="realtors__sold">198 houses sold</p>
                </div>
            </div>
        </div>
</template>

<script>
import gsap from 'gsap';
let masterTL = gsap.timeline();
export default {
    mounted() {
        masterTL.add(this.realtorsIMG());
        masterTL.add(this.realtorsTitle());
        masterTL.play();
    },

    methods: {
        realtorsIMG() {
            let tl = gsap.timeline();
            tl.to('.first--img',  {
                opacity: 1,
                x: 0,
                duration: 0.5,
                ease: 'power1'
            });
            tl.to('.second--img',  {
                opacity: 1,
                x: 0,
                duration: 0.5,
                ease: 'power1'
            }, '<.3');
            tl.to('.third--img',  {
                opacity: 1,
                x: 0,
                duration: 0.5,
                ease: 'power1'
            }, '<.3');

          return tl;
        },

        realtorsTitle() {
            let tl = gsap.timeline();
            tl.to('.realtors__details--first',  {
                opacity: 1,
                x: 0,
                duration: 0.5,
                ease: 'back'
            });
            tl.to('.realtors__details--second',  {
                opacity: 1,
                x: 0,
                duration: 0.5,
                ease: 'back'
            }, '<.3');
            tl.to('.realtors__details--third',  {
                opacity: 1,
                x: 0,
                duration: 0.5,
                ease: 'back'
            }, '<.3');

          return tl;
        }
    }
};
</script>

<style lang="scss" scoped>
</style>
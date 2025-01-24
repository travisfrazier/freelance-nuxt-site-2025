<script setup>
import CountUp from "vue-countup-v3";

const counter_data = [
  {
    id: 1,
    title: "Years Of Experience",
    count: 6,
    cls: "plus",
  },
  {
    id: 2,
    title: "Projects",
    count: 100,
    cls: "plus",
  },
  {
    id: 3,
    title: "Client Satisfactions",
    count: 90,
    cls: "percent",
  },
];
</script>

<template>
  <ClientOnly>
    <section id="about" class="about-area">
      <div class="container">
        <div class="row">
          <!-- START ABOUT TEXT DESIGN AREA -->
          <div class="col-lg-3 col-sm-3">
            <h2 class="about-pre-title">About Me</h2>
          </div>
          <div class="col-lg-9 col-sm-9">
            <div class="about-content-part wow fadeInUp delay-0-2s">
              <p>
                I specialize in helping small businesses take their web presence to the next level. Whether that's through revampging an existing site or creating a new one from scratch, I can help you achieve your goals. I also do custom web applications and have experience with a variety of technologies. Let's work together to create something amazing!
              </p>
            </div>
            <!-- START COUNTER DESIGN AREA -->
            <div
              class="hero-counter-area d-flex justify-content-between wow fadeInUp delay-0-4s"
            >
              <div
                v-for="(counter, i) in counter_data"
                :key="i"
                class="counter-item counter-text-wrap"
              >
                <span :class="`count-text d-flex justify-content-center ${counter.cls}`">
                  <count-up
                  :end-val="counter.count" 
                ></count-up>
                </span>
                <span class="counter-title">{{ counter.title }}</span>
              </div>
            </div>
            <!-- / END COUNTER DESIGN AREA -->
          </div>
          <!-- / END ABOUT TEXT DESIGN AREA -->
        </div>
      </div>
    </section>
  </ClientOnly>
</template>
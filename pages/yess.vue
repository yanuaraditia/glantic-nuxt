<template>
  <section class="py-5">
    <div class="container mt-lg-4">
      <div class="display-3 fw-bold mb-5">It's been <span class="text-primary" v-text="elapsed_time"></span> since moment we became lovers.</div>
      <div class="display-3 fw-bold mb-5">
        <span class="blurred">Whatever comes my way, I will hold your hand and know it will be okay.</span>
        <span class="blurred">If I could write thank you on every piece of paper in the world, I’d do it for you in a heartbeat.</span>
      </div>
      <div class="display-3 fw-bold mb-5">
        <span class="blurred">Although the most precious present of my life is my girlfriend,</span>
        <span class="blurred">I’m still thankful for the gift you gave me.</span>
      </div>
      <div class="display-3 fw-bold mb-5">
        <span class="blurred">Thank you for the love and caring.</span>
        <span class="blurred">I love you so much!</span>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  data() {
    return {
      when_start: 0
    }
  },
  computed: {
    elapsed_time() {
      this.time_elapsed()
      return this.when_start
    }
  },
  methods: {
    time_elapsed() {
      var countDownDate = new Date("Mar 28, 2022 18:30:00").getTime()
      setInterval(() => {

        // Get today's date and time
        var now = new Date().getTime();

        // Find the distance between now and the count down date
        var distance = now - countDownDate;

        // Time calculations for days, hours, minutes and seconds
        var days = Math.floor(distance / (1000 * 60 * 60 * 24));
        var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
        var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
        var seconds = Math.floor((distance % (1000 * 60)) / 1000);

        this.when_start = days + "d " + hours + "h "
          + minutes + "m " + seconds + "s ";
      },1000)
    }
  }
}
</script>

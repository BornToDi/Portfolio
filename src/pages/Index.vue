<template>
  <div class="row">
    <div class="col-12 col-md-6 pl-2 md:pl-20 py-2 md:py-24 q-pa-md">
      <div class="text-2xl md:text-4xl">Contact Me</div>
      <div class="mt-10 md:mt-20 flex gap-5">
        <q-icon class="text-2xl text-cyan-500" name="call" />
        <div class="text-md md:text-2xl">+8801749470282</div>
      </div>
      <div class="mt-10 flex gap-5">
        <q-icon class="text-2xl text-cyan-500" name="email" />
        <div class="text-md md:text-2xl">z.i.nayeem45@gmail.com</div>
      </div>
      <div class="mt-10 flex gap-5">
        <q-icon class="text-2xl text-cyan-500" name="facebook" />
        <div class="text-md md:text-2xl">
          <a
            class="text-white"
            style="text-decoration: none"
            href="https://www.facebook.com/the.leader.will.come.one.day?mibextid=ZbWKwL"
            >Facebook Link</a
          >
        </div>
      </div>
      <div class="mt-10 flex gap-5">
        <q-icon class="text-2xl text-cyan-500" name="link" />
        <div class="text-md md:text-2xl">
          <a
            class="text-white"
            style="text-decoration: none"
            href="https://github.com/BornToDi"
            >GitHub Link</a
          >
        </div>
      </div>
      <div class="mt-10 flex gap-3 md:gap-5">
        <q-icon class="text-2xl text-cyan-500" name="location_on" />
        <div class="text-md md:text-2xl">
          Banani Residential Area-50, Dhaka-1212
        </div>
      </div>
    </div>
    <div class="col-12 col-md-6">
      <div class="md:pr-20 md:pl-20 pt-14 md:pb-40">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3651.023519611964!2d90.39924681385392!3d23.782176793481053!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x3755c76db868adf1%3A0xf459889a1357ede!2sBSTI%20Quarters!5e0!3m2!1sen!2sbd!4v1675079462877!5m2!1sen!2sbd"
          height="600"
          class="w-full"
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        ></iframe>
      </div>
    </div>
  </div>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "PageIndex",
});
</script>
<style>
@import "tailwindcss/base";
@import "tailwindcss/components";
@import "tailwindcss/utilities";
</style>

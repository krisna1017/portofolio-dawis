<template>
  <div class="flex justify-center items-center">
    <span ref="typing" class="font-thin text-lg uppercase tracking-wider"></span>
  </div>
</template>

<script>
import Typed from 'typed.js';

export default {
  name: "TypingText",

  mounted() {
    new Typed(this.$refs.typing, {
      strings: [
        "GRAPHIC DESIGNER",
        "UI/UX DESIGNER",
      ],

      typeSpeed: 60,
      backSpeed: 40,
      backDelay: 1500,
      loop: true,
      showCursor: true,
      cursorChar: "|",
    });
  },
};
</script>
<script>
  export let theme = "default"
</script>

<div class={theme}><slot /></div>

<style>
  .default {
    /* Color */
    --white: #fff;

    --green-50: #edfcf2;
    --green-100: #d3f8df;
    --green-500: #16b364;

    --blue-50: #eff8ff;
    --blue-100: #d1e9ff;
    --blue-500: #2e90fa;

    --orange-50: #fef6ee;
    --orange-100: #fdead7;
    --orange-500: #ef6820;

    --gray-50: #f8fafc;
    --gray-400: #9aa4b2;
    --gray-600: #4b5565;
    --gray-700: #364152;

    /* Font */
    --font-family: "Inter", -apple-system, BlinkMacSystemFont, "Segoe UI",
      Roboto, Helvetica, Arial, sans-serif, "Apple Color Emoji",
      "Segoe UI Emoji", "Segoe UI Symbol";

    /* Text for Displays */
    --display-487: bold 3rem/1.25 var(--font-family);

    --text-204: normal 1.25rem/1.5 var(--font-family);
    --text-206: 600 1.25rem/1.5 var(--font-family);
    --text-207: bold 1.25rem/1.5 var(--font-family);

    --text-165: medium 1rem/1.5 var(--font-family);
    --text-167: bold 1rem/1.5 var(--font-family);

    /* Sizing */
    --size-4: 0.25rem;
    --size-8: 0.5rem;
    --size-12: 0.75rem;
    --size-16: 1rem;
    --size-20: 1.25rem;
    --size-24: 1.5rem;
    --size-32: 2rem;
    --size-40: 2.5rem;
    --size-48: 3rem;
    --size-64: 4rem;
    --size-80: 5rem;
    --size-96: 6rem;
    --size-128: 8rem;
    --size-160: 10rem;
    --size-192: 12rem;
    --size-224: 14rem;
    --size-256: 16rem;

    /* Shadows */
    --shadow-small: 0px 1px 3px rgba(16, 24, 40, 0.1),
      0px 1px 2px rgba(16, 24, 40, 0.06);
    --shadow-medium: 0px 4px 8px -2px rgba(16, 24, 40, 0.1),
      0px 2px 4px -2px rgba(16, 24, 40, 0.06);
    --shadow-large: 0px 12px 16px -4px rgba(16, 24, 40, 0.08),
      0px 4px 6px -2px rgba(16, 24, 40, 0.03);

    /* Border Radius */
    --radius-8: 8px;
  }
</style>

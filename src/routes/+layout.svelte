<script>
  import "../app.css";
</script>

<main class="bg-background text-text">
  <slot />
  <div class="flex justify-center py-2 px-8 sm:justify-end">
    <a class="pr-8 text-primary hover:underline" href="/">Home</a>
    <a class="pr-8 text-primary hover:underline" href="/translations"
      >Translations</a
    >
    <a
      class="pr-8 text-primary hover:underline"
      href="https://docs.google.com/forms/d/e/1FAIpQLSdKDaYchJ-g8Ly2xMAXb-PDRVG47yEHG1EVL8XdQVB7_a1a3Q/viewform?usp=sf_link"
      >Feedback</a
    >
    <a class="pr-8 text-primary hover:underline" href="/privacy">Privacy</a>
    <a class="text-primary hover:underline" href="/terms">Terms</a>
  </div>
</main>

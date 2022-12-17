<script>
  import "../app.css";
</script>

<main class="bg-background text-text">
  <slot />
  <div class="flex py-2 px-8 justify-center sm:justify-end">
    <a class="hover:underline text-primary pr-8" href="/">Home</a>
    <a class="hover:underline text-primary pr-8" href="/translations"
      >Translations</a
    >
    <a
      class="hover:underline text-primary pr-8"
      href="https://docs.google.com/forms/d/e/1FAIpQLSdKDaYchJ-g8Ly2xMAXb-PDRVG47yEHG1EVL8XdQVB7_a1a3Q/viewform?usp=sf_link"
      >Feedback</a
    >
    <a class="hover:underline text-primary pr-8" href="/privacy">Privacy</a>
    <a class="hover:underline text-primary" href="/terms">Terms</a>
  </div>
</main>

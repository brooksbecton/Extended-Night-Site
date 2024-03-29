<script>
  import Feature from "../components/Feature.svelte";
  import Lazy from "../components/Lazy.svelte";

  import encLogo from "../assets/encLogo.svg";
  import iosBadge from "../assets/badge-app-store.svg";
  import googleBadge from "../assets/badge-google-play.svg";
  import webBadge from "../assets/web.svg";

  const delayModuleLoad = (module) =>
    new Promise((res) => setTimeout(() => res(module), Math.random() * 2000));

  const Snow = () => import("../components/Snow.svelte").then(delayModuleLoad);
</script>

<div class="bg-grey-300 SnowContainer relative">
  <div
    class="absolute top-0 left-0 right-0 bottom-0 flex flex-col items-center justify-center"
  >
    <div
      class="flex  w-2/3 flex-col items-center text-center md:w-1/2 lg:w-1/3"
    >
      <img src={encLogo} alt="Extended Night Companion Logo" />
      <p class="text-md">
        A companion app for <br class="inline md:hidden" />
        <a
          class="text-primary hover:underline"
          href="https://www.thelongdark.com/"
          target="_blank"
          rel="noreferrer">The Long Dark®</a
        >
      </p>
    </div>
    <div
      class="mt-6 flex flex-col items-center justify-center space-y-2  md:flex-row md:space-y-0"
    >
      <a
        class="z-10  mr-0 md:mr-4"
        href="https://app.extendednightcompanion.com/"
      >
        <img
          height="40"
          src={webBadge}
          style="height: 40px"
          alt="Use the web application"
        />
      </a>
      <a
        class="z-10  mr-0 md:mr-4"
        href="https://apps.apple.com/us/app/extended-night-companion-app/id1554875268"
      >
        <img
          height="40"
          width="135"
          src={iosBadge}
          alt="Download on the App Store"
        />
      </a>
      <a
        class="z-10"
        href="https://play.google.com/store/apps/details?id=com.broabect.greatnorthguide"
      >
        <img
          height="40"
          width="135"
          src={googleBadge}
          alt="Get it on Google Play"
        />
      </a>
    </div>
  </div>

  <Lazy component={Snow} />
</div>

<div class="Topography flex flex-col items-center bg-background py-8 text-text">
  <!-- Review Section -->
  <div class="flex w-5/6 flex-1 flex-col xl:w-3/6">
    <h1 class="mb-4 text-2xl">What people think</h1>

    <div class="flex  flex-col md:flex-row">
      <div
        class="flex w-full flex-col items-center justify-center text-center md:w-1/4"
      >
        <p class="text-3xl">5 stars</p>
        <div class="mb-3 flex">
          <svg style="width: 24px; height: 24px" viewBox="0 0 24 24">
            <path
              fill="currentColor"
              d="M12,17.27L18.18,21L16.54,13.97L22,9.24L14.81,8.62L12,2L9.19,8.62L2,9.24L7.45,13.97L5.82,21L12,17.27Z"
            />
          </svg>
          <svg style="width: 24px; height: 24px" viewBox="0 0 24 24">
            <path
              fill="currentColor"
              d="M12,17.27L18.18,21L16.54,13.97L22,9.24L14.81,8.62L12,2L9.19,8.62L2,9.24L7.45,13.97L5.82,21L12,17.27Z"
            />
          </svg>
          <svg style="width: 24px; height: 24px" viewBox="0 0 24 24">
            <path
              fill="currentColor"
              d="M12,17.27L18.18,21L16.54,13.97L22,9.24L14.81,8.62L12,2L9.19,8.62L2,9.24L7.45,13.97L5.82,21L12,17.27Z"
            />
          </svg>
          <svg style="width: 24px; height: 24px" viewBox="0 0 24 24">
            <path
              fill="currentColor"
              d="M12,17.27L18.18,21L16.54,13.97L22,9.24L14.81,8.62L12,2L9.19,8.62L2,9.24L7.45,13.97L5.82,21L12,17.27Z"
            />
          </svg>
          <svg style="width: 24px; height: 24px" viewBox="0 0 24 24">
            <path
              fill="currentColor"
              d="M12,17.27L18.18,21L16.54,13.97L22,9.24L14.81,8.62L12,2L9.19,8.62L2,9.24L7.45,13.97L5.82,21L12,17.27Z"
            />
          </svg>
        </div>
        <p>254 Ratings</p>
      </div>

      <div class="flex w-full flex-col md:w-3/4">
        <div class="flex-1 flex-col md:flex">
          <div class="flex flex-1 flex-col">
            <ul>
              <li class="flex flex-1 ">
                <quote class="px-0 py-4 italic sm:p-4">
                  Amazing companion app. I used to spend way too much time
                  trying to pull up different maps and half the time they were
                  either blurry or outdated. This is exactly what I needed.
                  Phenomenal job!
                  <br />
                  <span class="ml-2">- Maxwell O'Brien</span>
                </quote>
              </li>
              <li class="flex flex-1 ">
                <quote class="px-0 py-4 italic sm:p-4">
                  This app is amazing. You can keep track of challenges, badges,
                  and feats. There are maps for all the regions. It's a great
                  companion app. I use it a evertime I play.
                  <br />
                  <span class="ml-2">- Jennifer Ghramm</span>
                </quote>
              </li>
              <li class="flex flex-1 ">
                <quote class="px-0 py-4 italic sm:p-4">
                  Very useful. You have the option to have the maps display
                  locations/items/etc, or leave it devoid of any information
                  beyond the map itself if you still want to discover everything
                  on your own. Very considerate, and helpful for all skill
                  levels. A great app!
                  <br />
                  <span class="ml-2">- Michael Otineru</span>
                </quote>
              </li>
            </ul>
          </div>
          <div class="flex justify-end">
            <a
              class="mr-4 text-primary  hover:underline"
              href="https://play.google.com/store/apps/details?id=com.broabect.greatnorthguide&showAllReviews=true"
              >More Android Reviews</a
            >
            <a
              class="text-primary hover:underline"
              href="https://apps.apple.com/us/app/extended-night-companion-app/id1554875268?see-all=reviews"
              >More iOS Reviews</a
            >
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- Features Section -->
  <Feature />
</div>

<style>
  .SnowContainer {
    background: radial-gradient(ellipse at bottom, #1b2735 0%, #090a0f 100%);

    overflow: hidden;

    height: 40vh;
  }

  @media (min-width: 768px) {
    .SnowContainer {
      height: 50vh;
    }
  }
</style>

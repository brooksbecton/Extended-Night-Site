<script lang="ts">
  import journalShot from "../assets/journalShot.png";
  import mapShot from "../assets/mapShot.png";
  import trophyShot from "../assets/trophyShot.png";

  type Feature = "maps" | "journals" | "trophies";

  let selectedFeature: Feature = "maps";
  const featureImageMap: Record<
    Feature,
    {
      image: string;
      altText: string;
    }
  > = {
    maps: {
      image: mapShot,
      altText: "Mystery Lake map with 6 custom pins dropped in it in the app",
    },
    journals: {
      image: journalShot,
      altText: "A list of 5 journal entries in the app",
    },
    trophies: {
      image: trophyShot,
      altText: "A list of The Long Dark trophies with checkboxes next to each",
    },
  };

  const setSelectedFeature = (newFeature: Feature) => {
    selectedFeature = newFeature;
  };
</script>

<div
  class="flex flex-col h-full pt-9 w-5/6 xl:w-3/6 sm:flex-row sm:justify-between"
>
  <div
    class="flex flex-row flex-1 justify-between sm:flex-col sm:justify-start"
  >
    <div class="flex flex-col">
      <button
        class:bg-surface={selectedFeature === "maps"}
        on:click={() => setSelectedFeature("maps")}
        class="flex py-2 flex-col rounded-xl hover:bg-surface items-center sm:flex-row"
      >
        <div class="flex flex-1 flex-col items-center px-4">
          <svg style="width: 64px; height: 64px" viewBox="0 0 24 24">
            <path
              fill="currentColor"
              d="M15,19L9,16.89V5L15,7.11M20.5,3C20.44,3 20.39,3 20.34,3L15,5.1L9,3L3.36,4.9C3.15,4.97 3,5.15 3,5.38V20.5A0.5,0.5 0 0,0 3.5,21C3.55,21 3.61,21 3.66,20.97L9,18.9L15,21L20.64,19.1C20.85,19 21,18.85 21,18.62V3.5A0.5,0.5 0 0,0 20.5,3Z"
            />
          </svg>
          <h2 class="text-xl">Maps</h2>
        </div>
      </button>
      <p class="hidden sm:flex mt-2">
        Explore maps from all regions with the ability to drop pins on maps to
        remember items you dropped or places you've travelled
      </p>
    </div>
    <div class="flex flex-col">
      <button
        class:bg-surface={selectedFeature === "journals"}
        on:click={() => setSelectedFeature("journals")}
        class="flex py-2 flex-col rounded-xl hover:bg-surface items-center sm:flex-row sm:mt-4"
      >
        <div class="flex flex-1 flex-col items-center px-4">
          <svg style="width: 64px; height: 64px" viewBox="0 0 24 24">
            <path
              fill="currentColor"
              d="M6,4H11V12L8.5,10.5L6,12M18,2H6A2,2 0 0,0 4,4V20A2,2 0 0,0 6,22H18A2,2 0 0,0 20,20V4A2,2 0 0,0 18,2Z"
            />
          </svg>
          <h2 class="text-xl">Journals</h2>
        </div>
      </button>
      <p class="hidden sm:flex mt-2">
        Track what you are doing during your run with journal entries. Keep up
        with where you are, what you were doing, and what items you have in each
        entry.
      </p>
    </div>
    <div class="flex flex-col">
      <button
        class:bg-surface={selectedFeature === "trophies"}
        on:click={() => setSelectedFeature("trophies")}
        class="flex py-2 flex-col rounded-xl hover:bg-surface items-center sm:flex-row sm:mt-4"
      >
        <div class="flex flex-1 flex-col items-center px-4">
          <svg style="width: 64px; height: 64px" viewBox="0 0 24 24">
            <path
              fill="currentColor"
              d="M18 2C17.1 2 16 3 16 4H8C8 3 6.9 2 6 2H2V11C2 12 3 13 4 13H6.2C6.6 15 7.9 16.7 11 17V19.08C8 19.54 8 22 8 22H16C16 22 16 19.54 13 19.08V17C16.1 16.7 17.4 15 17.8 13H20C21 13 22 12 22 11V2H18M6 11H4V4H6V11M20 11H18V4H20V11Z"
            />
          </svg>
          <h2 class=" text-xl">Trophy</h2>
        </div>
      </button>
      <p class="hidden sm:flex mt-2">
        Record what trophys you have earned in the game. Also create your own
        custom trophies.
      </p>
    </div>
  </div>

  <div
    class=" w-full pt-4  justify-center items-center  sm:flex sm:w-1/2 sm:pl-8  sm:pt-0 sm:items-start"
  >
    <img
      src={featureImageMap[selectedFeature].image}
      alt={featureImageMap[selectedFeature].altText}
    />
  </div>
  {#if selectedFeature === "maps"}
    <p class="flex sm:hidden mt-4 text-center">
      Explore maps from all regions with the ability to drop pins on maps to
      remember items you dropped or places you've travelled
    </p>
  {/if}
  {#if selectedFeature === "journals"}
    <p class="flex sm:hidden mt-4 text-center">
      Track what you are doing during your run with journal entries. Keep up
      with where you are, what you were doing, and what items you have in each
      entry.
    </p>
  {/if}
  {#if selectedFeature === "trophies"}
    <p class="flex sm:hidden mt-4 text-center">
      Record what trophys from the game you have earned or challenge yourself
      and create your own trophies to complete.
    </p>
  {/if}
</div>

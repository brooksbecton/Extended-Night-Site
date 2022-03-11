<!-- https://svelte.dev/repl/09abb8c287f745169f66f62d51f766d5?version=3.46.4 -->
<script>
    import { onMount } from "svelte";
  
    export let component;
    export let delayMs = null;
  
    let loadedComponent = null;
    let timeout;
    let showFallback = !delayMs;
  
    let props;
    $: {
      const { component, delayMs, ...restProps } = $$props;
      props = restProps;
    }
  
    onMount(() => {
      if (delayMs) {
        timeout = setTimeout(() => {
          showFallback = true;
        }, delayMs);
      }
      component().then(module => {
        loadedComponent = module.default;
      });
      return () => clearTimeout(timeout);
    });
  </script>
  
  {#if loadedComponent}
    <svelte:component this={loadedComponent} {...props} />
  {:else if showFallback}
    <slot />
  {/if}
  
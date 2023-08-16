<script>
  import { getContext } from "svelte"
  import { useLazyImage as lazyImage } from 'svelte-lazy-image';

  export let imgSrc
  export let imgAltText = "Assessment Capture"
  export let size

  const { styleable } = getContext("sdk")
  const component = getContext("component")
</script>


  <img data-src={imgSrc} alt={imgAltText} use:lazyImage style="width:{size}; height:{size}; object-fit: cover; border-radius: 10%"/>

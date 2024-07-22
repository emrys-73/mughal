<script>
// @ts-nocheck

    import { responsiveImage } from 'svelte-image';
  
    export let src;
    export let alt = '';
  </script>
  
  <!-- svelte-ignore component-name-lowercase -->
  <responsiveImage
    src={src}
    alt={alt}
    sizes="(max-width: 600px) 100vw, (max-width: 900px) 50vw, 33vw"
    formats={['webp', 'jpeg']}
  />
  
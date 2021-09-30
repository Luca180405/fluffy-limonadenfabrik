<script>
    import { url } from '@roxi/routify'
</script>

<style>
  .huge {
    font-size: 12rem;
  }
  .e404 {
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
  }
</style>

<div class="e404">
  <div class="text-red-800 huge">404</div>
  <div class="text-red-800 big">Page not found. 
  <!-- link to the parent folder of _fallback.svelte -->
  <a href={$url('../')}>Go back</a> <br>
  <div class="font-semibold">Have a ☕ and look at the problem.</div>
  </div>
</div>

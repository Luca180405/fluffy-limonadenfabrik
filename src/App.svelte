<script>
  import { Router } from "@roxi/routify";
  import { routes } from "../.routify/routes";
</script>

<Router {routes} />

<style global>
  @import "./global.css";
  @tailwind base;
  @tailwind components;
  @tailwind utilities;  
</style> 
<script>
    import { metatags } from '@roxi/routify'
    
    metatags.title = 'Fluffy - Rezepte🤫'
    metatags.description = 'Description coming soon...'
    
    let products = [
      {name: "Der magische Trunk", image: "/img/magischer_trunk.jpg", page: "./rezepte/dermagischetrunk"},
      {name: "Der schnelle Läufer", image: "/img/schneller_laeufer.jpg", page: "./rezepte/derschnellelaeufer"},
      {name: "Der Erfrischer", image: "/img/lemonade.jpg", page: "./rezepte/dererfrischer"},
    ]
</script>

    <div class="bg-gray-200 bg-opacity-30">
      <img src="public/img/barkeeper.webp" alt="Barkeeper" style="height: 256px; width:auto;" class="center mt-10"/>
        <h1 class="pt-12 font-sans text-5xl font-bold text-center">
            Rezepte
        </h1>
        
        <p class="block text-center pb-7 pt-9">
            Fluffy-Limonade entspricht dem Trend nach natürlicher und gesunder Ernährung: Ein alkoholfreies Erfrischungsgetränk, das durch auf natürliche Art hergestellt wird. Fluffy-Limonade ist von Haus aus calciumreich aber natriumarm. Mit den enthaltenen Mineralien stellt es ein wichtigen Baustein zur gesunden Ernährung dar, und dieses Tag für Tag Jüngste Forschungsergebnisse haben gezeigt, dass Fluffylimonade überaus geeignet ist die tägliche Versorgung mit Mineralstoffen und Spurenelementen sicherzustellen.
        </p>
    </div>


<div class="flex p-6 pb-12">
    
{#each products as product}
<a href= {product.page} class="hover:scale-105">
<div class="shadow-md rounded-md overflow-hidden relative mr-5" style="width: 350px">
  <img
    src={product.image}
    class=""
    alt= {product.name}
  />

  <div class="p-4">
    <h5 class="text-xl font-semibold mb-2">{product.name}</h5>
  </div>
</div>
</a>
{/each}

</div>
<script>
    import { metatags } from '@roxi/routify'
    
    metatags.title = 'Fluffy - Rezepte🤫'
    metatags.description = 'Description coming soon...'
    
    let products = [
      {name: "Der magische Trunk", description: "Hierfür werden eine frische Apfelsine, ein Apfel, ein wenig Zimt, etwas Ingwer und Fluffy Orangenlimonade gebraucht. Apfelsine und Apfel schälen und klein schneiden und mit der Fluffy Orangenlimonade verrühren. Zum Abschluss mit Zimt und Ingwer verfeinern.", 
      image: "/img/magischer_trunk.jpg"},
      {name: "Der schnelle Läufer", description: "Hierfür benötigen Sie eine Limette, etwas Kümmel und Fluffy Bitterlemon. Limette waschen und kleinschneiden, etwas Kümmel hinzugeben und zum Abschluss mit Fluffy Bitterlemon auffüllen. Mmmh, das schmeckt und gibt starke Beine.", 
      image: "/img/schneller_laeufer.jpg"},
      {name: "Der Erfrischer", description: "Hierfür benötigen Sie eine Zitrone, viel Eis und eine Dose Fluffygetränkedose (Zitrone oder Orange). Zitrone durchschneiden und ausdrücken, Eis bis zum Glasrand und zum Abschluss mit Fluffy aufgießen. Das erfrischt für den ganzen Tag!", 
      image: "/img/lemonade.jpg"},
    ]
</script>

    <div class="bg-gray-200 bg-opacity-30">
        <h1 class="pt-12 font-sans text-5xl font-bold text-center">
            Rezepte
        </h1>
        
        <p class="block text-center pb-7 pt-9">
            Fluffy-Limonade entspricht dem Trend nach natürlicher und gesunder Ernährung: Ein alkoholfreies Erfrischungsgetränk, das durch auf natürliche Art hergestellt wird. Fluffy-Limonade ist von Haus aus calciumreich aber natriumarm. Mit den enthaltenen Mineralien stellt es ein wichtigen Baustein zur gesunden Ernährung dar, und dieses Tag für Tag Jüngste Forschungsergebnisse haben gezeigt, dass Fluffylimonade überaus geeignet ist die tägliche Versorgung mit Mineralstoffen und Spurenelementen sicherzustellen.
        </p>
    </div>


<div class="flex p-6 pb-12">
    
{#each products as product}
<a href="/rezepte/dermagischetrunk" class="relative max-w-sm overflow-hidden rounded shadow-md right-10 hover:shadow-2xl hover:scale-105">
  <img class="w-auto h-3/6" src="{product.image}" alt="Rezept">
  <div class="px-6 py-4">
          <div class="mb-2 text-xl font-bold">{product.name}</div>
    <p class="block text-base text-gray-700">
      {product.description}
    </p>
  </div>
</a>
{/each}
      
</div>

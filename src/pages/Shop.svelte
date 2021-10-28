<script>
    import { metatags } from '@roxi/routify'
    
    metatags.title = 'Fluffy einkaufen'
    metatags.description = 'Description coming soon...'
    
    let products = [
      {name: "Fluffy Getränkedosen", image: "/img/limo1.png", price: "0,99€", label: "Fluffy Getränkedosen", page: "/produkte/fluffy-getraenkedosen"},
      {name: "Erzi Getränkedosen", image: "/img/limo_erzi.png", price: "1,49€", label: "Erzi Getränkedosen", page:"/produkte/erzi-getraenkedosen"},
      {name: "TAU Orange-Limonade", image: "/img/limo6.png", price: "8,99€", label: "TAU Orange-Limonade", page:"/produkte/tau-orange-limonade"},
      {name: "Fluffy Mehrwegkiste", image: "/img/limo_kiste.png.bak", price: "7,99€", label: "Fluffy Mehrwegkiste", page:"/produkte/fluffy-mehrwegkiste"},
      {name: "Fluffy Familienglück", image: "/img/limo3.png", price: "2,99€", label: "Fluffy Familienglück", page:"/produkte/fluffy-familienglueck"},
      {name: "Bionade", image: "/img/limo5.png", price: "1,99€", label: "Bionade", page:"/produkte/Bionade"},
      {name: "Fluffy Bitter Lemon", image: "/img/bitter_lemon.png", price: "3,99€", label: "Fluffy Bitter Lemon", page:"/produkte/bitter-lemon"},
      {name: "Fluffy Sekt", image: "/img/limo2.gif", price: "6,99€", label: "Fluffy Sekt", page:"/produkte/fluffy-sekt"},
    ]
</script>

<div class="bg-gray-50">
  <div class="max-w-2xl px-4 mx-auto py-14 sm:py-24 sm:px-6 lg:max-w-7xl lg:px-8">
    <h2 class="text-2xl font-extrabold tracking-tight text-gray-900">Bei Fluffy einkaufen</h2>

    <div class="grid grid-cols-1 mt-6 gap-y-10 gap-x-6 sm:grid-cols-2 lg:grid-cols-4 xl:gap-x-8">
{#each products as product}
<div class="relative group">
  <div class="w-full overflow-hidden bg-gray-200 rounded-md min-h-80 aspect-w-1 aspect-h-1 group-hover:opacity-75 lg:h-80 lg:aspect-none">
    <img src="{product.image}" alt={product.label} class="w-auto h-64 pt-12 center sm:pb-5">
  </div>
  <div class="flex justify-between mt-4">
    <div>
      <h3 class="text-sm text-gray-700">
        <a href="{product.page}">
          <span aria-hidden="true" class="absolute inset-0"></span>
          {product.name}
        </a>
      </h3>
    </div>
    <p class="text-sm font-medium text-gray-900">2,99€</p>
  </div>
</div>
{/each}
    </div>
  </div>
</div>
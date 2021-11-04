<script>
    import { metatags } from '@roxi/routify'
    
    metatags.title = 'Fluffy einkaufen'
    metatags.description = 'Description coming soon...'


  export  let products = [
      {id: "1", name: "Fluffy Getränkedosen", image: "/img/limo1.png", price: "0,99€", label: "Fluffy Getränkedosen", page: "/produkte/fluffy-getraenkedosen", quantity: "1"},
      {id: "2",name: "Erzi Getränkedosen", image: "/img/limo_erzi.png", price: "1,49€", label: "Erzi Getränkedosen", page:"/produkte/erzi-getraenkedosen", quantity: "1"},
      {id: "3",name: "TAU Orange-Limonade", image: "/img/limo6.png", price: "8,99€", label: "TAU Orange-Limonade", page:"/produkte/tau-orange-limonade", quantity: "1"},
      {id: "4",name: "Fluffy Mehrwegkiste", image: "/img/limo_kiste.png.bak", price: "7,99€", label: "Fluffy Mehrwegkiste", page:"/produkte/fluffy-mehrwegkiste", quantity: "1"},
      {id: "5",name: "Fluffy Familienglück", image: "/img/limo3.png", price: "2,99€", label: "Fluffy Familienglück", page:"/produkte/fluffy-familienglueck", quantity: "1"},
      {id: "6",name: "Bionade", image: "/img/limo5.png", price: "1,99€", label: "Bionade", page:"/produkte/Bionade", quantity: "1"},
      {id: "7",name: "Fluffy Bitter Lemon", image: "/img/bitter_lemon.png", price: "3,99€", label: "Fluffy Bitter Lemon", page:"/produkte/bitter-lemon", quantity: "1"},
      {id: "8",name: "Fluffy Sekt", image: "/img/limo2.gif", price: "6,99€", label: "Fluffy Sekt", page:"/produkte/fluffy-sekt", quantity: "1"},
    ]

</script>



<div class="bg-gray-50">
  <div class="max-w-2xl px-4 mx-auto py-16 sm:py-24 sm:px-6 lg:max-w-7xl lg:px-8">
    <h2 class="text-2xl font-extrabold  tracking-tight  text-gray-900">Bei Fluffy einkaufen</h2>

    <div class="grid grid-cols-1 mt-6 gap-y-10 gap-x-6 sm:grid-cols-2 lg:grid-cols-4 xl:gap-x-8">
{#each products as product}
<div class="relative group">
  <div class="w-full overflow-hidden bg-gray-200 rounded-md min-h-80 aspect-w-1 aspect-h-1 lg:h-80 lg:aspect-none">
    <img src="{product.image}" alt={product.label} class="w-auto h-64 pt-12 center sm:pb-5"/>
  </div>
  <div class="flex justify-between mt-4">
    <div>
      <a href="{product.page}" class="cursor-default">
      <h3 class="text-sm text-gray-700">
          <span aria-hidden="true" class="absolute inset-0"></span>
          {product.name}
      </h3>
      </a>
    </div>
  </div>
  <button class="bg-gray-300 hover:bg-gray-400 text-gray-800 font-bold py-2 px-4 rounded inline-flex items-center add-cart">
    <svg class="fill-current w-4 h-4 mr-2" xmlns="http://www.w3.org/2000/svg" width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="#000000" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><circle cx="10" cy="20.5" r="1"/><circle cx="18" cy="20.5" r="1"/><path d="M2.5 2.5h3l2.7 12.4a2 2 0 0 0 2 1.6h7.7a2 2 0 0 0 2-1.6l1.6-8.4H7.1"/></svg>
    <span>In den Warenkorb</span>
  </button>
    <p class="text-sm font-medium text-gray-900">{product.price}</p>
  </div>
{/each}
    </div>
  </div>
</div>

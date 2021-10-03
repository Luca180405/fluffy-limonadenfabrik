<script>
    import { metatags } from '@roxi/routify'
    
    metatags.title = 'Fluffy - die spritzige Limonade🍹'
    metatags.description = 'Description coming soon...'
    
    const data = {};
    let isVisible = true;
    
    function onSubmit(e) {
    const formData = new FormData(e.target);

    for (let field of formData) {
      const [key, value] = field;
      data[key] = value;
    }
    console.log(data)
    
    if(data.num === "3") {
        isVisible = false;
    }
    
  }
</script>


<img class="w-1/5 pt-4 h-1/5 center" src="/img/orangejuice.png" alt="Fluffy Logo">
<h1 class="py-10 text-2xl font-bold text-center text-yellow-500">Willkommen bei Fluffy, dem leckeren, spritzigen Erfrischungsgetränk!</h1>

<div class="text-center">
    <h2 class="pb-3 text-lg font-semibold text-gray-900 sm:text-lg lg:text-2xl">Gewinnspiel</h2>
    <p class="pb-5 text-gray-600">Machen Sie mit und Sie erhalten die Chance auf wertvolle Preise:</p>
    <ul class="list-decimal ">
        <li>Preis: Eine Reise in den Harz</li>
        <li>Preis: Ein Jahr ein Monatsabo an Limonade</li>
        <li>Preis: Ein Warengutschein über 50 Euro für alle Produkte der Fluffy-GmbH</li>
    </ul>
    <p class="pt-6 pb-5 ">Teilnehmen kann jeder der mindestens 18 Jahre alt ist. Mitmachen kann man noch bis zum 31.10.2007.</p>
</div>
<div class="text-center">
    <p class="pb-2 font-semibold">Die Preisfrage lautet:</p>
    <p class="cursor-wait hover:text-red-800">Wieviele Mitarbeiter hat die Fluffy GmbH zur Zeit?</p>
</div>

{#if isVisible === true}
<form class="pt-4 text-center" on:submit|preventDefault={onSubmit}>
    <input type="radio" id="1" name="num" value="1">
    <label for="1">1</label><br>
    <input type="radio" id="3" name="num" value="3">
    <label for="3">3</label><br>
    <input type="radio" id="5" name="num" value="5">
    <label for="5">5</label> 
    <br>
    <input class="w-20 mt-3 mb-2 font-semibold bg-yellow-400 rounded-lg cursor-pointer hover:bg-yellow-300 h-7" type="submit" value="Auflösen">
</form>
{/if}


{#if data.num === "3"}
<div class="text-center">
    <h1 class="pt-5">🎉<span class="text-semibold">Richtig</span>, Fluffy hat 3 Mitarbeiter🎉</h1>
    <form action="/">
        <input class="w-16 mt-3 mb-2 font-semibold bg-yellow-400 rounded-lg cursor-pointer hover:bg-yellow-300 h-7" type="submit" value="Zurück">
    </form>
</div>
{:else if data.num < 3}
<h1 class="text-center">❌Falsch❌</h1>
{:else if data.num > 3}
<h1 class="text-center">❌Falsch❌</h1>
{/if}

<p class="pt-5 text-center pb-9"><b>Viel Erfolg!</b></p>
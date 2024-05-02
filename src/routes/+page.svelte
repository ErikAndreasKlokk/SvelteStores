<script>

</script>

<main class=" w-screen min-h-screen flex items-center flex-col">
    <h1 class=" text-6xl font-bold text-white my-6">Svelte Stores</h1>
    <!-- Inni diven under kan du putte knappen! -->
    <div>
        
    </div>
    <div class=" text-white mt-6 space-y-3 md:max-w-[60vw] mb-20">
        <p>Start med å lage en mappe inni lib mappen som heter "stores". Deretter skal du lage en "store.js" fil inni den nye stores mappen.</p>
        <p>Inni "store.js" kan du kopiere koden nedenfor.</p>
        <div class=" bg-gray-800 w-fit p-3 rounded-lg flex h-fit">
            <div class=" pr-4 mr-3 border-r border-r-gray-500 text-gray-300 font-light text-sm flex justify-between flex-col">
                <p>1</p>
                <p>2</p>
                <p>3</p>
            </div>
            <div class=" leading-tight ">
                <p>import { "{ writable }" } from 'svelte/store';</p>
                <br>
                <p>export const store = writable({'{num: 0}'});</p>
            </div>
        </div>
        <p>Du har nå laget din første writeable svelte store. Det finnes flere forskjellige stores, men writeable er den mest relevante.</p>
        <br>
        <p>For å bruke denne nye svelte storen, må vi importere den til filen vi vil bruke den i. Hvis du kopierer koden under, i script taggen øverst i filen, vil du importere storen.</p>
        <div class=" bg-gray-800 w-fit p-3 rounded-lg flex h-fit">
            <div class=" pr-4 mr-3 border-r border-r-gray-500 text-gray-300 font-light text-sm flex justify-between flex-col">
                <p>1</p>
            </div>
            <div class=" leading-tight ">
                <p>import {'{ store }'} from '../lib/stores/store.js'</p>
            </div>
        </div>
        <p>Nå når du har importert storen, må vi bruke den på en eller annen måte. For å gjøre dette bruker vi JavaScript på en knapp, for å oppdatere storen, og legge til 1 hver gang vi trykker på knappen.</p>
        <p>For å lage knappen kan du kopiere koden under og putte den i "knappdiven" jeg har laget.</p>
        <div class=" bg-gray-800 w-fit p-3 rounded-lg flex h-fit">
            <div class=" pr-4 mr-3 border-r border-r-gray-500 text-gray-300 font-light text-sm flex justify-between flex-col">
                <p>1</p>
            </div>
            <div class=" leading-tight ">
                <p>{'<button on:click={() => updateStore()} class=" bg-gray-500 text-white p-3 rounded-lg m-3">Knapp</button>'}</p>
            </div>
        </div>
        <p>Denne koden vil gi en error, fordi at du ikke har laget funksjonen til å oppdatere svelte storen.</p>
        <p>Det kan vi veldig lett fikse ved å kopiere koden under, i {'<script>'} taggen øverst i koden.</p>
        <div class=" bg-gray-800 w-fit p-3 rounded-lg flex h-fit">
            <div class=" pr-4 mr-3 border-r border-r-gray-500 text-gray-300 font-light text-sm flex justify-between flex-col">
                <p>1</p>
                <p>2</p>
                <p>3</p>
                <p>4</p>
                <p>5</p>
                <p>6</p>
            </div>
            <div class=" leading-tight ">
                <p>{'function updateStore() {'}</p>
                <p class=" ml-7">{'store.set({'}</p>
                <p class=" ml-14">{'num: $store.num + 1'}</p>
                <p class=" ml-7">{'})'}</p>
                <p class=" ml-7">{'console.log($store)'}</p>
                <p>{'}'}</p>
            </div>
        </div>
        <p>Når du nå trykker på knappen, vil du se i consolen at tallet går oppover hver gang du trykker.</p>
        <p>For å se tallet på en side, kan du gå inn i mappen som heter OppdatertVariabel og åpne +page.svelte siden. Her skal vi legge inn det oppdaterte tallet som kommer fra svelte storen.</p>
        <p>Vi starter med å importere svelte storen.</p>
        <div class=" bg-gray-800 w-fit p-3 rounded-lg flex h-fit">
            <div class=" pr-4 mr-3 border-r border-r-gray-500 text-gray-300 font-light text-sm flex justify-between flex-col">
                <p>1</p>
            </div>
            <div class=" leading-tight ">
                <p>import {'{ store }'} from '../../lib/stores/store.js'</p>
            </div>
        </div>
        <p>I diven kan du kopiere koden under.</p>
        <div class=" bg-gray-800 w-fit p-3 rounded-lg flex h-fit">
            <div class=" pr-4 mr-3 border-r border-r-gray-500 text-gray-300 font-light text-sm flex justify-between flex-col">
                <p>1</p>
            </div>
            <div class=" leading-tight ">
                <p>{'<p class=" text-white font-extrabold text-8xl">{$store.num}</p>'}</p>
            </div>
        </div>
        <p>Gratulerer! Du har nå laget en global variabel som du kan oppdatere hver gang du trykker på en knapp. Hvis du vil lese mer om svelte stores kan du se her: <a class=" underline font-bold" href="https://svelte.dev/docs/svelte-store" target="_blank">Svelte Stores</a></p>
    </div>
</main>
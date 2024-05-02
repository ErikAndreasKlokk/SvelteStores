<script>
    import { store } from '../lib/stores/store.js'
</script>

<main class=" w-screen h-screen flex items-center flex-col">
    <h1 class=" text-6xl font-bold text-white mt-6">Svelte Stores</h1>
    <!-- Inni diven under kan du putte knappen! -->
    <div class=" ">
        <button on:click={$store = $store + 1} class=" bg-gray-500 text-white p-3 rounded-lg m-3">Knapp</button>
    </div>
    <div class=" text-white mt-6 space-y-3 md:max-w-[60vw]">
        <p>Start med å lage en mappe inni lib mappen som heter stores. Deretter skal du lage en store.js fil inni den nye stores mappen.</p>
        <p>Inni store.js kan du kopiere koden nedenfor.</p>
        <div class=" bg-gray-800 w-fit p-3 rounded-lg flex h-fit">
            <div class=" pr-4 mr-3 border-r border-r-gray-500 text-gray-300 font-light text-sm flex justify-between flex-col">
                <p>1</p>
                <p>2</p>
                <p>3</p>
            </div>
            <div class=" leading-tight ">
                <p>import { "{ writable }" } from 'svelte/store';</p>
                <br>
                <p>export const store = writable();</p>
            </div>
        </div>
        <p>Du har nå laget din første writeable svelte store. Det finnes flere forskjellige stores, men writeable er den mest relevante.</p>
        <br>
        <p>For å bruke denne nye svelte storen, må vi importere den til filen vi vil bruke den i. Hvis du kopierer koden under, i script taggen øverst i filen, vil du importere storen.</p>
        <div class=" bg-gray-800 w-fit p-3 rounded-lg flex h-fit">
            <div class=" pr-4 mr-3 border-r border-r-gray-500 text-gray-300 font-light text-sm flex justify-between flex-col">
                <p>2</p>
            </div>
            <div class=" leading-tight ">
                <p>import {'{ store }'} from '../lib/stores/store.js'</p>
            </div>
        </div>
        <p>Nå når du har importert storen, må vi bruke den på en eller annen måte. For å gjøre dette bruker vi JavaScript på en knapp, for å oppdatere storen, og legge til 1 hver gang vi trykker på knappen.</p>
        
    
    </div>
</main>
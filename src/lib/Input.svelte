<script>
import { arrList } from '../../store.js';
import Value from '../lib/Value.svelte';
let value = ""; 


function handleSubmit() {
    $arrList = [...$arrList, value]
}

</script>

<form class="border-solid">
    <label for="input-field">
        <input bind:value={value} class="border-solid border-sky-900 border-2" type="text">
    </label>
    <button on:click|preventDefault={handleSubmit} class="border-solid border-2 border-sky-800 ml-4 p-1 rounded-md bg-slate-300">Add New Task</button>
    <Value />
</form>
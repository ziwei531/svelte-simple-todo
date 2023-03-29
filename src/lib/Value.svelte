<script>
import {arrList} from '../../store.js';

function handleDelete(taskID) { 
    $arrList = $arrList.filter((task, i) => i !== taskID)
}

</script>

<div class="p-7 flex">
    <ul >
        {#each $arrList as list, i}
            <li class="list-disc p-2">{list}</li>
            <button id="delete-btn" on:click|preventDefault={() => handleDelete(i)} class="p-1 border-red-600 border-solid border-2 rounded-md">Delete</button>
        {/each}
    </ul>

</div>
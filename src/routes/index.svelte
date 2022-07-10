<script>
    let todos = [];
    function addTodo() {
        todos = [...todos, '']
    }
    function removeSelf(index) {
todos = [...todos.slice(0, index), ...todos.slice(index+1)];
    }
</script>

<div class="Title">
	<h1>Exercise!</h1>
</div>

<div class = "list">
    {#each todos as todos, index}
        <input bind:value={todos[index]}>
        <button on:click={()=>removeSelf(index)}>X</button>
        <br>
    {/each}
<button on:click={addTodo}>Add</button>
</div>



<footer>
    <h1>Get back into shape!</h1>
</footer>

<style>
	.Title {
		text-align: center;
		display: block;
		margin: 20px auto;
	}
    .list {
        text-align: center;
    }
    footer{
        text-align: center;
    }
    
</style>

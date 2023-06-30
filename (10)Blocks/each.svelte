<script>
    let cats = [
        { id: "J---aiyznGQ", name: "Keyboard Cat" },
        { id: "z_AbfPXTKms", name: "Maru" },
        { id: "OUtn3pvWmpg", name: "Henri The Existential Cat" },
    ];
</script>

<h1>The Famous Cats of YouTube</h1>

<ul>
    <!-- open each block -->
    {#each cats as cat}
        <li>
            <a target="_blank" href="https://www.youtube.com/watch?v={cat.id}" rel="noreferrer">
                {cat.name}
            </a>
        </li>
    {/each}
    <!-- close each block -->
</ul>


<!-- specific{id} -->
<script>
	import Thing from './Thing.svelte';

	let things = [
		{ id: 1, name: 'apple' },
		{ id: 2, name: 'banana' },
		{ id: 3, name: 'carrot' },
		{ id: 4, name: 'doughnut' },
		{ id: 5, name: 'egg' }
	];

	function handleClick() {
		things = things.slice(1);
	}
</script>

<button on:click={handleClick}> Remove first thing </button>

{#each things as thing (thing.id)}
  <Thing name={thing.name} />
{/each}


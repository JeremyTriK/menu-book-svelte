<script lang="ts">
	    import { cartCounter } from "$lib/store/order";
      import MenuPrice from "./MenuPrice.svelte";
      export let name: string;
      export let desc: string;
      export let photoUrl: string;
      export let prices: {label:string; price:number}[]
      function increase() {
        cartCounter.update((n) => n + 1);
      }
      function decrease() {
        cartCounter.update((n) => n - 1);
      }
      const add = () => {

      }
</script>
  <div class="menu-tile">
      <div class="menu-photo">
        <img src={photoUrl} alt={name} />
      </div>
      <div class="menu-tile-name">{name}</div>
      <div class="menu-tile-description">
        {desc}
      </div>

      {#each prices as pri}
        <MenuPrice label={pri.label} price={pri.price} />
      {/each}
    <button class="add" on:click={increase} >Tambah</button>
    <button class="min" on:click={decrease} >Kurang</button>
  </div>
<style>
  div.menu-tile-name {
    font-weight: 500;
		font-size: 16px;
		padding: 8px 16px;
		align-self: stretch;
		text-align: center;
  }
    div.menu-tile-description {
		font-size: 12px;
		align-self: stretch;
		text-align: center;
		padding: 0px 16px;
		height: 60px;
		padding-bottom: 16px;
	}
  div.menu-tile {
    flex: 1;
    display: flex;
    flex-direction: column;
    padding-bottom: 16px;
  }
  div.menu-photo img {
    aspect-ratio: 1;
    object-fit: cover;
    max-width: 100%;
  }
  button {
    margin:2px;
    border:none;
  }
  .add { 
    background-color:#f44336; 
    color:white;
  }
  .min {
    background-color:white; 
    color:#f44336; 
    border-color:#f44336; 
    border-radius:2px
  }
</style>
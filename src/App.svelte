<script>
  export let name;
  // image folder is pubic/
  let image = './images/profile.webp';
  let inputUser = 'username : <input type="search" name="username">';
  let inputMail = 'email : <input type="email" name="email">';
  let isInputUser = true;
  const switchInput = () => isInputUser = !isInputUser;
</script>

<main>
	<h1>{name} portfolio</h1>
  <img src={image} alt="dd">
  <p><button on:click={switchInput}>切り替え</button> {@html isInputUser ? inputUser : inputMail}</p>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>
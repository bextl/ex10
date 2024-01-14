<script>
	let name = 'Jane Appleased';
	
	let numbers = '1234 5678 9123 0000';
	let creditCardData;
	let month = '00';
	
	let year = '00';
	let cvv = '00';

	// let formData = {
	// 	cardNumber: '',
    // cardHolderName: '',
    // expirationDate: '',
    // cvv: '',
	// }


// 	function handleInputChange(event) {
//     const { name, value } = event.target;
//     creditCardData = { ...creditCardData, [name]: value };
//   }

//   function handleSubmit() {
//     // Handle credit card form submission with creditCardData
//     console.log('Credit card form submitted with data:', creditCardData);
//   }
</script>

<main>
	<!-- <h1>Hello {name}!</h1>
	<div>{@html channel}</div> -->



	<div class = "template">
		<h1>Cardholder Name</h1>
		<input bind:value={name} placeholder="e.g Jane Appleased " />
		<h1>Card Number</h1>
		<input bind:value={numbers} type="text" placeholder="e.g 1234 5678 9123 0000" />

		<input bind:value={month} type="text" placeholder="MM" />
		{#if month.length < 2 }
		<p class="error">Can't be blank</p>
		{/if}
		<input bind:value={year} type="text" placeholder="YEAR" />
		{#if year.length < 2  || year.length > 2}
		<p class="error">Can't be blank</p>
		{/if}
		<input bind:value={cvv} type="text" placeholder="e.g 123" />
		{#if cvv.length < 2 || cvv.length>3}
		<p class="error">Can't be blank</p>
		{/if}

		
		
		
		




		





		


	</div>



	<div class = "card">
		<div class = "rectangle">


		
		<h1 class="cardAt">{numbers}</h1>
		<h1 class="cardAt">{month}</h1>
		<h1 class="cardAt">{year}</h1>
		<h1 class="cardName">{name}</h1>
		
	</div>
	</div>



	<div class="back">

		<div class="black"></div>

		<div class="grey">
			<h1 class="cardCvv">{cvv}</h1>


		</div>

		
	</div>
	<div >
	<button class = "submit">Confirm</button>
</div>
</main>

<style>

	.error{
		color: var(--Red, #FF5050);
font-feature-settings: 'clig' off, 'liga' off;

/* Body (S) */
font-family: Space Grotesk;
font-size: 12px;
font-style: normal;
font-weight: 500;
line-height: normal;
	}

	.submit{
		width: 381px;
height: 53px;
flex-shrink: 0;
border-radius: 8px;
background: var(--Deep-Violet, #21092F);
	}

	.rectangle{
		height: 245px;
		width: 447px;
		border-radius: 10px;
		background: linear-gradient(164deg, #6348FE 4.74%, #610595 88.83%);


	}

	.cardName{
		color: var(--White, #FFF);
font-feature-settings: 'clig' off, 'liga' off;

/* Body (L) */
font-family: Space Grotesk;
font-size: 14px;
font-style: normal;
font-weight: 500;
line-height: normal;
letter-spacing: 2px;
text-transform: uppercase;


margin-top: 5px;

	}

	.cardAt{
		color: var(--White, #FFF);
	font-feature-settings: 'clig' off, 'liga' off;
/* Heading (XL) */
	font-family: Space Grotesk;
	font-size: 28px;
	font-style: normal;
	font-weight: 500;
	line-height: normal;
	letter-spacing: 3.422px;

	}
	
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #5f5a58;
		text-transform: uppercase;
		font-size: 2em;
		font-weight: 100;
	}

	.cardCvv{
		color: var(--White, #FFF);
text-align: right;
font-feature-settings: 'clig' off, 'liga' off;

/* Body (L) */
font-family: Space Grotesk;
font-size: 20px;
font-style: normal;
font-weight: 500;
line-height: normal;
letter-spacing: 2px;
text-transform: uppercase;
	}

	.back{
		margin-top: 20px;
		
width: 447px;
height: 245px;
flex-shrink: 0;
border-radius: 10px;
background: linear-gradient(169deg, #FFF 5%, #D2D3D9 91.69%);


	}

	.black{
		width: 447px;
		height: 54px;
		flex-shrink: 0;
		background: #2F2F2F;
	}
	
	/* @media (min-width: 640px) {
		main {
			max-width: none;
		} */
	.grey{
		width: 361px;
	height: 38px;
	flex-shrink: 0;
	border-radius: 4px;
	background: #ADB5BE;
	margin-left: 50px;
	}
</style>


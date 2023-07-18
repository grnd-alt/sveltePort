<script lang="ts">
	import { base } from '$app/paths'
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div class="images">
	<a class="imgwrap" href="{base}/frontend">
		<img src="https://images.unsplash.com/photo-1535957998253-26ae1ef29506?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxzZWFyY2h8NTF8fGRlc2lnbnxlbnwwfHwwfHx8MA%3D%3D&auto=format&fit=crop&w=600&q=60" alt="">
		<div class="greyscaled"></div>
		<div class="content">
			<h2 class="content-head">Frontend</h2>
			<ul>
				<li>
					Visual Frontend-projects
				</li>
				<li>Algorithm visualizations</li>
				<li>Design concepts</li>
			</ul>
		</div>
	</a>
	<a class="imgwrap" href="{base}/backend">
		<img src="https://img.freepik.com/premium-photo/computer-servers-with-purple-lights-server-farm-created-using-generative-ai-technology_772924-1989.jpg" alt="">
		<div class="greyscaled"></div>
		<div class="content">
			<h2 class="content-head">Backend</h2>
			<ul>
				<li>Backend API applications</li>
				<li>Fullstack application and clones</li>
			</ul>
		</div>
	</a>
	<a class="imgwrap" href="{base}/exp">
		<img src="https://images.unsplash.com/photo-1689579230089-5f3715ebe0f5?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxlZGl0b3JpYWwtZmVlZHw5fHx8ZW58MHx8fHx8&auto=format&fit=crop&w=600&q=60" alt="">
		<div class="greyscaled"></div>
		<div class="content">
			<h2 class="content-head">Experience</h2>
			<ul>
				<li>
					Professional experience I've been able to gather over the years
				</li>
			</ul>
		</div>
	</a>
</div>

<style>
	a{
		text-decoration: none;
	}
	li {
		line-height: 1.5em;
	}
	ul {
		padding-left:0px;
		list-style-type: none;
	}
	.content{
		z-index: 9;
		grid-row: 1;
		grid-column: 1;
		color:white;
		display: flex;
		flex-direction: column;
		justify-content: flex-end;
		padding-inline:1rem;
		background-image: linear-gradient(to top right,rgba(0,0,0,.7),rgba(0,0,0,0));
	}
	.content h2 {
		color: var(--color-highlight);
		font-size: 2.5em;
		margin: 0;
		padding:0;
	}
	.content p {
		margin-top:0;
	}
	.images{
		margin: auto;
		display:flex;
		width: 100%;
		justify-content: space-evenly;
		flex-wrap: wrap-reverse;
	}
	.imgwrap{
		border: 3px solid var(--color-highlight);
		border-radius: 20px;
		overflow: hidden;
		display: grid;
	}
	.imgwrap img {
		grid-row: 1;
		grid-column: 1;
		object-fit: cover;
		width: 100%;
		height: 100%;
		z-index: 0;
		transform: scale(1);
		transition: transform ease-in-out .7s;
	}
	.images .imgwrap{
		margin-top:1rem;
		min-width: 100px;
		max-width: 300px;
	}

	.imgwrap:hover img {
		transform: scale(1.05);
		transition: ease-in-out .7s;
	}

	.imgwrap:hover .greyscaled {
		cursor: pointer;
		opacity: 0;
		transition: opacity cubic-bezier(0.47, 0, 0.745, 0.715) .7s;
	}
	.images .greyscaled {
		z-index: 10;
		grid-row: 1;
		grid-column: 1;
		background: black;
		filter: grayscale(1);
		opacity: 0.5;
		transition: opacity cubic-bezier(0.47, 0, 0.745, 0.715) 1s;
	}

</style>

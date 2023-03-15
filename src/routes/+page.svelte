
<script>
	import helloWordArr from './hello'
	import Highlight from './components/Highlight.svelte';

	let helloWord = helloWordArr[Math.floor((Math.random() * helloWordArr.length))]
</script>

<main>
	<h1><span>{helloWord},</span>我是Kevin Rocco.</h1>
	<p>主流<Highlight icon="apple,h5" highlightClass="moegi">Java</Highlight>开发工程师，就职于<Highlight icon="didi" highlightClass="orange">Rocco's Life</Highlight>。</p>
	<a href="https://github.com/KevinRocco">Github</a>
	<a href="https://kevinrocco.github.io/my-app/">Blog</a>
</main>


<style>
	:root {
        --color-text: #515151;
        --color-text-emphasize: #333333;
        --color-text-lighter: rgba(0, 0, 0, 0.4);
        --color-text-solight: rgba(0, 0, 0, 0.16);
        --color-background: #ffffff;
        --color-background-inner: rgba(255, 255, 255, 0.8);
        --color-decoration: rgba(0, 0, 0, 0.04);
        --color-decoration-darker: rgba(0, 0, 0, 0.08);
    }

    @media (prefers-color-scheme: dark) {
        :root {
            --color-text: rgba(255, 255, 255, 0.6);
            --color-text-emphasize: #EEEEEE;
            --color-text-lighter: rgba(255, 255, 255, 0.4);
            --color-text-solight: rgba(255, 255, 255, 0.16);
            --color-background: #222222;
            --color-background-inner: rgba(#{hexToRGB(#222222)}, 0.8);
            --color-decoration: rgba(255, 255, 255, 0.04);
            --color-decoration-darker: rgba(255, 255, 255, 0.08);
        }
    }
	
	p {
        margin: 0;
        padding: 0;
        font-weight: normal;
        vertical-align: baseline;
    }

	main {
        font: 400 16px/1.6 PingFang SC, Lantinghei SC, Microsoft Yahei,Hiragino Sans GB, Microsoft Sans Serif, WenQuanYi Micro Hei, sans-serif;
        margin: 0;
        padding: 10vh 10vw;
        min-height: 100vh;
		box-sizing: border-box;
		background: var(--color-background);
    }

	h1 {
		font-size: 2.4rem;
		color: var(--color-text-emphasize);
		font-weight: bold;
		margin-bottom: 1.6rem;
	}
    h1 span {
        display: block;
    }

	p {
		font-size: 1.4rem;
		color: var(--color-text);
		margin-bottom: 0.5rem;
	}

	a {
        text-decoration: none;
		display: inline-block;
		margin-top: 2.4rem;
		margin-right: 0.2rem;
		padding: 0.3rem 0.8rem;
		background: var(--color-decoration);
		border-radius: 4px;
		font-size: 1.1rem;
		color: var(--color-text-lighter);
		transition: all 0.3s ease;
	}
    a:hover {
        background: var(--color-text);
		color: var(--color-background);
    }
</style>
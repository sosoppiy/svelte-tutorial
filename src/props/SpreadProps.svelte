<script>
	import Info from './Info.svelte';

	const pkg = {
		name: 'svelte',
		version: 3,
		speed: '燃える',
		website: 'https://svelte.dev'
	};
</script>

<div style="padding-bottom:100px;">
    <h3>チュートリアルの内容</h3>
    <div>
        <p>propsを普通に1つ1つ渡してあげても出来るけど…</p>
        <Info name={pkg.name} version={pkg.version} speed={pkg.speed} website={pkg.website}/>      
    </div>

    <div>
        <p>スプレッド構文を使えばもっと簡単に書けちゃうよ</p>
        <Info {...pkg} /> 
    </div>

    <!-- todo::ここの深堀りから -->
</div>


<script>
	let count = 0;

	function handleClick() {
		count += 1;
	}
</script>

<div>
    <h4>反応性</h4>
    <div>
        Svelteのには、イベントへの応答など、DOMをアプリケーションの状態と同期させるための強力な反応性システムがあります。（google翻訳コピペ）<br>
        ボタンを押す度にcountが増えていくよ。ボタンの文字列に、押した回数も表示させるよ。
    </div>
    <button on:click={handleClick}>
        Clicked {count} {count === 1 ? 'time' : 'times'}
    </button>
</div>

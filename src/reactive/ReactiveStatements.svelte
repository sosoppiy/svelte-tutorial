<script>
    let count = 0;
    $: console.log(`the count is ${count}`);

    // ↓グループ化もできるよ
    $: {
        console.log("グループ化したものから呼び出し")
        console.log(`the count is ${count}!!!!!`);
    }

    // ↓if分岐とかも
    $: if (count >= 10) {
        alert(`count is dangerously high!`);
        count = 9;
    }

	function handleClick() {
		count += 1;
	}
</script>

<h1>リアクティブなステートメント</h1>

<div style="padding-bottom: 30px;">
    <h3>ボタンが押される度に、consoleに出力したい</h3>
    <div>{"$: console.log(`the count is ${count}`);"}</div>
    こんな感じに書くだけ。
    <div>
        <button on:click={handleClick}>
            Clicked {count} {count === 1 ? 'time' : 'times'}
        </button>
    </div>
</div>




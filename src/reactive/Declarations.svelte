<script>
    let count1 = 0;
    let count2 = 0;
    let doubled1 = count1 * 2;
    $: doubled2 = count2 * 2;

	function handleClick01() {
		count1 += 1;
    }
    function handleClick02() {
		count2 += 1;
	}
</script>

<h1>リアクティブな変数</h1>
<div style="margin-bottom: 30px;">
    <h3>countの倍数を出したいゾ</h3>
    <div>
        前回のをちょっと変えて、countとは別の変数で、countの倍の数を出したいとする。<br>
        とりあえず、「let doubled = count * 2;」と宣言してみる。
    </div>
    <div>
        <button on:click={handleClick01}>
            Clicked {count1} {count1 === 1 ? 'time' : 'times'}
        </button>
        <p>{count1} doubled is {doubled1}</p>
    </div>
    <div>ボタンを押しても、doubledの値が変わらない。</div>
</div>

<div style="margin-bottom: 30px;">
    <h3>なんで？</h3>
    <div>
        何でかというと、「let doubled = count * 2;」と宣言した場合、最初の宣言のときにしかレンダリングされないから、<br>
        count=0の時に計算されたまま変わらない。
    </div>
</div>

<div style="margin-bottom: 30px;">
    <h3>じゃあどうするの</h3>
    <div>
        宣言を、「$: doubled2 = count * 2;」とすることで、countの値の変化に応じて再計算される。
    </div>
    <div>
        <button on:click={handleClick02}>
            Clicked {count2} {count2 === 1 ? 'time' : 'times'}
        </button>
        <p>{count2} doubled is {doubled2}</p>
    </div>
    <div>
        vueのcomputed的な感じだと思う。
    </div>
</div>



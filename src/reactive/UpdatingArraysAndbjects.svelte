<script>
	let numbers = [1, 2, 3, 4];
	let numbers2 = [1, 2, 3, 4];
	let numbers3 = [1, 2, 3, 4];
	let array = [1,2,3,4,5,6,7,8,9,10];
	let array2 = [1,2,3,4,5,6,7,8,9,10];

	let obj = {id: 1, name: "hoge", age: 20};

	function addNumberFaild() {
        //# ↓これだけだと、numbers配列の変化に応じて再描画してくれない。 ※配列自体は変わってるので、console.logで表示した時は値が追加されている
        numbers.push(numbers.length + 1);       
	}

	function addNumberSuccess() {
		//# ↓スプレッド構文を使うなどして、変数に再代入してあげれば再描画される。
		// スプレッド構文については https://qiita.com/akisx/items/682a4283c13fe336c547 
		numbers2 = [...numbers2, numbers2.length + 1];
	}
	function addNumberSuccess02() {
		//# インデックス指定して、値を入れるパターン
		numbers3[numbers3.length] = numbers3.length + 1;
	}

	function removeArrayFailed() {
		array.pop();
	}

	function removeArraySuccess() {
		array2.pop();
		array2 = array2;
	}

	/**
	 * オブジェクトの値更新
	 */
	function updateObjectValues() {
		obj.age++;
	}

	$: sum = numbers.reduce((t, n) => t + n, 0);
	$: sum2 = numbers2.reduce((t, n) => t + n, 0);
	$: sum3 = numbers3.reduce((t, n) => t + n, 0);
</script>

<!-- チュートリアルの例 -->
<div style="margin-bottom:100px">
	<div>
		<h3>チュートリアルの例</h3>
		<p>{numbers.join(' + ')} = {sum}</p>
	
		<button on:click={addNumberFaild}>
			数字追加（再描画されない）
		</button>
	</div>
	
	<div>
		<p>{numbers2.join(' + ')} = {sum2}</p>
		<button on:click={addNumberSuccess}>
			数字追加（再描画される）
		</button>
	</div>

	<div>
		array[i] = x  みたいに、直接値を入れてもOK
		<p>{numbers3.join(' + ')} = {sum3}</p>
		<button on:click={addNumberSuccess02}>
			数字追加（再描画される）
		</button>

	</div>
</div>

<!-- 自分で色々やってみる -->
<div>
	<h3>自分で色々試してみる</h3>

	<div style="padding-bottom: 30px;">
		<h4>popも試してみる。</h4>
		<div>
			<p>{array.join(', ')}</p>
			<button on:click={removeArrayFailed}>remove!再描画されない</button>
		</div>
		<div>
			<p>{array2.join(', ')}</p>
			<button on:click={removeArraySuccess}>remove!再描画される</button>
		</div>
	</div>

	<!-- オブジェクト -->
	<div>
		<h4>オブジェクトはどう？</h4>
		<p>id: {obj.id}</p>
		<p>name: {obj.name}</p>
		<p>age: {obj.age}</p>

		<button on:click={updateObjectValues}>誕生日を迎えたぜ</button>
	</div>
</div>

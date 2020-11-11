<script>
	import Nested from './Nested.svelte';
</script>

<style>
	p {
		color: purple;
		font-family: 'Comic Sans MS', cursive;
		font-size: 2em;
	}
    .class-test {
        font-family: "游ゴシック体", YuGothic;
        font-size: 1em;
        color:aquamarine
    }

    #myComponent {
        padding: 0.5em 1em;
        margin: 2em 0;
        border: solid 3px #6091d3;/*線*/
        border-radius: 10px;/*角の丸み*/
    }
</style>

<div>
    アプリ全体を1つのコンポーネントにまとめるのはあまりにも実用的じゃない。<br>
    代わりに、他のファイルからコンポーネントをインポートして使ってみよーう。
</div>

<div id="myComponent">
    <p>ここは自コンポーネントの要素</p>
    <div class="class-test">ここも自コンポーネントの要素。class="class-test"をつけた。</div>
</div>

<Nested/>
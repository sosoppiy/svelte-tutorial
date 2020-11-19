<script>
	export let name;
	export let version;
	export let speed;
	export let website;
</script>

<p class="border">
    {name}っていうのは{speed}ように早いよ。<br>
    <a href="https://www.npmjs.com/package/{name}">npm</a>からバージョン{version}をダウンロードしよう！<br>
    詳しくは<a href={website}>ここ</a>を見てね。
</p>

<style>
.border {
    padding: 0.5em 1em;
    margin: 2em 0;
    border: solid 3px #6b60d3;/*線*/
    border-radius: 10px;/*角の丸み*/
}
</style>

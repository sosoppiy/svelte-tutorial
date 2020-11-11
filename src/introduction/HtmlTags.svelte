<script>
	let string = `this string contains some <strong>HTML!!!</strong>`;
</script>

<div style="margin-bottom: 20px;">
    <div>
        通常、文字列はプレーンテキストとして挿入されるので、文字列の変数にhtmlのタグを入れてもそのまま表示される。
    </div>
    <p>{string}</p>
</div>

<div>
    <div>
        htmlとしてレンダリングしたい場合は、@html をつける。
    </div>
    <p>{@html string}</p>
    <div>
        vue同様、何も対策しないとXSS攻撃されるので注意。
    </div>
</div>

<script></script>

<style>
    #nestedComponents {
        padding: 0.5em 1em;
        margin: 2em 0;
        border: solid 3px #6b60d3;/*線*/
        border-radius: 10px;/*角の丸み*/
    }
</style>

<div id="nestedComponents">
    <p>
        ここがimportした別コンポーネントの要素だよ。<br>同じp属性だけどstyleは適用されないね。<br>
        ちなみに、ユーザー定義のコンポーネントと通常のHTMLタグを区別できるようにするため、コンポーネント名の頭文字は大文字だよ。
    </p>

    <div class="class-test">
        別コンポーネントに、親で定義しているclass="class-test"をつけた。class指定でstyleつけても、コンポーネントが違うと反映されないので注意。<br>
        コンポーネント別に独自classが勝手に生成されて、コンパイルした後だと、 「.自分で作ったクラス .独自クラス」ってstyleが指定されているから、<br>
        別コンポーネントには適用されないんだと思われる。<br><br>
        <img src="images/tutorial03.png" alt="" width="50%">
    </div>
</div>

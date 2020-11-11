<script>
    let src = 'images/image.gif';
    let name = "Crazy guy";
</script>

<main>
    <div style="padding-bottom: 30px;">
        <h4>alt属性なし。</h4>
        <div>表示はされるけど、エラー表示してくれる。</div>
        <div>
            <img src={src}>
        </div>
        
        <div>
            コード内でのエラー<br>
            <img src="images/tutorial01.png" alt="tutorial01">
        </div>

        <div>
            コンパイルでのエラー(警告？)<br>
            <img src="images/tutorial02.png" alt="tutorial02">
        </div>
        
    </div>

    <div>
        <h4>alt属性あり</h4>
        <img src={src} alt="A man dances.">
    </div>  
    
    <div>
        <h4>属性内でも中括弧ガウt変えるよ（変数が使えるよ）</h4>
        <div>
            alt="A man dances."　→　alt="変数name dances"　にしてみる <br>
            変数nameの値　→　{name}
        </div>
        <div>
            <img src={src} alt="{name} dances.">
        </div>
    </div>
</main>

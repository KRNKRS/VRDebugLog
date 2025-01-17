# VRDebugConsole
これはVR開発上でデバッグの補助を行うアセットで、3D空間上にデバッグログの情報を表示します。<br>
現在、実装されている機能は以下。<br>

## Ver.0.6 機能<br>Function
<ul>
<li>リサイズ</li>
<li>ビルボード</li>
<li>最小化</li>
<li>ログのクリア</li>
<li>タイプごとのログの表示/非表示切り替え</li>
<li>項目選択によるスタックトレース表示</li>
<li>Viveコントローラによる限定的な操作</li>
</ul>
## 使い方<br>How to
<ol>
<li>インスペクターもしくはシーンビューにVRDebugプレハブをD&Dします</li>
<li>終わり</li>
</ol>
![D&D](https://cloud.githubusercontent.com/assets/3947216/21044584/0efda7ec-be40-11e6-889f-87ba8f4e2ae2.gif "D&D")<br>
<br>
好みのサイズと位置に調整して使用できます。<br>
![Resize and Billboard](https://cloud.githubusercontent.com/assets/3947216/21043606/02cb9222-be3b-11e6-9898-3014e3e5bdf6.gif "Resize and Billboard")<br>
<br>
HTC Viveを使用している場合は、EventSystemにアタッチされている「VRDebugInputModule」にコントローラを指定し、Unity再生中にトリガーを引くことで操作を行うことが出来ます。
![Vive Controller Attach](https://cloud.githubusercontent.com/assets/3947216/21046523/75b92c88-be48-11e6-9bcc-a76f8e0ed32c.gif "Vive Controller Attach")
![Vive operate](https://cloud.githubusercontent.com/assets/3947216/21043849/4c8f64aa-be3c-11e6-80cf-610affdd40bf.gif "Vive operate")

## クリック(or Viveコントーラによる操作)しても反応ないんだけど！<br>
「EventSystem」のInputModuleがどちらも有効になっていると正常なクリックなどの操作を判断してくれなくなります。<br>
Viveによる操作をしたいならば「Standard Inpu Module」を、マウス等による操作をしたいならば「VR Debug Input Module」を非有効化にしてください。<br>

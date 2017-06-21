# convert_font
フォントファイルから画像生成．

前から研究室で受け継がれてたものが古くて改造しにくかったので新しいものを作ろうと．
PythonのPillowでフォント指定して描画できそうだったからやってみたものです．

## Requirement
- Python 3.6
- Pillow
- numpy

## Usage
```
python font2img.py {フォントファイル(ttf, otf)が入ったディレクトリ} {出力ディレクトリ(自動生成)} {キャンバスサイズ} [options]
```
### Options
|オプションコマンド|効果|
|:-|:-|
|`-f (--font_size) {フォントサイズ}`|フォントサイズ指定．指定しなければ適当に決まる．|
|`-e (--ext) {拡張子}`|拡張子．デフォルト拡張子．デフォルトは'png'．|
|`-m (--maximum)`|キャンバスサイズいっぱいに最大化．これ指定するとフォントサイズは無視される． **とにかく遅いです．またうまくいかないフォントも．** 改善予定…|
|`-b (--binary)`|2値画像として保存|
|`-l (--lang)`|作成する文字．`['eng_caps', 'jp', 'gbk', 'kr', 'gb2312_t']`から選ぶ．zi2ziのcharset/cjk.jsonから拝借している．|
|`--not-centering`|センタリングなし．動作速い．|

## References
- [zi2zi](https://github.com/kaonashi-tyc/zi2zi)のfont2img.py

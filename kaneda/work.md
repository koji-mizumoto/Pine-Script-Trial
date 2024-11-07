# TradingViewの作業メモ

## TradingView（無料版）

- 開けるタブは2つまで
  - 3つ目を開くと最初に開いたタブは強制的に接続が切られる
  スクリプトはコピペでローカルに保存しておくこと
  - 無料版はタブ1つに対して、インジゲーター（1つのPineScript）しか表示できない
    - 追加のインジゲーターを作りたい場合は、新規でタブを作る
    - 無料版はタブを2つまでしか作れない点に注意する

## PineScript

- 最新版は、Version5
  - 更新は2021/10/7頃
  - これ以前の情報はVersion4以前のもので、スクリプトの文法が全然違うので注意
    - コードでstudy(...)関数があったら間違いなくv4以前のものなので、参考にするかはよく考えること。
    - ※studyは、v5でindicator関数に変わっている
    - 他にもema(v4)がta.ema(v5)になっているなど、多数の変更点が見られる
    - PineScriptエディタでは、旧式のコードはエラーが出る様になっている
  - エディタでv4からv5にコンバートすることができる模様

## 用語集

### 移動平均線、Exponential Moving Average(EMA)

- テクニカル指標
  - 指数平滑移動平均線のこと

### ボリンジャーバンド

- テクニカル指標
  - 移動平均線と標準偏差で構成されており、移動平均を表す線とその上下に値動きの幅を示す線を加えた指標で、「価格の大半がこの帯（バンド）の中に収まる」という統計学を応用したテクニカル指標のひとつ。
    - 標準偏差の計算式　標準偏差＝√(n×n日間の終値の2乗の合計－n日間の終値の合計の2乗)÷(n×(n－1))
  - ボリンジャーバンドの計算式　±1σ ＝ n日の移動平均 ± n日の標準偏差
±2σ ＝ n日の移動平均 ± n日の標準偏差 × 2
±3σ ＝ n日の移動平均 ± n日の標準偏差 × 3
  - 特徴は、収束と拡散を繰り返していることで、この動きにあわせて「順張り」「逆張り」それぞれの投資に利用することができる
  - [ボリンジャーバンド](https://info.monex.co.jp/technical-analysis/indicators/003.html)

## RSI（相対力指数）

- テクニカル指標
  - 現在の相場の相対的な強弱（又は過熱感）を表す指標
  - 特徴としてボックス相場が続いているときの的中率は高いものの、上下に強いトレンドが出ると、売買シグナルが出ていたとしても、トレンドの勢いが止まらずに、結局ダマシに終わることがある
    - 計算式１　RS＝（n日間の終値の上昇幅の平均）÷（n日間の終値の下落幅の平均）
    - 計算式２　RSI= 100　-　（100　÷　（RS+1））
  - [RSI](https://info.monex.co.jp/technical-analysis/indicators/005.html)
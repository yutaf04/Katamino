# Polyomino（ポリオミノ）

[公式サイト(Katamino)](https://www.assiston.co.jp/2659)


## 概要
Polyominoの敷き詰めパズルを以下のアルゴリズムで解く

1. フロンティア法(TdZDD)
2. AlgorithmX

## Exact Cover Problem への定式化

Polyominoの敷き詰めパズルは「どのマスを埋めるか」及び「どのミノを使うか」を1つの集合として考えると,

これらの集合族の中で全ての要素を1度だけカバーするような部分集合の集合を求める問題である（exact cover problem）に定式化できる．

これはKnuth's AlgorithmXで全探索可能である．


## AlgorithmX

* [Knuth's Algorithm XとDancing Linksの解説 - TopCoderとJ言語と時々F#](http://d.hatena.ne.jp/JAPLJ/20090902/1251901464)
* [Knuth's Algorithm X - Wikipedia](https://en.wikipedia.org/wiki/Knuth%27s_Algorithm_X)

dancing-linksと呼ばれるデータ構造を用いる．

各ノードが上下左右の4方向への参照を持つ双循環連結リスト

ノードの削除(cover)及び復元（uncover)を高速に行うことができる．

## 入力
入力は以下の形式で与えられる.

H:ボードの高さ　W:ボードの幅

N:Polyominoの個数  

$h$:各Polyominoの高さ  

$w$:各Polyominoの幅 

```

H W
N
h w
(form of Polyomino)

...

```



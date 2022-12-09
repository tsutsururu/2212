# 2212

# 1203

# ABLA   Repeat ACL   diff 10

解答遷移 AC

計 01:17

備考　

なし

# ABLB  Integer Preference  diff 51

解答遷移 AC

計 03:52

備考

➀　思考

A C の大小関係に注目し、A<C なら CとB ,  C<A　なら AとD の大小関係で条件判定した。

➁　解法

max(left) と min(right) で区間の被りを判定できる


# ABL C   Connect Cities  diff 435

解答遷移 AC

計 05:59

備考

➀　思考

連結成分を1頂点とみなしたグラフを作成すればよいので、連結成分-1 が答えになる


# 082C  Good Sequence  diff 593

解答遷移 AC

計 04:38

備考

➀　思考

個数を管理。出てくる要素を全探索して、その要素の値 > その要素の数 なら要素の数だけインクリメント。　その要素の値 < その要素の数 なら その要素の数 - その要素の値　だけインクリメント



1209

# 244D  Swap Hats  diff 165

解答遷移 AC

計 12:59

備考

➀　思考

全並び替えが6通りしかないので、偶数回の操作で到達可能な並びを素直に調べて T を判定すればよいと考えた。

➁　補足

転倒数の偶奇に注目することで 並び替えの数が増えても対応できる。

・転倒数

自分より前にある要素で、自分より大きな値がいくつあるかの総数

転倒数が偶数である並び替えを偶置換、奇数である並び替えを奇置換と呼ぶ

https://mathlandscape.com/permutation/


偶置換か、奇置換であるかは BIT で判定できる。



# BIT (Binary Index Tree) 勉強

値の更新と、自分より前の総和を O(logN)　で求められるデータ構造

http://hos.ac/slides/20140319_bit.pdf


https://ikatakos.com/pot/programming_algorithm/data_structure/binary_indexed_tree

x & (-x) が x(2) における一番下位の1の位置であることを利用して、x , x+( x&-x) , .... の値を更新する。ここで特定の値も更新しておくことで、総和演算が効率的に行えるようになる。

![image](https://user-images.githubusercontent.com/109026838/206773492-b7f977aa-774e-4e97-8292-280227e2b1f6.png)

具体的には、x , x-(x&-x) , ... を調べることで、自分より前の総和を計算可能になる。

![image](https://user-images.githubusercontent.com/109026838/206774186-d071a874-5c08-459a-9b01-5fd5b6267220.png)


注意点としては、bit演算の都合、与える要素は非負整数でなければいけないことである。

操作イメージ

https://scrapbox.io/pocala-kyopro/%E8%BB%A2%E5%80%92%E6%95%B0













# Welcome to Quantum Native Dojo !

Quantum Native Dojoは量子コンピュータについて勉強したいと思っている方のために作られた自習教材です。

量子コンピュータの基本的な動作原理から、基礎アルゴリズム、それらを応用してどのように化学計算や金融計算などに役立てるかを学ぶことができます。本教材は誤り訂正の有る量子コンピュータのアルゴリズムの他、数年以内に実用されるであろうNISQ (Noisy Intermidiate-Scale Quantum) デバイスのアルゴリズムもカバーしています。

全ての教材が `Jupyter notebook` で製作され、そのまま Google Colaboratory 上で実行可能になっているので、面倒な環境設定をすることなく学習を始めることが可能です。

なおウェブサイト版もありますので、合わせてご利用下さい。  
https://dojo.qulacs.org

## この教材の意義： Becoming Quantum Native
量子コンピュータは、量子力学の原理に基づいて計算を行います。一方、私達がふだん目にする物理現象は主に古典力学に支配されています。ここに「量子コンピュータは難しい」と思われる原因の一端があります。

Quantum Native Dojoでは、みなさまに量子コンピュータの動作を感覚的に理解して使いこなせる**Quantum Native**になっていただくことを目標としています。Quantum Nativeへの道のりは簡単ではありませんが、このDojoを通して基礎からじっくりと量子力学と量子コンピュータの原理・応用を学ぶことが着実な一歩となるでしょう。

このDojoを巣立ち、Quantum Nativeとなったみなさまが様々な量子アルゴリズム/アプリケーションを作るエンジニアとして活躍されることを期待しています！

## 前提となる知識
Quantum Native Dojoの内容を理解するには、以下のような知識が必要です。
- 複素数とは何か
- 簡単な関数(sin, cos, exp, ...)の微積分
- 行列とベクトルの掛け算、対角化とは何か

こちらの前提知識及びPython・NumPyの使用に不安がある方は、[Chainer Tutorial](https://tutorials.chainer.org/ja/tutorial.html)の1. ~ 12.を先に学習することをオススメします。

## 教材の進め方
基本的に、このレポジトリの"notebook"フォルダ以下にある `Jupyter notebook` を読みながら/実行しながら進めていきましょう。
各 `Jupyter notebook` は `Google Colabolatory` で実行することができるので、自前で環境を構築する必要はありません。
(もちろん、Pythonに詳しい方は手元でnotebookを実行して納得するまで使い倒してください)

### `Google Colabolatory`  上で実行する場合
1. [Google Colabolatory](https://colab.research.google.com/notebooks/welcome.ipynb?hl=ja) のページを開きます
2. `ファイル` > `ノートブックを開く` を選択します
![colab](readme-figs/how-to-colab-00.png)
![colab](readme-figs/how-to-colab-01.png)

3. `GITHUB` のタブを選択し、ノートブックの絞り込みの欄に `qulacs` と入力します
![colab](readme-figs/how-to-colab-02.png)

4. レポジトリのプルダウンで `qulacs/quantum-native-dojo` を選択し、ブランチで `master` を選択します
![colab](readme-figs/how-to-colab-03.png)

5. 開きたいノートブックを選択します
![colab](readme-figs/how-to-colab-04.png)

### `Jupyter notebook` で実行する場合
1. [Quantum Native Dojo のリポジトリ](https://github.com/qulacs/quantum-native-dojo) をフォークします
2. Console から `$ jupyter notebook` で[ノートブックを起動](https://jupyter.readthedocs.io/en/latest/running.html#running)させます

`Jupyter` を起動させるためには `Python 3.3` 以上と `Jupyter` をインストールする必要があります。

また、ノートブックに埋め込まれているコードを実行するためには、`numpy`、`scipy`、`sympy` をインストールする必要があります。
上記のパッケージをまとめてインストールするには `anaconda3` のインストールが便利です。


## 目次
===== 第1部：基礎編 =====
- 第0章 量子计算机是什么？
- 第1章 量子信息的基础
  - 1-1. 量子比特
  - 1-2. 量子比特对应的运算
  - 1-3. 复数量子比特的记述
  - 专栏：通用门是什么？
  - 1-4. 回路图的基础
  - 专栏1：量子复制不可能 (No-Cloning) 定理
  - 专栏2：Bell (CHSH) 不等式
- 第2章 量子算法入门
  - 2-1. NISQ算法とlong-term算法
  - 2-2. Hadamard Test
  - 专栏：量子乱数生成
  - 2-3. 量子傅立叶变换
  - 2-4. 相位推定算法（入门篇）
- 第3章 量子算法的运行环境
  - 3-1. 世界最高速模拟器Qulacs的使用方法
  - 3-2. Qiskit和IBM Q Experience的使用方法

===== 第2部：NISQ篇 =====

- 第4章 量子动力学模拟
  - 4-1. 薛定谔方程式、量子动力学是什么
  - 4-2. 使用Trotter分解的量子模拟
- 第5章 基于变分量子回路的量子算法
  - 5-1. Variational QuantumEigensolver（VQE）变分量子特征求解器
  - 5-2. Quantum Circuitlearning
  - 专栏：基于Quantum CircuitLearning的分类
  - 专栏：量子储层计算
  - 5-3. Quantum Approximate Optimazation Algorithm (QAOA):量子近似优化算法
- 第6章 量子化学计算
  - 6-1. OpenFermion的使用方法
  - 6-2. 基于Qulacs的变分量子特征求解器的实装
  - 6-3. 激发态的搜索算法 (subspace-search variational quantumeigensolver)

===== 第3部：Long-term篇 =====
- 第7章 量子相位推定算法的发展
  - 7-1. 量子相位推定算法实例：在水分子上的应用
  - 7-2. Harrow-Hassidim-Lloyd (HHL)算法
  - 专栏：量子随机存取储存器(qRAM)
  - 7-3. 基于HHL算法的投资组合优化
  - 专栏：低秩行列式对应的高速奇异值分解和取样（量子启发算法）
- 第8章 量子探索算法
  - 8-1. Oracle
  - 8-2. 全局算法
- 第9章 量子纠错
  - 9-1. 经典误差
  - 9-2. 量子误差
 

`*`标记的章需要物理和化学的专业知识

## 参考文献
量子力学・量子コンピュータについてより詳しく知りたい/深く理解したい場合には、以下のような参考書をオススメします。
- 量子力学について：
  - 清水明「[量子論の基礎 - その本質のやさしい理解のために](
https://www.amazon.co.jp/dp/4781910629)」、サイエンス社 (2004)
- 量子コンピュータ・量子アルゴリズムについて：
  - 竹内 繁樹「[量子コンピュータ - 超並列計算のからくり](https://www.amazon.co.jp/dp/4062574691)」、講談社 (2005)

また、英語に抵抗がない場合、量子コンピュータの金字塔とも言えるNiesen-Chaungの教科書を読むのがベストです(分量が多いので、時間はかかります)。
- M. Nielsen and I. Chuang,  "[Quantum Computation and Quantum Information: 10th Anniversary Edition](https://www.amazon.co.jp/dp/1107002176)", Cambridge University Press (2010)

## Community
本教材について分からないことは以下のコミュニティで聞いてください。  
[Qulacs Slack Community](https://join.slack.com/t/qulacs/shared_invite/enQtNzY1OTM5MDYxMjAxLWM1ZDc3MzdiNjZhZjdmYTQ5MTJiOTEzZjI3ZjAwZTg0OGFiNjcxY2VjZWRjMWY0YjE5ZTViOWQzZTliYzdmYzY)

## 本教材の作者
本教材は[株式会社QunaSys](https://qunasys.com)と以下のContributorの方々によって作製・メンテナンスされています。

[Keisuke Fujii](http://quantphys.org/wp/keisukefujii/),
[kwkbr](https://github.com/kwkbtr),
[MakotoNakai](https://github.com/MakotoNakai),
[yoooopeeee](https://github.com/yoooopeeee),
[Kosuke Mitarai](https://scholar.google.com/citations?user=TfsGcnMAAAAJ),
[Yuya-O-Nakagawa](https://scholar.google.co.jp/citations?user=LyU8LXsAAAAJ),
[yamamoto-takahiro](https://github.com/yamamoto-takahiro)

## リリース履歴
- 2019/4/26: v0.1.0をリリースしました。
- 2019/12/5: v1.0.0をリリースしました。 

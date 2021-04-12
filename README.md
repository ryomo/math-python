## これは何？

Pythonでの計算をするのに使う複数のソフトウェアを、ローカル環境を汚さないようにDockerで使えるようにしたもの。
Dockerfile, docker-compose.ymlともに、なるべくシンプルにしている。

以下が含まれる。

* Python3
* [Anaconda | Individual Edition](https://www.anaconda.com/products/individual)
* [JupyterLab](https://jupyterlab.readthedocs.io/en/latest/)
* [PuLP](https://pypi.org/project/PuLP/)

## 使い方

```bash
git clone git@github.com:ryomo/math-python.git
docker-compose up
```

表示されるリンクの1つを開くと、JupyterLabに自動ログインされる。


## pipパッケージを追加する場合

docker/requirements.txtに書いて、以下を実行。

```bash
docker-compose build
docker-compose up
```

# deep-learning-environment

## example

Dockerfile

``` dockerfile
FROM hkamei/deep-learning

ENV TZ=Asia/Tokyo \
  DEBIAN_FRONTEND=noninteractive \
  LD_LIBRARY_PATH=/usr/local/cuda/lib64:$LD_LIBRARY_PATH \
  PATH=/usr/local/cuda/bin:$PATH \
  LIBRARY_PATH=/usr/local/cuda/lib64:$LD_LIBRARY_PATH

# デフォルトランタイムをnvidiaにしてないとインストールに失敗するので注意
# 参考：https://qiita.com/yuyakato/items/640ba7a6264f1c21aea7
RUN pip3 install cupy

RUN apt-get update

```

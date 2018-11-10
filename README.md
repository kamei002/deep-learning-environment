# deep-learning-environment

## example

Dockerfile

``` dockerfile
FROM hkamei/deep-learning-environment

ENV TZ=Asia/Tokyo \
  DEBIAN_FRONTEND=noninteractive \
  LD_LIBRARY_PATH=/usr/local/cuda/lib64:$LD_LIBRARY_PATH \
  PATH=/usr/local/cuda/bin:$PATH \
  LIBRARY_PATH=/usr/local/cuda/lib64:$LD_LIBRARY_PATH
RUN pip3 install cupy

RUN apt-get update

```

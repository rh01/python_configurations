## configuration for tensorflow in PyCharm software with Dcoker container.

This tutorials main descript how to configure Docker tensorflow env in PyCharm IDE.

## Requirements

1. [Docker for Windows](https://www.docker.com/docker-windows)
2. [PyCharm Pro](https://www.jetbrains.com/pycharm/download/download-thanks.html?platform=windows)
3. [Anaconda](www.anaconda.org)

##  Setting Docker images from Dockerfile
 
I will upload [Dockerfile](./Dockerfile) for this tutorial. and Enter into shell.

```bash
docker build -t tensorflow:v1 .
```

soon, setting up Docker tensorflow environment.

## Setting PyCharm

Open PyCharm IDE, and `File->setting`, Searching **Docker**, like this.

![](https://ooo.0o0.ooo/2017/06/26/59509cfb8ca68.png)

In **API URL:** `tcp://localhost:2375`, and leave **Certificates folder** empty.

and open **Docker for Windows**, setting `General` like this. and `Share Drives`, click `C:` and apply.

![](https://ooo.0o0.ooo/2017/06/26/59509d9edb665.png)


![](https://ooo.0o0.ooo/2017/06/26/59509dfd55f24.png)

ok, last come back `PyCharm IDE`, for specific project, You can custom specific interpreter for it, so now you can setting python interpret in Docker for this preject.

`File->setting->Project:xxxx->Project Interpreter-> More-> Add remote->Docker`
like this.

![](https://ooo.0o0.ooo/2017/06/26/59509caa412ef.png)

![](https://ooo.0o0.ooo/2017/06/26/59509f4880b58.png)

`Image name:` write your custom docker development environment.
`Python interpreter path:` (default) python

## Test

open your terminal, enter.

```bash
docker run -it -p 8888:8888 -d --name tensorflow tensorflow:v1
```

![](https://ooo.0o0.ooo/2017/06/26/5950a0cdc65dc.png)

and in `PyCharm IDE`, lanch `Docker`

![](https://ooo.0o0.ooo/2017/06/26/5950a0f19e2a1.png)


That’s all. Time to play with it.



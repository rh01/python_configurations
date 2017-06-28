## Mongodb Configurations

This is a document tutorial about install MongoDb in `Windows10`.

## Install

### Download

Go to [Mongodb Official Website](https://www.mongodb.com/download-center?jmp=nav#community), and Dowload local dir.

![](https://ooo.0o0.ooo/2017/06/28/5953b590dbff5.png)

### Install 

Default Install Path and precession.Default Install Path: `C:\Program Files\MongoDB`


## Configuration

### Test

1. make new dir `data` in `C:\Program Files\MongoDB\Server\3.4` path, and in  `C:\Program Files\MongoDB\Server\3.4\data` create new dir `db`

2. move dir `.\mongod.exe --dbpath "C:\Program Files\MongoDB\Server\3.4\data\db"`, right click and choose  

![](https://ooo.0o0.ooo/2017/06/28/5953b70f111cd.png) and Enter

```shell
.\mongod.exe --dbpath "C:\Program Files\MongoDB\Server\3.4\data\db"
```

Open Browser, go to `http://127.0.0.1:27017/`

![](https://ooo.0o0.ooo/2017/06/28/5953b757eab6a.png)

It's ok!

### Configure Server

1. `Win + X` -- `Windows Power Shell(管理员)` 

![](https://ooo.0o0.ooo/2017/06/28/5953b805e1a2e.png)

2. Create New Dir `C:\Program Files\MongoDB\Server\3.4\data\log`, and move it, and touch new file `mongo.log`

3. Open Terminal, Enter: 

```shell
.\mongod.exe --bind_ip 0.0.0.0 --logpath 'C:\Program Files\MongoDB\Server\3.4\data\log\mongo.log' --logappend --dbpath 'C:\Program Files\MongoDB\Server\3.4\data\db' --install
```

4. `Win + X` -- `计算机管理` 

![](https://ooo.0o0.ooo/2017/06/28/5953ba8f68058.png)

![](https://ooo.0o0.ooo/2017/06/28/5953ba17731fe.png)


![](https://ooo.0o0.ooo/2017/06/28/5953b9cb6ed9d.png)

## License

![](https://img.shields.io/github/license/mashape/apistatus.svg)


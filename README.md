<table style="border-collapse: collapse; border: none;">
  <tr>
    <td>
      <img src="https://github.com/bsc-dom/dataclay/blob/main/docs/_static/dataclay-full.png" alt="dataClay" style="width: 100%;"/>
    </td>
    <td>
      <img src="https://github.com/bsc-dom/API-cargo/blob/main/docs/_static/admire_logo.png" alt="admire" style="width: 100%;"/>
    </td>
  </tr>
</table>


# DataClay 

DataClay is a distributed data store that enables applications to store and access objects in the same format they have in memory, and executes object methods within the data store. These two main features accelerate both the development of applications and their execution.

To ease interoperability and allow dataClay to be used as a backend, a minimal translation layer is offered. This experimental user library offers seamless interaction between \cargo{} files and dataClay objects by translating POSIX file paths into dataClay object identifiers.

## Installation

### Downloading source code archives
+ Go to the DataClay repository [\[here\]](https://github.com/admire-eurohpc/DataClay.git) 
+ Press the green button "<> Code"
+ Download the ZIP

<img src="https://github.com/bsc-dom/API-cargo/blob/main/docs/_static/download_ZIP.png" alt="picture" style="width: 50%;"/>

+ Extract the content of the zip



#### -Or-


### Cloning the repository
#### http
```bash
git clone https://github.com/admire-eurohpc/DataClay.git
```
-or-
#### ssh
```bash
git clone git@github.com:admire-eurohpc/DataClay.git
```

## Usage:

```bash
pip install /<path>/<to>/<plugin>/dataclay-plugin/requirements.txt 
```

+ Modify (if necessary) the python path and/or it's version at the Makefile

+ Change the "/\<path\>/\<to\>/\<plugin\>/" paths

+ Add what is needed to the Makefile

+ Include the plugin to your code #include "/\<path\>/\<to\>/\<plugin\>/dataclay-plugin/dataclayplugin.h"

+ <mark style="background-color: orange">Remember:</mark> When calling the function "dataclay_plugin()" you must write the path to the \</dataclay-plugin\> folder

```bash
make
```
```bash
docker compose -f /<path>/<to>/<plugin>/dataclay-plugin/docker-compose.yaml up
```
```bash
./main
```

+ ...

```bash
docker compose -f /<path>/<to>/<plugin>/dataclay-plugin/docker-compose.yaml down
```

## Recompile Shared Object:
If some changes are done to the dataclay_plugin.c file, the shared object can be recompiled with the following command line:
```bash
gcc -shared -o libdataclayplugin.so -fPIC -I/usr/include/python<python-version> dataclay_plugin.c -lpython<python-version>
```



<!--
parent:
  order: false
-->

<div align="center">
  <h1> Key Locker Repo </h1>
</div>

<div align="center">
  <a href="https://github.com/savour-labs/key-locker/releases/latest">
    <img alt="Version" src="https://img.shields.io/github/tag/savour-labs/key-locker.svg" />
  </a>
  <a href="https://github.com/savour-labs/key-locker/blob/main/LICENSE">
    <img alt="License: Apache-2.0" src="https://img.shields.io/github/license/savour-labs/key-locker.svg" />
  </a>
  <a href="https://pkg.go.dev/github.com/savour-labs/key-locker">
    <img alt="GoDoc" src="https://godoc.org/github.com/savour-labs/key-locker?status.svg" />
  </a>
</div>

key-locker is a key manager for social recovery wallet and mpc wallet private key.

**Tips**: need [Go 1.18+](https://golang.org/dl/)

## 1.create database

```
CREATE DATABASE keylocker DEFAULT CHARACTER SET utf8 DEFAULT COLLATE utf8_general_ci;
```

## 2.install and build

#### 1. build project

```
make key-locker
```

#### 2. migrate database table

```
./key-locker init
```

#### 3. start web server

```bash
./key-locker web
```

#### 4. start rpc server
```bash
./key-locker start 
```

#### 5. start the RPC interface test interface

```
grpcui -plaintext 127.0.0.1:8089
```

## Contribute

### 1.fork repo

fork key-locker to your github

### 2.clone repo

```bash
git@github.com:guoshijiang/key-locker.git
```

### 3. create new branch and commit code

```bash
git branch -C xxx
git checkout xxx

coding

git add .
git commit -m "xxx"
git push origin xxx
```

### 4.commit PR

Have a pr on your github and submit it to the key-locker repository

### 5.review 

After the key-locker code maintainer has passed the review, the code will be merged into the key-locker repo. At this point, your PR submission is complete

### Disclaimer
This code has not yet been audited, and should not be used in any production systems.

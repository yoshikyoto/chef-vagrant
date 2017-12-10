# Vagrant Chef

## Install chef on Host OS

https://downloads.chef.io/chefdk から Chef Development Kit をダウンロード。

`chef -v` などでインストールされているかどうかを確認できます。

```
$ chef -v
Chef Development Kit Version: 2.4.17
chef-client version: 13.6.4
delivery version: master (73ebb72a6c42b3d2ff5370c476be800fee7e5427)
berks version: 6.3.1
kitchen version: 1.19.2
inspec version: 1.45.13
```


## Install vagrant-omnibus

vagrant up 時にchefをVMにインストールします。

```
$ vagrant plugin install vagrant-omnibus
```

Vagrantfileに以下を追記します。

```
config.omnibus.chef_version = :latest
```

これで最新版のchefがインストールされます。

## berkshelf

vagrant plugin install vagrant-berkshelf

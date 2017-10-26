# box

Boxes

``vagrant box list``

``vagrant box add xx/xx local_file.box``

`vagrant box remove xxx`

## search box online

[Search box](https://app.vagrantup.com/boxes/search)

Package 重新打包

> `vagrant package --out a.box`
>
> `vagrant box add xxx a.box`

php box:

```conf
Vagrant.configure("2") do |config|
  config.vm.box = "cacaty/phpwork"
  config.vm.box_version = "1.0.0"
end
```
# Vagrantfile

``vagrant init``

```bash
Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/precise64"
end
```

## 启动

> `vagrant up`

## 进入

> `vagrant ssh`

## 网络和文件共享

> config.vm.network :forwarded_port, guest: 8000, host: 8000
>
> config.vm.network :forwarded_port, guest: 8001, host: 8001
>
> config.vm.synced_folder "src/", "/srv/website"
>


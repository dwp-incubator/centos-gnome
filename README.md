# CentOS base box with gnome

Also includes:
- git
- curl
- vim

## Creating a base box

Once you have provisioned a virtual instance using `vagrant up` you then need to create a base box using the following:

```shell
vagrant halt
vagrant package --base centos-gnome
vagrant box add centos-gnome ./package.box
```


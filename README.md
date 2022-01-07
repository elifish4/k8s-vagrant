## Prerequisite
Install virtualbox:
```shell
https://www.virtualbox.org/wiki/Downloads
```

Install Hasicorp vagrant:
```shell
https://www.vagrantup.com/
```

## Usage

in order to provision the cluster- execute the following commands.

```shell
cd <VAGRANT_FOLDER_PATH>
vagrant up
```

## Set Kubeconfig file varaible:

```shell
cd <VAGRANT_FOLDER_PATH>
cd configs
export KUBECONFIG=$(PWD)/config
```

or you can copy the config file to .kube directory.

```shell
cp config ~/.kube/
```

## Kubernetes Dashboard URL:

```shell
http://localhost:8001/api/v1/namespaces/kubernetes-dashboard/services/https:kubernetes-dashboard:/proxy/#/overview?namespace=kubernetes-dashboard
```

## Kubernetes login token:

Vagrant up will create the admin user token and saves in the configs directory.

```shell
cd <VAGRANT_FOLDER_PATH>
cd configs
cat token
```

## To see status of the cluster:

```shell
cd <VAGRANT_FOLDER_PATH>
vagrant status
```

## To ssh into the nodes:

```shell
cd <VAGRANT_FOLDER_PATH>
vagrant ssh [ master | node01 | node02 ]
```

## To shutdown the cluster:

```shell
vagrant halt
```

## To destroy the cluster:

```shell
vagrant destroy -f
```

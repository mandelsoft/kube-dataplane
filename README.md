# Run local Kubernetes Dataplane

The [kube-apiserver](https://kubernetes.io/releases/download/)
and [etcd](https://github.com/etcd-io/etcd/releases/) executables for amd linux
are included. If another platform or version is desired,
change the content of the `kube` or `etcd` folder, appropriately.

Additionally you need to install [spiff](https://github.com/mandelsoft/spiff/releases)
and [kubectl](https://kubernetes.io/releases/download/) to be usable via your `PATH`.

- setup

run

> `bin/configure`

to create keys, certificates and the kubeconfig.
Alternatively , you can just run

> `spiff merge --interpolation auto/configure`

- run `etcd`

run

> `bin/etcd`

to start the `etcd`.

- run the api server

run 

> `bin/kube-apiserver`

to start the `kube-apiserver`.


- work with your dataplane

execute 

> `bin/kubectl`

with your commands or set

> `export KUBECONFIG="$(pwd)/gen/kube/kubeconfig"`

and use your `kubectl` command.


# kubernetes the hard way #12-dns-addon

#### You will run into a few minor issues setting up core dns from the [12 module](https://github.com/kelseyhightower/kubernetes-the-hard-way/blob/master/docs/12-dns-addon.md) of the k8s the hard way by [Kelsey Hightower](https://github.com/kelseyhightower)

This command, as in the guide:
```
kubectl apply -f https://storage.googleapis.com/kubernetes-the-hard-way/coredns-1.8.yaml
```

Will fail because the link is no longer available. <br>
The simplest solution is just to re-use Kelsey's [core-dns-1.7.yaml](https://github.com/kelseyhightower/kubernetes-the-hard-way/blob/master/docs/12-dns-addon.md) file like this:

```
kubectl apply -f https://raw.githubusercontent.com/kelseyhightower/kubernetes-the-hard-way/master/deployments/coredns-1.7.0.yaml
```

Or fork it to your own repository and change the image version to _1.8_ as the original guide is performed <br>

I have added the file with the updated image so you can use it straight from here:
```
kubectl apply -f https://raw.githubusercontent.com/koenry/k8s-hard-way-core-dns-1.8/main/coredns-1.8.yaml
```

Either way will work! Good luck!

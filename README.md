
# microk8s

Belajar tentang kubernetes menggunakan tool microk8s




## Part 1 : Pengertian k8s(kuberntes)


k8s adalah tools untuk mengelola container (pembungkus aplikasi secara mandiri) di dalam cluster.

microk8s adalah tool k8s yang digunakan pada pengembangan atau jadi playground k8s di komputer lokal. aplikasi serupa : minikube.

## Part 1 : Mengapa menggunakan k8s

- dapat memanagement container runtime seperti docker, podman.  banyak container yang berjalan bisa dapat dikendalikan dengan satu tool k8s.  
 
- memudahkan meningkatkan skalabilitas dengan mereplika pod (di dalam pod biasanya 1 container berjalan). sehingga siap apa bila ada request yang sangat banyak, dan apabila request masih ukuran tahap kecil bisa di kurangsi sesuai beban 

## Used By

This project is used by :

- Personal research



## Description about code 

kode somple untuk deployemet nginx 

```yaml
    apiVersion: apps/v1
    kind: Deployment
    metadata:
    name: nginx-deployment
    labels:
        app: nginx
    spec:
    selector:
        matchLabels:
        app: nginx
    template:
        metadata:
        labels:
            app: nginx
        spec:
        containers:
        - name: nginx
            image: kjackal/mynginx:public
            ports:
            - containerPort: 80

```



- mau deploy dengan nama nginx-deployment dengan tambahan desikupsi app:nginx  dengan container ynag telah ada di docker hub dengan nama image  kjackal/mynginx:public menggunkana port 80.



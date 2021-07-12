# Trivy

Trivy is an open source software, develop by [Aqua](https://www.aquasec.com/), that aim to scan vulnerabilities in containers and other artifacts. 

## Installation

There are so many options to install, depending on the OS you use. All those ways can be found on the url bellow:

- [How to install trivy](https://aquasecurity.github.io/trivy/v0.18.3/installation/)

## Basic Commands


```
$ trivy image [YOUR_IMAGE_NAME]
```

```
$ docker run --rm -it aquasec/trivy
```


## References

https://github.com/aquasecurity/trivy

https://aquasecurity.github.io/trivy/v0.18.3/

https://0x1.gitlab.io/security/Trivy/

buildah push localhost/turing-app oci:/home/marcelo/turing-app.tar
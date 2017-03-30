Build kubernetes rpm binaries
-------------
```bash
git clone --recursive https://github.com/khogeland/kubernetes-rpm-builder
# No RPM currently available for the right version of golang - you must install golang 1.7.x manually
# Maybe with https://github.com/travis-ci/gimme
sudo yum install rpm-build etcd
sudo yum groupinstall "Development Tools"
# make sure you have ample storage space available, both here and in /tm; 5GB is not enough
cd kubernetes-rpm-builder
./build_latest_stable_kubernetes.sh v1.5.3    # argument is the git tag to build
```

# c70n_manifest
Local manifest file for building LineageOS 14.1 for LG Spirit 4G LTE

Steps to build LineageOS for Spirit 4G LTE:

### Initialize the LineageOS source repository

Enter the following to initialize the repository:
```
cd ~/android/system/
repo init -u git://github.com/LineageOS/android.git -b cm-14.1
```
### Get the required local manifest

```
mkdir -p ~/android/system/.repo/local_manifests
curl https://raw.githubusercontent.com/pcfighter/c70n_manifest/cm-14.1/local_manifest.xml > .repo/local_manifests/local_manifest.xml
```

If you are builing on Linux, you don't need Darwin compilers - it is required on OSX only:

```
curl https://raw.githubusercontent.com/pcfighter/c70n_manifest/cm-14.1/rm-darwin.xml > .repo/local_manifests/rm-darwin.xml
```
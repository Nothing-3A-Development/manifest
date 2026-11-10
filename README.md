# Nothing Phone (3a) / (3a) Pro (asteroids)

```
mkdir lineage && cd lineage
repo init -u https://github.com/LineageOS/android.git -b lineage-24.0 --git-lfs
mkdir -p .repo/local_manifests
curl -L https://raw.githubusercontent.com/Nothing-3A-Development/manifest/lineage-24.0/Nothing3A.xml -o .repo/local_manifests/Nothing3A.xml
repo sync -c --no-tags --no-clone-bundle -j$(nproc --all)
source build/envsetup.sh
brunch asteroids
```


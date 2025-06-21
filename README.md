mkdir LOS && cd LOS

repo init -u https://github.com/LineageOS/android.git -b lineage-22.2 --git-lfs
mkdir .repo/local_manifests && wget https://raw.githubusercontent.com/Nothing-3A-Development/manifest/main/Nothing3A.xml -O .repo/local_manifests/Nothing3A.xml

repo sync -c --force-sync --optimized-fetch --no-tags --no-clone-bundle --prune -j$(nproc --all)

#To build for Nothing 3a / Pro aka asteroids
source build/envsetup.sh

breakfast asteroids

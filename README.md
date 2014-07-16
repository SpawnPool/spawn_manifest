SpawnPool Manifest
=============================

Provider of clean AOSP sources
----------------------------------------------------
Serving clean, optimized (Linaro) AOSP builds for a wide range of devices. Including up-to-date optimized stock kernels.

Intended as base ROM source (for creating your own custom ROM) or for normal usage without customization (Clean AOSP build for your device).



Downloading Sources:
----------
* mkdir ~/SpawnPool
* cd ~/SpawnPool
* repo init -u git://github.com/SpawnPool/spawn_manifest -b kk-4.4
* repo sync



Building:
----------
* source build/envsetup.sh
* lunch
* bacon -j#   (number of CPU cores + 1)



Error Solutions:
------------------------
Fixing 'lz4c' not found:
Due to new lossless kernel compression (LZ4) used in some kernels, the lz4c binary is needed. This can be installed by following the steps below:

- wget http://lz4.googlecode.com/files/lz4-r112.tar.gz
- tar -xf lz4-r112.tar.gz
- cd lz4-r112
- make
- sudo make install

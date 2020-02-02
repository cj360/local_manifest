
	curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.githubusercontent.com/cj360/local_manifest/lineage-17.1/local_manifest.xml

Init shallow clone to save time and space:

	repo init --depth=1 -u https://github.com/LineageOS/android -b lineage-17.1

Then to sync up:

	repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

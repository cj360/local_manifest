
	curl --create-dirs -L -o .repo/local_manifests/local_manifest.xml -O -L https://raw.githubusercontent.com/cj360/local_manifest/quartz/local_manifest.xml

		and place it in ~/Android/.repo/local_manifest.xml (or ~/'name you chose'/.repo)

Init shallow clone to save time and space:

	repo init --depth=1 -u https://github.com/AOSPA/manifest -b quartz

Then to sync up:

	repo sync -c -j$(nproc --all) --force-sync --no-clone-bundle --no-tags

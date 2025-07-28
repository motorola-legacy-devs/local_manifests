## Sync the manifest:

```
mkdir .repo/local_manifests
```
```
curl https://raw.githubusercontent.com/motorola-legacy/local_manifests/master/$DEVICE/$MANIFEST_NAME > .repo/local_manifests/manifest.xml
```
be sure to replace $DEVICE and $MANIFEST_NAME with a device codename and manifest name, that are available.

Example:
```
mkdir .repo/local_manifests && curl https://raw.githubusercontent.com/motorola-legacy/local_manifests/master/jeter/manifest-q.xml > .repo/local_manifests/manifest.xml
```

After that do 
```repo sync --force-sync --no-tags --no-clone-bundle -c```
to get both the rom and device sources.

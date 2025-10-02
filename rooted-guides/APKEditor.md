## Requirements

* [LSPosed](https://github.com/JingMatrix/LSPosed)
* [CorePatch](https://github.com/LSPosed/CorePatch)
* [APKEditor](https://github.com/REAndroid/APKEditor)
* [j-hc ReVanced CLI](https://github.com/j-hc/revanced-cli)
* ReVanced patches or any related fork
* [YouTube APK](https://www.apkmirror.com/apk/google-inc/youtube)

# Prepare & Patch

# Extract YouTube's signature data
```
java -jar ApkEditor_X.X.X.jar d -t sig -i YouTube_XX.XX.XX.apk
```

# Patch YouTube
```
java -jar revanced-cli-X.X.X-all.jar patch -p patches-X.XX.X.rvp -d "GmsCore support" --unsigned -f --purge -o ReVanced_XX.XX.XX.apk YouTube_XX.XX.XX.apk
```

# Sign with fake signature
```
java -jar ApkEditor_X.X.X.jar b -t sig -i ReVanced_XX.XX.XX.apk -sig $PWD/YouTube_XX.XX.XX_decompile_sig/signatures -o ReVanced_XX.XX.XX_Root.apk
```

# Final apk
* **ReVanced_XX.XX.XX_Root.apk**

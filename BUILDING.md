# Building

Build debug

```console
./gradlew assembleDebug
```

Build release

```console
./gradlew assembleRelease
```

Sign APK with dumb key

```console
keytool -genkeypair -v \
    -keystore testkey.keystore \
    -alias testkey \
    -keyalg RSA \
    -keysize 2048 \
    -validity 3650 \
    -storepass 123123 \
    -keypass 123123 \
    -dname "CN=Test Key, OU=Test, O=Test, L=Test, S=Test, C=Test"

# Find apksigner
find $ANDROID_HOME -name "apksigner"

# Build release APK
./gradlew assembleRelease

# Sign with apksigner
/path/to/apksigner sign --ks testkey.keystore --ks-pass pass:123123 app/build/outputs/apk/release/app-release-unsigned.apk

# Upload
mv app/build/outputs/apk/release/app-release-unsigned.apk app/build/outputs/apk/release/locatemydevice-v1.1.0.apk
tag=$(gh release -R thewh1teagle/locatemydevice view --json tagName --jq '.tagName')
gh release upload -R thewh1teagle/locatemydevice $tag app/build/outputs/apk/release/locatemydevice-v1.1.0.apk --clobber
```
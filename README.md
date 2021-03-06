- Android 树的 build/target/product/security 目录中提供了测试密钥。使用 make 编译 Android OS 映像便可使用这些测试密钥对所有 .apk 文件进行签名。由于这些测试密钥是公开的，任何人都可以使用相同的密钥对他们自己的 .apk 文件签名，这样他们就能够替换或盗用您的操作系统映像中编译的系统应用。因此，您必须使用只有您自己才能访问的特殊“发布密钥”集对公开发布或部署的 Android OS 映像进行签名。

- The Android tree includes test-keys under build/target/product/security. Building an Android OS image using make will sign all .apk files using the test-keys. Since the test-keys are publicly known, anybody can sign their own .apk files with the same keys, which may allow them to replace or hijack system apps built into your OS image. For this reason it is critical to sign any publicly released or deployed Android OS image with a special set of release-keys that only you have access to.

https://source.android.com/devices/tech/ota/sign_builds
https://android.googlesource.com/platform/build/+/donut-release/target/product/security/platform.x509.pem
https://www.jianshu.com/p/69525b2b4937
https://github.com/h4de5ing/TestSystemPermission/releases

```
-----BEGIN CERTIFICATE-----
MIIEqDCCA5CgAwIBAgIJALOZgIbQVs/6MA0GCSqGSIb3DQEBBAUAMIGUMQswCQYD
VQQGEwJVUzETMBEGA1UECBMKQ2FsaWZvcm5pYTEWMBQGA1UEBxMNTW91bnRhaW4g
VmlldzEQMA4GA1UEChMHQW5kcm9pZDEQMA4GA1UECxMHQW5kcm9pZDEQMA4GA1UE
AxMHQW5kcm9pZDEiMCAGCSqGSIb3DQEJARYTYW5kcm9pZEBhbmRyb2lkLmNvbTAe
Fw0wODA0MTUyMjQwNTBaFw0zNTA5MDEyMjQwNTBaMIGUMQswCQYDVQQGEwJVUzET
MBEGA1UECBMKQ2FsaWZvcm5pYTEWMBQGA1UEBxMNTW91bnRhaW4gVmlldzEQMA4G
A1UEChMHQW5kcm9pZDEQMA4GA1UECxMHQW5kcm9pZDEQMA4GA1UEAxMHQW5kcm9p
ZDEiMCAGCSqGSIb3DQEJARYTYW5kcm9pZEBhbmRyb2lkLmNvbTCCASAwDQYJKoZI
hvcNAQEBBQADggENADCCAQgCggEBAJx4BZKsDV04HN6qZezIpgBuNkgMbXIHsSAR
vlCGOqvitV0Amt9xRtbyICKAx81Ne9smJDuKgGwms0sTdSOkkmgiSQTcAUk+fArP
GgXIdPabA3tgMJ2QdNJCgOFrrSqHNDYZUer3KkgtCbIEsYdeEqyYwap3PWgAuer9
5W1Yvtjo2hb5o2AJnDeoNKbf7be2tEoEngeiafzPLFSW8s821k35CjuNjzSjuqtM
9TNxqydxmzulh1StDFP8FOHbRdUeI0+76TybpO35zlQmE1DsU1YHv2mi/0qgfbX3
6iANCabBtJ4hQC+J7RGQiTqrWpGA8VLoL4WkV1PPX8GQccXuyCcCAQOjgfwwgfkw
HQYDVR0OBBYEFE/koLPdnLop9x1yh8Tnw48ghsKZMIHJBgNVHSMEgcEwgb6AFE/k
oLPdnLop9x1yh8Tnw48ghsKZoYGapIGXMIGUMQswCQYDVQQGEwJVUzETMBEGA1UE
CBMKQ2FsaWZvcm5pYTEWMBQGA1UEBxMNTW91bnRhaW4gVmlldzEQMA4GA1UEChMH
QW5kcm9pZDEQMA4GA1UECxMHQW5kcm9pZDEQMA4GA1UEAxMHQW5kcm9pZDEiMCAG
CSqGSIb3DQEJARYTYW5kcm9pZEBhbmRyb2lkLmNvbYIJALOZgIbQVs/6MAwGA1Ud
EwQFMAMBAf8wDQYJKoZIhvcNAQEEBQADggEBAFclUbjZOh9z3g9tRp+G2tZwFAAp
PIigzXzXeLc9r8wZf6t25iEuVsHHYc/EL9cz3lLFCuCIFM78CjtaGkNGBU2Cnx2C
tCsgSL+ItdFJKe+F9g7dEtctVWV+IuPoXQTIMdYT0Zk4u4mCJH+jISVroS0dao+S
6h2xw3Mxe6DAN/DRr/ZFrvIkl5+6bnoUvAJccbmBOM7z3fwFlhfPJIRc97QNY4L3
J17XOElatuWTG5QhdlxJG3L7aOCA29tYwgKdNHyLMozkPvaosVUz7fvpib1qSN1L
IC7alMarjdW4OZID2q4u1EYjLk/pvZYTlMYwDlE448/Shebk5INTjLixs1c=
-----END CERTIFICATE-----
```
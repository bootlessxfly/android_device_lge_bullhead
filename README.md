# Maru on the Nexus 5X

## Vendor files

Maru uses [android-prepare-vendor](https://github.com/anestisb/android-prepare-vendor) to generate a complete vendor tree for bullhead, including `vendor.img`.
This allows you to flash your build without having to first flash the latest stock image.
If your build hangs on the Google boot logo, please ensure that you have generated a complete vendor tree with android-prepare-vendor:
```shell
# from outside your Maru working tree
git clone https://github.com/anestisb/android-prepare-vendor
cd android-prepare-vendor
./execute-all.sh -d bullhead -o ./vendor -f -b OPM7.181205.001 --debugfs
```
The build id can be obtained from [Google's list of factory images](https://developers.google.com/android/images#bullhead).
Once you have the `./vendor/bullhead` directory, you can copy it over `vendor/lge/bullhead` in your Maru working tree.

If you want to use an alternative method of obtaining the vendor files that does not generate `vendor.img`, see this [PR](https://github.com/maruos/android_device_lge_bullhead/pull/1) for an easy workaround.

## Contributing

See the [main Maru OS repository](https://github.com/maruos/maruos) for more
info.

## Licensing

[Apache 2.0](https://github.com/maruos/maruos/blob/master/LICENSE)

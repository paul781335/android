
https://medium.com/@BushMinusZero/cuttlefish-on-arm64-in-aws-b1f60d937614

 setup

Create ubuntu arm a1 metal eu west 1 ireland
Security group add my ip port 22 ssh access
Disk size set to 256gb


Cd base before line :-




sudo dpkg-buildpackage --no-sign

After fix broken install line do this From readme



for dir in base frontend; do
    pushd $dir
    dpkg-buildpackage -uc -us
    popd
done

Then go to folder

/home/ubuntu/cuttlefish-common/android-cuttlefish/base

And run previous command :-

sudo dpkg-buildpackage --no-sign



https://medium.com/@BushMinusZero/cuttlefish-on-arm64-in-aws-b1f60d937614

Create ubuntu arm a1 metal eu west 1 ireland
Security group add my ip port 22 ssh access
Disk size set to 256gb

cd base before line :-

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

follow steps 3 thru 9 here :-

https://android.googlesource.com/device/google/cuttlefish/

aosp_cf_arm64_only_phone-img-9374348.zip
cvd-host_package.tar.gz

vnc support removed from later versions of cuttlefish, WebRTC is the way to go

install app :-
    adb install -r app-debug.apk

start app :-
    adb shell am start -a  android.intent.action.MAIN -n com.example.myapplication/.MainActivity
    
Install Frida :-

https://book.hacktricks.xyz/mobile-pentesting/android-app-pentesting/frida-tutorial#installation

Then Frida Hooks :- 

https://11x256.github.io/Frida-hooking-android-part-1/

Cuttlefish WebRTC :-

https://source.android.com/docs/setup/create/cuttlefish-ref-webrtc


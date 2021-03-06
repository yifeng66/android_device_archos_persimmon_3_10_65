Device repository for Archos 50 Cobalt (CyanogenMod)
===========================
For Stock 3.10.65 kernel

Это дерево создано на основе работы @divis1969 , без него ничего бы не было.

Getting Started
---------------

Initialize a repository with CyanogenMode:

    repo init -u git://github.com/CyanogenMod/android.git -b cm-14.1
    
Sync sources:    

    repo sync
    
Build the code:
    
    cd device
    mkdir archos
    cd archos
    git clone https://github.com/olegsvs/android_device_archos_persimmon_3_10_65 persimmon
    cd persimmon/patches
    . apply-patches.sh
    cd vendor
    mkdir archos
    cd archos
    git clone https://github.com/olegsvs/android_vendor_archos_persimmon_3_10_65 persimmon
    cd ../../
    source build/envsetup.sh
    breakfast persimmon
    make -j 4 bacon

Current state
-------------

- Cyanogen boots
- Touch, screen, keyboard working
- Wifi is working
- Audio is working
- Telephony is working (see Known Issues)
    - USIM (3G) supported
    - Incoming/outgoung call
    - SMS, USSD
    - Data connectivity
- GPS
- Bluetooth (pairing only testes so far)
- Sensors

Known Issues
-------------
- Livedisplay (lagging)
- FMRadio
- VoLTE
- Gps without network connections?
- Camera
- Hardware OMX codecs are not working

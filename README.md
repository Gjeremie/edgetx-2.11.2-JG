**Version EdgeTX 2.11.2 avec mes modif suivantes JG**

modif vario pour avoir son continu (pas encore fait)

**Pour faire build edgetx:**

info tiré de : https://github.com/EdgeTX/edgetx/wiki/Building-radio-firmware-in-a-webbrowser-with-Gitpod <br>
options: https://github.com/EdgeTX/edgetx/wiki/Compilation-options <br> <br>


**CODE: <br>**

https://gitpod.io/#https://github.com/edgetx/edgetx/tree/2b920a014b0d69684eecfc20a74855d8b553e005


cmake -Wno-dev -DPCB=X7 -DPCBREV=MT12 -DDEFAULT_MODE=2 -DCMAKE_BUILD_TYPE=Release ../

make arm-none-eabi-configure

make -C arm-none-eabi -j\`nproc\` firmware

cd arm-none-eabi <br>
mv firmware.bin edgetx_mt12_3d1e7a9_6_dec_2024.bin

 <br> <br>
**ou AUTRE CODE: <br>**

https://gitpod.io/#https://github.com/Gjeremie/edgetx-2.11.2-JG

cd /workspace/edgetx-2.11.2-JG/

FLAVOR=mt12 tools/build-gh.sh

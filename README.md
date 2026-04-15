**Version EdgeTX 2.11.2 avec mes modif suivantes JG**

modif vario pour avoir son continu (pas encore fait)

**Pour faire build edgetx:**

info tiré de : https://github.com/EdgeTX/edgetx/wiki/Building-radio-firmware-in-a-webbrowser-with-Gitpod <br>
options: https://github.com/EdgeTX/edgetx/wiki/Compilation-options <br> <br>


**CODE: <br>**

dans ma Fork EdgeTX:

cliquer sur code puis codespace pour create new code space

laisser charger puis une fois dans le terminal (si ouvre pas terminal cliquer sur le + en haut barre terminal et New Terminal) taper les commandes:




cmake -DPCB=X7 -DPCBREV=MT12 -DDEFAULT_MODE=2 -DCMAKE_BUILD_TYPE=Release /workspaces/edgetx-2.11.2-JG



make arm-none-eabi-configure



make -C arm-none-eabi -j$(nproc) firmware



Mon firmware.bin perso doit etre sur la gauche dans le dossier : arm-none-eabi





 <br> <br>
**ou AUTRE CODE: <br>**

https://gitpod.io/#https://github.com/Gjeremie/edgetx-2.11.2-JG

cd /workspace/edgetx-2.11.2-JG/

FLAVOR=mt12 tools/build-gh.sh

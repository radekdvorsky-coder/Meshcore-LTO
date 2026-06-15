# RAK4631 repeater LTO build

Tento ZIP uz ma pro RAK4631 zakomentovany build flag:

```ini
;  -D NRF52_POWER_MANAGEMENT  ; disabled for LTO low-voltage boot
```

Cilovy firmware je:

```bash
RAK_4631_repeater
```

## Nejjednodussi lokalni build

```bash
pip install platformio
cd MeshCore-main
export FIRMWARE_VERSION=v1.16.0-LTO
export DISABLE_DEBUG=1
mkdir -p out
sh build.sh build-firmware RAK_4631_repeater
```

Vysledek bude v `out/*.uf2` nebo v `.pio/build/RAK_4631_repeater/firmware.uf2`.

## GitHub Actions cesta

1. Nahraj obsah tohoto ZIPu do noveho GitHub repozitare.
2. Otevri zalozku Actions.
3. Spust workflow `Build RAK4631 repeater LTO firmware` pres `Run workflow`.
4. Po dokonceni stahni artifact `RAK4631-repeater-LTO-UF2`.

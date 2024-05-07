Elite: Dangerous Star Names: [![Get it from the Workshop](https://img.shields.io/badge/steam-%23000000.svg?style=for-the-badge&logo=steam&logoColor=white)](https://steamcommunity.com/sharedfiles/filedetails/?id=2904925738)

Even More Names: [![Get it from the Workshop](https://img.shields.io/badge/steam-%23000000.svg?style=for-the-badge&logo=steam&logoColor=white)](https://steamcommunity.com/sharedfiles/filedetails/?id=2900560084)

# Elite: Dangerous Star Names for Stellaris

## Building the list

Data dumps can be downloaded from https://spansh.co.uk/dumps

This Python script is certainly slow (~2.5h on my desktop).

# Uploading

```
STEAMUSER=
WBI=""
for file in $(ls steamcmd*.txt | sort -r); do
  WBI="${WBI} +workshop_build_item /code/${file}"
done
podman run -v $PWD:/code:ro -v steamcmd-data:/data -v steamcmd-root:/root/.local/share/Steam -it steamcmd/steamcmd:debian-12 \
  +login $STEAMUSER ${WBI} +quit
```

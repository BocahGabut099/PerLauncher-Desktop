# PerLauncher PC memory profiles

The memory presets only change Minecraft's Java heap settings. They do not modify Windows, GPU drivers, or the graphics options inside Minecraft.

| PC memory | Potato PC | Balanced | Performance |
|---|---:|---:|---:|
| Up to 3 GiB | 768 MiB | 1,024 MiB | 1,024 MiB |
| 4 GiB | 1,024 MiB | 1,536 MiB | 1,792 MiB |
| 6 GiB | 1,536 MiB | 2,048 MiB | 2,560 MiB |
| 8 GiB | 2,048 MiB | 3,072 MiB | 4,096 MiB |
| More than 8 GiB | 2,048 MiB | 4,096 MiB | 6,144 MiB |

New installations also receive lower concurrent task/download defaults on PCs with less than 4 GiB or 8 GiB RAM. Existing user preferences are preserved because the settings system only applies registered defaults when a value has not been saved before.

For low-end PCs, start with **Potato PC**, use a lower in-game render distance, avoid heavy shader packs, and close unnecessary applications. Allocating more RAM is not automatically faster; too much allocation can starve Windows and cause paging.

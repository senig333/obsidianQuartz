# cambiar nombre a contenedor LXC proxmox

Para cambiar el nombre de un contenedor LXC en Proxmox, sigue estos pasos:

1. Detén el contenedor LXC:
```bash
pct stop <ID_del_contenedor>
```

2. Utiliza el comando `pct set` para cambiar el nombre del contenedor:
```bash
pct set <ID_del_contenedor> --hostname <nuevo_nombre_del_contenedor>
```

3. Verifica que el cambio se haya aplicado correctamente:
```bash
pct config <ID_del_contenedor>
```

4. Inicia el contenedor nuevamente:
```bash
pct start <ID_del_contenedor>
```

Este proceso actualiza automáticamente la configuración interna del contenedor para reflejar el nuevo nombre de host[^1]. Es un método sencillo y seguro que no requiere editar manualmente archivos de configuración[^1].

Alternativamente, puedes cambiar el nombre del contenedor a través de la interfaz gráfica de Proxmox:

1. Selecciona el contenedor en el árbol de recursos.
2. En el panel central, elige "Options".
3. Haz clic en el botón "Edit" junto a "Name".
4. Introduce el nuevo nombre y confirma[^2].

Recuerda que estos cambios se aplican al nombre del contenedor dentro de Proxmox y al hostname del sistema operativo dentro del contenedor.

<div style="text-align: center">⁂</div>

[^1]: https://nosololinux.es/modificar-el-nombre-de-un-contenedor-lxc-en-proxmox/

[^2]: https://www.fpgenred.es/proxmox/cambiar_el_nombre_de_una_mv.html

[^3]: https://aulautil.com/unidad/curso/proxmox/taller-8-instalacion-de-contenedores-lxc-y-docker-en-proxmox/

[^4]: https://www.youtube.com/watch?v=2NzLYKRVRtk

[^5]: https://forum.proxmox.com/threads/rename-container-proxmox-5.35319/

[^6]: https://forum.proxmox.com/threads/renaming-an-lxc.34517/

[^7]: https://www.reddit.com/r/Proxmox/comments/1icl2he/how_do_i_rename_my_proxmox_node_with_lxc/?tl=es-es

[^8]: https://algodelinux.com/proxmox-cambiar-el-hostname-de-la/


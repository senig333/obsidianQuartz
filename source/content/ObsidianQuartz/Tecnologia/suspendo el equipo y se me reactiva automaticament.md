<img src="https://r2cdn.perplexity.ai/pplx-full-logo-primary-dark%402x.png" class="logo" width="120"/>

# suspendo el equipo y se me reactiva automaticamente manjaro

Si su equipo con Manjaro se suspende y se reactiva automáticamente, hay varias posibles soluciones para este problema:

1. Deshabilitar el despertar por dispositivos USB:
Ejecute el siguiente comando para ver qué dispositivos pueden despertar el sistema:

```bash
cat /proc/acpi/wakeup
```

Luego deshabilite los dispositivos no esenciales con:

```bash
echo DISPOSITIVO > /proc/acpi/wakeup
```

Reemplace DISPOSITIVO con el nombre del dispositivo que quiere deshabilitar[^2].
2. Crear una regla udev para deshabilitar el despertar:
Cree un archivo en /etc/udev/rules.d/ con una regla como esta:

```
KERNEL=="0000:00:01.1", ATTR{power/wakeup}="disabled"
```

Ajuste los valores según los dispositivos de su sistema[^2].
3. Verificar la configuración de suspensión:
Revise el archivo /etc/systemd/sleep.conf y asegúrese de que las opciones de suspensión estén habilitadas correctamente[^2].
4. Actualizar el kernel y los controladores:
Asegúrese de tener la última versión del kernel y los controladores, especialmente si tiene hardware AMD[^6].
5. Agregar parámetro al kernel:
Añada rtc_cmos.use_acpi_alarm=1 a los parámetros del kernel en el gestor de arranque[^6].

Si el problema persiste, puede ser útil revisar los logs del sistema después de un intento de suspensión para identificar cualquier error o conflicto específico[^7].

<div style="text-align: center">⁂</div>

[^1]: https://www.reddit.com/r/ManjaroLinux/comments/r4tr19/help_with_automatic_suspend/

[^2]: https://wiki.archlinux.org/title/Power_management/Suspend_and_hibernate

[^3]: https://forum.manjaro.org/t/kde-problem-suspend-resume/166574

[^4]: https://forum.manjaro.org/t/bizarre-automatic-suspend-behavior/111446

[^5]: https://forum.manjaro.org/t/recommended-solution-for-kernel-suspend-problem/107727

[^6]: https://community.frame.work/t/resolved-systemd-suspend-then-hibernate-wakes-up-after-5-minutes/39392

[^7]: https://forum.manjaro.org/t/cannot-resume-from-suspend/155420

[^8]: https://forum.manjaro.org/t/wake-up-immediately-after-suspend-and-shut-down/131686

[^9]: https://forum.pine64.org/showthread.php?tid=14180

[^10]: https://bbs.archlinux.org/viewtopic.php?id=250902

[^11]: https://forum.garudalinux.org/t/black-screen-after-wake-up-from-sleep-hibernate/26919


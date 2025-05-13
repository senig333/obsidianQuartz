# como ver procesos en docker

Para ver los procesos en Docker, puedes utilizar varios comandos:

1. **docker ps**: Este comando muestra los contenedores en ejecución[^2][^5].
    - Usa `docker ps -a` para listar todos los contenedores, incluyendo los que no están en ejecución[^2][^5].
2. **docker top**: Muestra todos los procesos en ejecución de un contenedor específico[^6].
3. **docker stats**: Proporciona estadísticas en tiempo real sobre el uso de recursos de los contenedores, incluyendo CPU, memoria y red[^5][^6].
4. **docker logs**: Muestra los logs de un contenedor, lo cual puede ser útil para ver la actividad y los procesos que se han ejecutado[^4][^7].
5. **docker exec**: Te permite ejecutar comandos dentro de un contenedor en ejecución. Por ejemplo, puedes usar `docker exec -it <nombre_del_contenedor> bash` para acceder a una shell dentro del contenedor y luego usar comandos como `ps` o `top`[^4].
6. **docker inspect**: Proporciona información detallada sobre un contenedor, incluyendo su configuración y estado[^5][^6].

Estos comandos te ayudarán a monitorizar y gestionar los procesos en tus contenedores Docker de manera efectiva.

<div style="text-align: center">⁂</div>

[^1]: https://dockertips.com/Monitorizacion_en_Docker

[^2]: https://aprenderbigdata.com/comandos-docker/

[^3]: https://www.youtube.com/watch?v=ImLoqbY9DNA

[^4]: https://coffeebytes.dev/es/tutorial-de-comandos-basicos-de-docker/

[^5]: https://www.ionos.es/digitalguide/servidores/know-how/comandos-de-docker/

[^6]: https://www.hostinger.com/es/tutoriales/comandos-docker

[^7]: https://dev.to/zeedu_dev/docker-curso-practico-con-ejemplos-2fkd

[^8]: https://labex.io/es/tutorials/docker-docker-display-running-processes-in-container-271507


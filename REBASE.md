# Documentación de limpieza con Rebase

## ¿Qué se hizo?
1. Se generaron 3 commits con mensajes genéricos y poco descriptivos ("Arreglos", "Cambios", "Actualización de cosas").
2. Se utilizó el comando `git rebase -i --root` para reescribir el historial local desde el origen.
3. Se aplicó la acción `reword` al primer y tercer commit para modificar su mensaje por uno descriptivo.
4. Se aplicó la acción `squash` al segundo commit ("Cambios") para fusionarlo con el primer commit, eliminando redundancias.
5. Se forzó la actualización del repositorio remoto usando `git push --force`.

## ¿Por qué?
Mantener un historial limpio ayuda a la legibilidad del proyecto. Mensajes como "Cambios" no explican qué aporta el commit. Con `squash` agrupamos modificaciones que pertenecen al mismo hito y con `reword` les damos un contexto claro. El uso de `--force` es obligatorio porque reescribimos el pasado y el historial local difiere del remoto.

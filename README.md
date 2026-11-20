# Agentes de Distribuidora Tumalac

Abrí este repositorio como proyecto en Codex con soporte para subagentes. Desde ahí podés pedirle tareas al agente principal y decirle explícitamente cuándo querés que delegue.

> Usá los subagentes Redacción y Revisión para preparar un borrador de una publicación y verificarlo antes de entregármelo.

## Cambiar las reglas

Editá [AGENTS.md](AGENTS.md) en GitHub. Las reglas de ese archivo se aplican al agente principal y a todas las tareas delegadas. Guardá los cambios en `main` y abrí una sesión de Codex con la versión actualizada del repositorio.

## Agregar una imagen obligatoria

1. Subí la imagen a [reglas/imagenes/](reglas/imagenes/) con **Add file → Upload files**.
2. Agregá una fila en la tabla de [reglas/imagenes.md](reglas/imagenes.md). Escribí la ruta relativa a la raíz, qué tareas requieren la imagen y si hay que insertarla o usarla como referencia visual.
3. Guardá ambos cambios en `main`. Al recibir una tarea, el agente principal indicará al subagente qué imágenes debe abrir y cómo usarlas. Si falta una imagen aplicable o el entorno no permite verla, la tarea queda pendiente de validación.

## Administrar subagentes

Los perfiles están en [`.codex/agents/`](.codex/agents/). Para sumar uno, duplicá un archivo TOML, elegí un `name` único y adaptá `description` y la parte específica de `developer_instructions`. Conservá las instrucciones sobre reglas compartidas e imágenes. Para quitar un perfil, eliminá su archivo y abrí una nueva sesión.

GitHub guarda las reglas, las imágenes y los perfiles. La ejecución ocurre en Codex.

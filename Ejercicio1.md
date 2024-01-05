# Práctica Git & GitHub

## Preguntas

#### 1. ¿Qué comando utilizaste en el paso 11? ¿Por qué?

git reset --hard HEAD~1
Este comando se utiliza para deshacer el último commit y perder los cambios en el working copy.

#### 2. ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

git reflog
git reset --hard
Primero usamos git reflog para obtener el hash del commit antes de realizar el reset, y luego git reset --hard <hash_del_commit> para regresar al estado anterior.

#### 3. El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

No, porque la rama main ya contenía todos los cambios de la rama styled. Es un "fast-forward".

#### 4. El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

Sí, ya que ambas ramas (styled y htmlify) modificaron las mismas líneas del archivo.

#### 5. El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

No, porque la rama styled ya contenía todos los cambios de la rama main. Es un "fast-forward".

#### 6. ¿Qué comando o comandos utilizaste en el paso 25?

git log --graph --oneline --all
Esto muestra el historial de commits en un formato gráfico.

#### 7. El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

Sí, porque la rama title es una versión avanzada de la rama main y no tiene commits adicionales desde el punto de bifurcación.

#### 8. ¿Qué comando o comandos utilizaste en el paso 27?

git reset HEAD~1
Esto deshace el merge sin perder los cambios en el working copy.

#### 9. ¿Qué comando o comandos utilizaste en el paso 28?

git checkout -- .
Esto descarta los cambios en el working copy.

#### 10. ¿Qué comando o comandos utilizaste en el paso 29?

git branch -D title
Esto elimina la rama title incluso si no está fusionada.

#### 11. ¿Qué comando o comandos utilizaste en el paso 30?

git reflog
git reset --hard
Usamos git reflog para obtener el hash del commit antes de realizar el reset, y luego git reset --hard para regresar al estado anterior.

#### 12. ¿Qué comando o comandos utilizaste en el paso 32?

git log --oneline
git checkout
Esto nos permite volver al commit inicial.

#### 13. ¿Qué comando o comandos utilizaste en el punto 33?

git reflog
git reset --hard
Usamos git reflog para obtener el hash del commit final antes de realizar el reset, y luego git reset --hard para regresar al estado final.

#### 14. Crear los siguientes tags: inicial, styled, htmlify, title

git tag inicial
git tag styled
git tag htmlify
git tag title

#### 15. ¿Qué comando o comandos utilizaste para ir al tag htmlify?

git checkout htmlify

#### 16. ¿Qué comando o comandos utilizaste para volver a la rama main?

git checkout main

#### 17. ¿Qué comando o comandos utilizaste para subir a GitHub todas las ramas y todos los tags?

git push origin --all
git push origin --tags
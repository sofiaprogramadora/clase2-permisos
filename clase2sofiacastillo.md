1. ¿Qué sucede al hacer?
cd staff
(Img 1.)
Vamos a ir al directorio staff

2. ¿Qué sucede al hacer?
cd lib
(Img 2.)
va a dar este error: -bash: cd: lib: No such file or directory
porque el directorio lib no existe dentro de staff

3. ¿Qué sucede al hacer?
cd /lib
(Img 3.)
Vamos a ir al directorio lib dentro de ROOT

4. ¿Qué sucede al hacer?
cd ..
(Img 4.)
Vamos a ir al directorio anterior

5. ¿Qué sucede al hacer?
cd /users/staff
(Img 5.)
Vamos a quedar en el mismo directorio porque desde la raiz vamos a users y de users a staff.

6. ¿Qué sucede al hacer?
pwd
(Img 6.)
vamos a mostrar "/home/users/staff"

7. ¿Qué sucede al hacer?
rm staff
(Img 7.)
Nos da un error porque: staff/ es un directorio y tiene archivos dentro

8. ¿Qué sucede al hacer?
rm -r staff
(Img 8.)
Como (Ahora) no hay archivos en staff y usamos el flag --recursive entonces se borra la carpeta

9. ¿ERROR O NO?
(Img 9.)
mv staff1 staff
Si, porque staff1 no existe

10. ¿Cómo ejecutamos el programa X?
/bin/x
(Img 10.)

11. ¿Cómo ejecutamos el programa X?
x
(Img 11.)

12. ¿Cómo ejecutamos el programa X?
./bin
(Img 12
.)
13. Si el usuario tiene acceso a / y a users / entonces ¿Qué tan seguro es el sistema Linux?
Es seguro si el usuario no tiene acceso a root.

14. ¿ What is this ?
ls -la
muestra TODOS los archivos en una lista con todos los datos

15. ¿Qué no podemos hacer?
Escribir (x)
(Img 15.)
(Permisos!)

1) d rwx r-x r-x

(d) = directorio
(rwx) = Todos los permisos
(r-x) = Leer y ejecutar
(r-x) = Leer y ejecutar

2) - rwx r-x r-x

(-) = Es un archivo
(rwx) = Todos los permisos
(r-x) = Leer y ejecutar
(r-x) = Leer y ejecutar

3) d r-x rwx -wx

(d) = directorio
(r-x) = Leer y ejecutar
(rwx) = Todos los permisos
(-wx) = Escribir y ejecutar

4) - rw- rw- rw-

(-) = Es un archivo
(rw-) = Leer y escribir
(rw-) = Leer y escribir
(rw-) = Leer y escribir

5) - rw- r-- r--

(-) = Es un archivo
(rw-) = Leer y escribir
(r--) = Leer
(r--) = Leer

6) d -w- rwx -w-

(d) = directorio
(rw-) = Leer y escribir
(rwx) = Todos los permisos
(-w-) = Escribir

7) 414

(r = 4, w = 2, x = 1)
(4) = r
(1) = x
(4) = r

8) 422

(r = 4, w = 2, x = 1)
(4) = r
(2) = w
(2) = w

9) 303

(r = 4, w = 2, x = 1)
(3) = w, x
(0)
(3) = w, x

10) 404

(r = 4, w = 2, x = 1)
(4) = r
(0)
(4) = r

11) 755

(r = 4, w = 2, x = 1)
(7) = r, w, x
(5) = r, x
(5) = r, x

12) 766

(r = 4, w = 2, x = 1)
(7) = r, w, x
(6) = r, w
(6) = r, w

13) 711

(r = 4, w = 2, x = 1)
(7) = r, w, x
(1) = x
(1) = x

14) 070

(r = 4, w = 2, x = 1)
(0)
(7) = r, w, x
(0)

15) Crear un archivo

touch file.txt

16) Asignar los permisos a usuario tal que éste pueda leer y escribir y que no tengan privilegios ni grupo ni otros

chmod 600 file.txt

17) Al mismo archivo asignarle permisos de lectura y escritura a grupo

chmod 760 file.txt

18) Al archivo, cambiar el permiso del usuario para que se pueda ejecutar

chmod 766 file.txt

19) A ese mismo archivo asignarle permiso de lectura a otros


chmod 762 file.txt

20) Crear un archivo

touch newfile.txt

21) Quitarle todos los permisos

chmod 000 newfile.txt

22) Abrirlo con sublime

subl newfile.txt

23) ¿Qué error aparece?

(Al hacer ctrl + s)
Unable to save ~/Escritorio/Escritorio/desafiolatam/Bash/Clase2/newfile.txt
Error: /home/sofia/Escritorio/Escritorio/desafiolatam/Bash/Clase2/newfile.txt is readonly

24) Dar permisos de lectura al dueño

chmod 400 newfile.txt

25) Abrirlo con sublime, modificarlo y guardarlo.

(Modificado)

26) Dar permisos de escritura

chmod 600 newfile.txt

27) Crea un archivo .txt utilizando sudo

sudo touch newsudofile.txt

28) ¿Qué usuario queda al hacer ls -la ?

-rw-r--r-- 1 root  root     0 oct 19 10:40 newsudofile.txt

29) Cambia los permisos para que todos puedan escribir en él sin sudo

chmod 222 newsudofile.txt

30) ¿Permitido?

no:
chmod: changing permissions of 'newsudofile.txt': Operation not permitted

31) Cambia el owner a tu usuario (chown)

sudo chown sofia newsudofile.txt

32) Confirma el cambio con ls -la

-rw-r--r-- 1 sofia root     0 oct 19 10:42 newsudofile.txt

33) Cambia los permisos para que sólo el usuario pueda leer y escribir

chmod 600 newsudofile.txt

34) ¿Permitido?

si
-rw------- 1 sofia root     0 oct 19 10:42 newsudofile.txt


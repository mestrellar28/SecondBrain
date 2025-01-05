  Hero Banner

	Tamano alto con carousel si hay mas de una imagen

Tarjetas Destacadas

	 

Cajas Destacadas

	

Header

	Si existe el hero banner sale transparente estando al top 0, y al hacer scroll paso a blanco
	Si no existe el hero banner sale blanco
	Cuando abro el menu en mobile va a ser blanco
	Mismo comportamiento que desktop
	Siempre sticky

Formulario de Review

	Estrellas en una sola linea y mas pequenas

Modulo de Productos

	Quitar los arrows
	Slider con el dedo y con el mouse
	Imagen mas pequena

Banner con Icono

	En mobile icono a la izquierda

Lista de Puntos

	Formato tabla en desktop y mobile


----
### Form Agente Registro

Form Agencia

	Mostrar mensaje de error cuando el servicio devuelva KO en el primer paso.

	Cambiar titulo del codigo IATA por Loyalty ID dependiendo del form agency.

	Si continuo "sin acreditacion" el Codigo IATA o Loaylty ID Input desaparece

	No enviar el Codigo IATA o Loyalty ID del form agency (es solo informativo y sale bloqueado)

	Codigo TBD cambia por "Pagina Web"

	En estos dos tanto agente como agencia, lo que venga precargado bloqueado y lo que no es editable, la unica cosa "especial" es el campo codigo IATA o el que sea que va a arriba unicamente a modo informativo y no se manda en el form, y si el user pasa a los datos de agencia sin precargar no sale
### Perfil

### Formulario datos de Agencia

	Mover el campo tipo a datos personales

	Quitar boton "Solicitar traslado de agencia".

	Los formularios tienes 2 estados vista (bloqueado) edicion (habilitado)

	Cada form va a tener su editar.

	 Los datos del formulario de agencia son los mismos de registro de agente, mas el Codigo IATA y Loyalty ID.

Corner Case 1

	Algunos de esos campos son no sensibles (puedo editarlos).

	Datos sensibles (no pueden modificarse).

Corner Case 2

	Si intento modificar el NIF (en el momento que lo toco se borran todos los datos del formulario).

	Codigo IATA y Loyalty ID no son obligatorios.
	No permitir cambio de code iata ni loyalty id

Corner Case 3 

	Si intento introducir Codigo IATA o Loyalty ID se bloquean los demas campos.

	Al hacer submit se envian los datos si esta OK reemplazar los datos del form y quitar modo edicion.

### Formulario datos personales

----
Form Agent los datos vienen desde el pre registro.
Form Agency los datos vienen del primer paso.
Los datos que vienen se quedan bloqueados.
Contrasena no existe y repetir contrasena tampoco.

---
	3 HTML (Login, Reset Contrasena, Set Contrasena)

---
### Primer Item
Modal con el total de puntos y un input para ingresar cantidad a cambiar
Boton "Pasar mis puntos a Rewards"

### Segundo Item
Modal con el total de puntos y un input para ingresar cantidad a cambiar
Boton "Solicitar tarjeta"

---
### Listado de puntos

	Paginacion en Desktop y si es posible en mobile
	Tabla con filtrado
	Si es tipo reserva tiene 6 campos 
	Si es puntos solo 3
	Si es caducidad tiene 1 solo campo
	Hay uno que no tiene campo
	El que no tiene nada quitar la flecha de desplegable
	En mobile no hay scroll horizontal
	Solo mostrar en mobile Fecha de reserva y tipo de  movimiento 

### Formulario Reserva Manual

	Los puntos rewards saber de donde sacar el valor
	Devolver simulacion de puntos si es satisfactoria la respuesta


```
ewogICJhZ2VuY3kiOiB7CiAgICAiYnVzaW5lc3NEYXRhIjogewogICAgICAid2ViUGFnZSI6ICJodHRwczovL2h1YWthaS5lcy8iLAogICAgICAic2hpcHBpbmdBZGRyZXNzIjogewogICAgICAgICJzdGF0ZSI6ICJNYWRyaWQiLAogICAgICAgICJwb3N0YWxDb2RlIjogIjI4MjM0IiwKICAgICAgICAiY291bnRyeSI6ICJFUyIsCiAgICAgICAgImNpdHkiOiAiTWFkcmlkIiwKICAgICAgICAiYWRkcmVzcyI6ICJDYWxsZSBWaWxsYSIKICAgICAgfSwKICAgICAgImlkSUFUQSI6ICJFMiIsCiAgICAgICJidXNpbmVzc05hbWUiOiAiSHVha2FpIiwKICAgICAgImFnZW5jeUxveWFsdHlJZCI6ICIyNDA0MTA0NTc4IgogICAgfSwKICAgICJmaXNjYWxEYXRhIjogewogICAgICAic3RhdHVzIjogIlByZSIsCiAgICAgICJzaGlwcGluZ0FkZHJlc3MiOiB7CiAgICAgICAgInN0YXRlIjogIk1hZHJpZCIsCiAgICAgICAgInBvc3RhbENvZGUiOiAiMjgyMzQiLAogICAgICAgICJjb3VudHJ5IjogIkVTIiwKICAgICAgICAiY2l0eSI6ICJNYWRyaWQiLAogICAgICAgICJhZGRyZXNzIjogIkNhbGxlIFZpbGxhIgogICAgICB9LAogICAgICAicHJlZml4IjogIiszNCIsCiAgICAgICJwaG9uZSI6ICI2NDk3NjUzODkiLAogICAgICAiZmlzY2FsTmFtZSI6ICJIdWFrYWkiLAogICAgICAiZW1haWwiOiBudWxsLAogICAgICAiY2lmIjogIkg4ODk3NiIKICAgIH0KICB9LAogICJhZ2VudCI6IHsKICAgICJ0cmFuc2ZlclBvaW50c1Jld2FyZHMiOiBmYWxzZSwKICAgICJzdGF0dXMiOiAiQWN0aXZlIiwKICAgICJzaGlwcGluZ0FkZHJlc3MiOiB7CiAgICAgICJzdGF0ZSI6ICJNYWRyaWQiLAogICAgICAicG9zdGFsQ29kZSI6IG51bGwsCiAgICAgICJjb3VudHJ5IjogIkVTIiwKICAgICAgImNpdHkiOiAiTWFkcmlkIiwKICAgICAgImFkZHJlc3MiOiAiQ2FsbGUgVmlsbGEiCiAgICB9LAogICAgInByZWZpeCI6ICIrMzQiLAogICAgInBvc2l0aW9uIjogIkFnZW50ZSIsCiAgICAicG9pbnRzIjogewogICAgICAidG90YWxQb2ludHNCYWxhbmNlVmFsdWUiOiAwLAogICAgICAidG90YWxQb2ludHNCYWxhbmNlIjogMCwKICAgICAgInRvdGFsUG9pbnRzQWNjdW11bGF0ZWRQaW50c1ZhbHVlIjogMCwKICAgICAgInRvdGFsUG9pbnRzQWNjdW11bGF0ZWQiOiAwLAogICAgICAicmV3YXJkc0NvbnZlcnRlZFBvaW50c1ZhbHVlIjogMCwKICAgICAgInJld2FyZHNDb252ZXJ0ZWRQb2ludHMiOiAwLAogICAgICAicGVuZGluZ1BvaW50c1ZhbHVlIjogMCwKICAgICAgInBlbmRpbmdQb2ludHMiOiAwLAogICAgICAibXVsdGlwbHlQb2ludHNCeSI6IDAKICAgIH0sCiAgICAicGVyc29uQmlydGhkYXRlIjogIjE5OTQtMDMtMjMiLAogICAgIm5ld3NsZXR0ZXJzIjogdHJ1ZSwKICAgICJtb2JpbGVQaG9uZSI6ICIyMzU0NDY2OTAiLAogICAgIm1lbWJlclJlZmVyYWxDb2RlIjogIiIsCiAgICAibGFzdE5hbWUiOiAiVG9ycmVzIiwKICAgICJsYW5ndWFnZSI6ICJlcyIsCiAgICAiaXNSZXNwb25zaWJsZUFnZW50IjogZmFsc2UsCiAgICAiaWRSZXdhcmRzIjogbnVsbCwKICAgICJnZW5kZXIiOiBudWxsLAogICAgImZsYWdBZ3JlZVJlZ2lzdGVyQjJDIjogdHJ1ZSwKICAgICJmaXJzdE5hbWUiOiAiTW9uaWNhIiwKICAgICJlbWFpbCI6ICJsb2dpbnRlc3QzQHlvcG1haWwuY29tIiwKICAgICJkb2N1bWVudFR5cGUiOiAiRE5JIiwKICAgICJkb2N1bWVudE51bWJlciI6ICIzNDU2NzgzMiIKICB9LAogICJob3RlbHMiOiBbCiAgICB7CiAgICAgICJuYW1lSG90ZWwiOiAiSG90ZWwgMiIKICAgIH0sCiAgICB7CiAgICAgICJuYW1lSG90ZWwiOiAiSG90ZWwgMiIKICAgIH0KICBdCn0=
```


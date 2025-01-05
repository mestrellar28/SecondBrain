- En una pagina debajo de inicio, ir a properties > advanced > login page : /bin/palladium-pro/login
- Guardar y publicar la pagina
- Abrir incognito tab ir a la pagina creada
- Logarse con las credenciales

```
logintest3@yopmail.com
```

```
admin123#
```

- Llamar al servlet del login
- Desde el header hacer llamada al servlet del login para recuperar el loyaltyId y accessToken y llamar al agency agent para recuperar los datos del agente y guardarlos
- /headerlogin servlet

```
/bin/palladium-pro/headerlogin
```

adobe granite 

----

Boton de Registrate = Pre registro
Boton de Iniciar sesion = enviar a home privada

----

userInfo

```
ewogICJhZ2VuY3kiOiB7CiAgICAiYnVzaW5lc3NEYXRhIjogewogICAgICAid2ViUGFnZSI6ICJodHRwczovL2h1YWthaS5lcy8iLAogICAgICAic2hpcHBpbmdBZGRyZXNzIjogewogICAgICAgICJzdGF0ZSI6ICJNYWRyaWQiLAogICAgICAgICJwb3N0YWxDb2RlIjogIjI4MjM0IiwKICAgICAgICAiY291bnRyeSI6ICJFUyIsCiAgICAgICAgImNpdHkiOiAiTWFkcmlkIiwKICAgICAgICAiYWRkcmVzcyI6ICJDYWxsZSBWaWxsYSIKICAgICAgfSwKICAgICAgImlkSUFUQSI6ICJFMiIsCiAgICAgICJidXNpbmVzc05hbWUiOiAiSHVha2FpIiwKICAgICAgImFnZW5jeUxveWFsdHlJZCI6ICIyNDA0MTA0NTc4IgogICAgfSwKICAgICJmaXNjYWxEYXRhIjogewogICAgICAic3RhdHVzIjogIlByZSIsCiAgICAgICJzaGlwcGluZ0FkZHJlc3MiOiB7CiAgICAgICAgInN0YXRlIjogIk1hZHJpZCIsCiAgICAgICAgInBvc3RhbENvZGUiOiAiMjgyMzQiLAogICAgICAgICJjb3VudHJ5IjogIkVTIiwKICAgICAgICAiY2l0eSI6ICJNYWRyaWQiLAogICAgICAgICJhZGRyZXNzIjogIkNhbGxlIFZpbGxhIgogICAgICB9LAogICAgICAicHJlZml4IjogIiszNCIsCiAgICAgICJwaG9uZSI6ICI2NDk3NjUzODkiLAogICAgICAiZmlzY2FsTmFtZSI6ICJIdWFrYWkiLAogICAgICAiZW1haWwiOiBudWxsLAogICAgICAiY2lmIjogIkg4ODk3NiIKICAgIH0KICB9LAogICJhZ2VudCI6IHsKICAgICJ0cmFuc2ZlclBvaW50c1Jld2FyZHMiOiBmYWxzZSwKICAgICJzdGF0dXMiOiAiQWN0aXZlIiwKICAgICJzaGlwcGluZ0FkZHJlc3MiOiB7CiAgICAgICJzdGF0ZSI6ICJNYWRyaWQiLAogICAgICAicG9zdGFsQ29kZSI6IG51bGwsCiAgICAgICJjb3VudHJ5IjogIkVTIiwKICAgICAgImNpdHkiOiAiTWFkcmlkIiwKICAgICAgImFkZHJlc3MiOiAiQ2FsbGUgVmlsbGEiCiAgICB9LAogICAgInByZWZpeCI6ICIrMzQiLAogICAgInBvc2l0aW9uIjogIkFnZW50ZSIsCiAgICAicG9pbnRzIjogewogICAgICAidG90YWxQb2ludHNCYWxhbmNlVmFsdWUiOiAwLAogICAgICAidG90YWxQb2ludHNCYWxhbmNlIjogMCwKICAgICAgInRvdGFsUG9pbnRzQWNjdW11bGF0ZWRQaW50c1ZhbHVlIjogMCwKICAgICAgInRvdGFsUG9pbnRzQWNjdW11bGF0ZWQiOiAwLAogICAgICAicmV3YXJkc0NvbnZlcnRlZFBvaW50c1ZhbHVlIjogMCwKICAgICAgInJld2FyZHNDb252ZXJ0ZWRQb2ludHMiOiAwLAogICAgICAicGVuZGluZ1BvaW50c1ZhbHVlIjogMCwKICAgICAgInBlbmRpbmdQb2ludHMiOiAwLAogICAgICAibXVsdGlwbHlQb2ludHNCeSI6IDAKICAgIH0sCiAgICAicGVyc29uQmlydGhkYXRlIjogIjE5OTQtMDMtMjMiLAogICAgIm5ld3NsZXR0ZXJzIjogdHJ1ZSwKICAgICJtb2JpbGVQaG9uZSI6ICIyMzU0NDY2OTAiLAogICAgIm1lbWJlclJlZmVyYWxDb2RlIjogIiIsCiAgICAibGFzdE5hbWUiOiAiVG9ycmVzIiwKICAgICJsYW5ndWFnZSI6ICJlcyIsCiAgICAiaXNSZXNwb25zaWJsZUFnZW50IjogZmFsc2UsCiAgICAiaWRSZXdhcmRzIjogbnVsbCwKICAgICJnZW5kZXIiOiBudWxsLAogICAgImZsYWdBZ3JlZVJlZ2lzdGVyQjJDIjogdHJ1ZSwKICAgICJmaXJzdE5hbWUiOiAiTW9uaWNhIiwKICAgICJlbWFpbCI6ICJsb2dpbnRlc3QzQHlvcG1haWwuY29tIiwKICAgICJkb2N1bWVudFR5cGUiOiAiRE5JIiwKICAgICJkb2N1bWVudE51bWJlciI6ICIzNDU2NzgzMiIKICB9LAogICJob3RlbHMiOiBbCiAgICB7CiAgICAgICJuYW1lSG90ZWwiOiAiSG90ZWwgMiIKICAgIH0sCiAgICB7CiAgICAgICJuYW1lSG90ZWwiOiAiSG90ZWwgMiIKICAgIH0KICBdCn0=
```


{
  "error": {
    "errorCode": 409,
    "errorDateTime": "2024-04-24T15:31:00.354Z",
    "errorMessage": "MobilePhone already in the system",
    "errorDescription": "MobilePhone already in the system"
  }
}

https://author-palladiumhotelgroup-dev.adobemsbasic.com

{
    "email": "mestrellar28@gmail.com",
    "subject": "Cambio de datos personales",
    "origin": "North America",
    "description": "aspdkpaodkpoasdads"
}


/content/experience-fragments/palladium-pro/es
/content/dam/palladium-pro
/content/palladium-pro

### Reset Password

```
https://palladiumprodev.b2clogin.com/palladiumprodev.onmicrosoft.com/oauth2/v2.0/authorize?p=B2C_1A_PASSWORDRESET_PALLADIUMPRO&client_id=0d4affdd-3ba7-4f06-aa00-f71f275af766&nonce=defaultNonce&redirect_uri=https%3A%2F%2Fbalancer.palladiumhotelgroup-dev.com%2Fcallback%2Fj_security_check&scope=openid&response_type=id_token&prompt=login
```

----

```
testaltapro08@yopmail.com
```

```
MRproper2
```
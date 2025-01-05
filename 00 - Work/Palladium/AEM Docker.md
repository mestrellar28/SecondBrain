#### Login Azure

```
az login
```

#### Get username and password

```
az acr login --name seidorcxcontainerregistry.azurecr.io --expose-token
```

#### Login in docker

```
cat ~/docker_password.txt | sudo docker login --username 00000000-0000-0000-0000-000000000000 --password-stdin seidorcxcontainerregistry.azurecr.io
```

	username

```
00000000-0000-0000-0000-000000000000
```

	password

```
eyJhbGciOiJSUzI1NiIsInR5cCI6IkpXVCIsImtpZCI6IlFSMlc6U0pXWTpTWUZXOkg3M1I6TkhPMzo2SktOOkU1SDM6WEpYNzpISlRCOlFZQkk6NU1aWjpQT1ZaIn0.eyJqdGkiOiIwMjNiMjYxNi1mNDE0LTQyZDEtYjllNy01NTYzNjZhODc2MDEiLCJzdWIiOiJtZXN0cmVsbGFAc2VpZG9yLmVzIiwibmJmIjoxNzEyMzE3NzkwLCJleHAiOjE3MTIzMjk0OTAsImlhdCI6MTcxMjMxNzc5MCwiaXNzIjoiQXp1cmUgQ29udGFpbmVyIFJlZ2lzdHJ5IiwiYXVkIjoic2VpZG9yY3hjb250YWluZXJyZWdpc3RyeS5henVyZWNyLmlvIiwidmVyc2lvbiI6IjEuMCIsInJpZCI6ImI4ZjNiN2E4MDI2NzQwODA5MTg3ODBlN2EyMzNmODY2IiwiZ3JhbnRfdHlwZSI6InJlZnJlc2hfdG9rZW4iLCJhcHBpZCI6IjA0YjA3Nzk1LThkZGItNDYxYS1iYmVlLTAyZjllMWJmN2I0NiIsInRlbmFudCI6IjY1NDYyM2Q2LTE1MDQtNGYyMi1hMTQ2LWI3YzcyNjM3NzY2YSIsInBlcm1pc3Npb25zIjp7ImFjdGlvbnMiOlsicmVhZCIsIndyaXRlIl19LCJyb2xlcyI6W119.EWnjY4Nw1qpFuEdca98scxv8fxomlN5piVqpMLqZ95aJ_z44v7k2yrUQyps3NPiwV7DISozVpxPfJc272C7mSoR8F_Owtbvh9-fORijuwnoPRfzFMibVVNfU0Tu1nsQ03ERB7nFlBCTWmNa0DoB_kB-GMJLng73zz91CisP3MEOEXPdOuYe7KP88DQMrhmdi_EXzow6lW8ZdfhAB1iJytcGU4d8Rjb3SkvyjwE07DbuXEBpLNN59MlDZT1SpM17ujziFygc0CmFgevg95pUFfYNk2Dw_EYiSTGIxOcN9YD-BKpG4Ds6b4qT3lFqRvsLDlpxpIE7xKZ1jAC7aRl7vgw
```

### Run environments

```json
docker-compose -f seidor-stack.yml up -d
```


```
**sqp_6ef32541bc242e3d2653ca1c0a66d81a078aa5b6**
```

```
mvn clean verify sonar:sonar \
  -Dsonar.projectKey=PalladiumCloud \
  -Dsonar.host.url=http://localhost:9000 \
  -Dsonar.login=sqp_6ef32541bc242e3d2653ca1c0a66d81a078aa5b6
```
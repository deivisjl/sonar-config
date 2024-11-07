
### Configuraciones para angular
```
npm install sonar-scanner --save-dev


sonar-scanner.properties
/***/
sonar.host.url=http://192.168.71.140:9000
sonar.login=admin
sonar.password=admin
sonar.projectKey=demo-app
sonar.projectName=demo-app
sonar.projectVersion=1.0
sonar.sourceEncoding=UTF-8
sonar.sources=src
sonar.exclusions=**/node_modules/**
sonar.tests=src
sonar.test.inclusions=**/*.spec.ts
sonar.typescript.lcov.reportPaths=coverage/lcov.info

"scripts": {
    "sonar": "sonar-scanner"
}

npm run sonar
```

### Configuraciones .NET CORE
```
dotnet tool install --global dotnet-sonarscanner
dotnet sonarscanner begin /k:"backend" /d:sonar.host.url="http://192.168.131.130:9000" /d:sonar.login="77e622c9f98cd5520da0344af1abef4ebb9b4fc8"
dotnet build API.sln
dotnet sonarscanner end /d:sonar.login="77e622c9f98cd5520da0344af1abef4ebb9b4fc8"
```
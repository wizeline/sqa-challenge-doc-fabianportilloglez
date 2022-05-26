### **Front End con Cypress:**
**Variables de ambiente** — Guardar en(.env y cypress.json) los valores usados a lo largo del SQA. También se puede tener un folder de config y centro varios files dependiendo el ambiente o un archivo cypress.env.json donde se definan las cosas

**Utilizar POM y BDD** - hacer que la estrategia sea escalable y las funciones definidas o los elenentos sean reutilizables

**Definir un ESLint** — en el proyecto con reglas y estructura
Crear scripts --- En el package.json definir algunos scripts para poder correr los tests también en --headless CLI
Eliminar los tests y data después de correrse - Definir los before() and after() en cada archivo de .js para que los tests se mantengan independientes y sin data que estorbe

**Selección de elementos** --- Encontrar la estrategia de mejor selección de elementos y comprobar si es mejor guardarlos por archivo de Page o tener algunas definciiones en archivos independientes y llamarlos desde ahí

**Comandos comunes y reutilizables** --- Es conveniente definir algunos comandos en commands.js o crear un file de commonSteps donde se definan aquellos que se pueden reutilizar?

**Ocultar contraseña** - Hacer que los datos sensibles no sean visibles al correr el Test runner con log: false
Screenshots: Hacer eficiente la forma en que se almacenan y también borrarlos una vez que el test termina

**Assertions** --- Chai assertions de expect y should en los tests

**Reportes** --- Lograr que se creen reportes cuando finalice el test y que se guarden en un folder

**Slack notification**
Jenkins, asignar que los tests corran por consola usando jenkins pipeline y definiendo todo en un Jenkinsfile

**Sonarqube** --- Configurar sonarqube e integrarlo con el repo de github y además en un stage del Jenkinsfile para checar las validaciones
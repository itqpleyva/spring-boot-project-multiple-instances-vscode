# spring-boot-project-multiple-instances-vscode

<h2> Multiple instances from a spring boot project in VSCODE</h2>

<p>To create multiple instances from a SpringBoot project in VSCODE just add e new configuration to the <strong>launch.json</strong> file in the .vscode folder</p>

          {
              "configurations": [
                  {
                      "type": "java",
                      "name": "Spring Boot-DemoApplication<demo> (8002)",// microservice to run in port 8002
                      "request": "launch",
                      "mainClass": "com.example.demo.DemoApplication",
                      "projectName": "demo",
                      "vmArgs": "-Dserver.port=8002"// defining the port
                  },
                  {
                      "type": "java",
                      "name": "Spring Boot-DemoApplication<demo> (8001)",// microservice to run in port 8001
                      "request": "launch",
                      "mainClass": "com.example.demo.DemoApplication",
                      "projectName": "demo",
                      "vmArgs": "-Dserver.port=8001"//definig the port
                  }
              ]
          }
          
          
<p>Then go to debug and run the two instances</p>

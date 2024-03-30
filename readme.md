## OpenAPI not generating, Swagger UI not building

http://localhost:8080/docs/openapi.json
http://localhost:8080/q/swagger-ui

## Application properties
```
quarkus.swagger-ui.always-include=true
quarkus.swagger-ui.enable=true
```

### Run commands
```
mvn clean package
java -jar target/quarkus-app/quarkus-run.jar
```

### Output
```
dk@MacBook-Pro backend % mvn clean package 
[INFO] Scanning for projects...
[INFO] 
[INFO] --------------------< io.dvkdo.kogito:test-process >--------------------
[INFO] Building Test Process 1.0.0-SNAPSHOT
[INFO]   from pom.xml
[INFO] --------------------------------[ jar ]---------------------------------
[INFO] 
[INFO] --- clean:3.2.0:clean (default-clean) @ test-process ---
[INFO] Deleting /Users//dekaido/kogito-processes/backend/target
[INFO] 
[INFO] --- resources:3.3.1:resources (default-resources) @ test-process ---
[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] Copying 10 resources from src/main/resources to target/classes
[INFO] 
[INFO] --- compiler:3.11.0:compile (default-compile) @ test-process ---
[INFO] No sources to compile
[INFO] 
[INFO] --- resources:3.3.1:testResources (default-testResources) @ test-process ---
[WARNING] Using platform encoding (UTF-8 actually) to copy filtered resources, i.e. build is platform dependent!
[INFO] skip non existing resourceDirectory /Users//dekaido/kogito-processes/backend/src/test/resources
[INFO] 
[INFO] --- compiler:3.11.0:testCompile (default-testCompile) @ test-process ---
[INFO] No sources to compile
[INFO] 
[INFO] --- surefire:3.2.2:test (default-test) @ test-process ---
[INFO] No tests to run.
[INFO] 
[INFO] --- jar:3.3.0:jar (default-jar) @ test-process ---
[INFO] Building jar: /Users//dekaido/kogito-processes/backend/target/test-process.jar
[INFO] 
[INFO] --- quarkus:2.16.10.Final:build (default) @ test-process ---
[INFO] [io.quarkus.deployment.QuarkusAugmentor] Quarkus augmentation completed in 686ms
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time:  2.268 s
[INFO] Finished at: 2024-03-29T20:52:33-04:00
[INFO] ------------------------------------------------------------------------
dk@MacBook-Pro backend % java -jar target/quarkus-app/quarkus-run.jar 
__  ____  __  _____   ___  __ ____  ______ 
 --/ __ \/ / / / _ | / _ \/ //_/ / / / __/ 
 -/ /_/ / /_/ / __ |/ , _/ ,< / /_/ /\ \   
--\___\_\____/_/ |_/_/|_/_/|_|\____/___/   
2024-03-29 20:52:46,391 INFO  [io.qua.sma.ope.run.OpenApiRecorder] (main) CORS filtering is disabled and cross-origin resource sharing is allowed without restriction, which is not recommended in production. Please configure the CORS filter through 'quarkus.http.cors.*' properties. For more information, see Quarkus HTTP CORS documentation
2024-03-29 20:52:46,468 INFO  [io.quarkus] (main) test-process 1.0.0-SNAPSHOT on JVM (powered by Quarkus 2.16.10.Final) started in 0.430s. Listening on: http://0.0.0.0:8080
2024-03-29 20:52:46,470 INFO  [io.quarkus] (main) Profile prod activated. 
2024-03-29 20:52:46,470 INFO  [io.quarkus] (main) Installed features: [cdi, resteasy-jackson, smallrye-context-propagation, smallrye-health, smallrye-openapi, vertx]

```

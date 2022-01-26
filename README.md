# wire-maven-plugin
Maven plugin for [wiring](https://square.github.io/wire/) in GPB files into your Java project.
It will run by default in the `generate-sources` lifecycle phase.

Usage example:
```xml
    <build>
        <plugins>
            <plugin>
                <groupId>uk.co.crunch</groupId>
                <artifactId>wire-maven-plugin</artifactId>
                <executions>
                    <execution>
                        <configuration>
                            <protoPaths>/path/to/some-shared-message-schemas</protoPaths>
                            <protoFiles>
                                <param>uk/co/crunch/domain/some_service_request.proto</param>
                                <param>uk/co/crunch/domain/some_service_response.proto</param>
                            </protoFiles>
                        </configuration>
                    </execution>
                </executions>
            </plugin>
        </plugins>
    </build>
```
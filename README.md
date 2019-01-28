## Install [![Maven Central](https://img.shields.io/maven-central/v/com.qoomon/maven-enforcer-rules.svg)](http://search.maven.org/#search%7Cga%7C1%7Cg%3A%22com.qoomon%22%20AND%20a%3A%22maven-enforcer-rules%22)
[![Build Status](https://travis-ci.com/qoomon/maven-enforcer-rules.svg?branch=master)](https://travis-ci.com/qoomon/maven-enforcer-rules)
            
```xml
...
<build>
    <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-enforcer-plugin</artifactId>
            <version>LATEST</version>
            <dependencies>
                <dependency>
                    <groupId>com.qoomon</groupId>
                    <artifactId>maven-enforcer-rules</artifactId>
                    <version>LATEST</version>
                </dependency>
            </dependencies>
            <executions>
                <execution>
                    <id>release-rules</id>
                    <goals>
                        <goal>enforce</goal>
                    </goals>
                    <configuration>
                        <rules>
                            <requireReleaseVersion/>
                            <requireReleaseDeps/>
                            <requireSemverFormat implementation="com.qoomon.maven.enforcer.rules.SemverFormatEnforcerRule">
                        </rules>
                    </configuration>
                </execution>
            </executions>
        </plugin>
    </plugins>
</build>
...
```
### Implementations
* semver format
  * com.qoomon.maven.enforcer.rules.SemverFormatEnforcerRule

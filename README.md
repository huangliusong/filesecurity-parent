# filesecurity-parent
filesecurity-parent

[![Maven central](https://img.shields.io/badge/Maven%20central-v1.1-red.svg)](https://oss.sonatype.org/#nexus-search;quick~filesecurity-parent)
[![top](https://img.shields.io/badge/build-top.huangliusong2019-green.svg)](https://github.com/huangliusong/filesecurity-parent)
[![Sonatype Nexus (Snapshots)](https://img.shields.io/badge/Sonatype%20Nexus-v1.1-blue.svg)](https://oss.sonatype.org/content/repositories/snapshots/top/huangliusong2019/)
[![build](https://img.shields.io/badge/build-passing-brightgreen.svg)](https://travis-ci.org/huangliusong/filesecurity-parent)


## Dependency

### [filesecurity-spring-boot-starter](https://github.com/huangliusong/filesecurity-spring-boot-starter)

### [filesecurity-parent](https://github.com/huangliusong/filesecurity-parent)

### [filesecurity-spring-boot](https://github.com/huangliusong/filesecurityspringboot)


## Requirements

* Java 8+ and 
* Spring Boot 1.5.7+
* Maven 3.3.9+


## Quick Start

~~~
<dependency>
  <groupId>top.huangliusong2019</groupId>
  <artifactId>filesecurity-parent</artifactId>
  <version>1.1.4-SNAPSHOT</version>
</dependency>
~~~


## push
> mvn clean package deploy

## Build
~~~
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 29.995 s
[INFO] Finished at: 2019-07-26T23:13:11+08:00
[INFO] Final Memory: 16M/210M
[INFO] ------------------------------------------------------------------------
~~~

## Build config
~~~
<build>
        <plugins>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-source-plugin</artifactId>
                <version>3.0.1</version>
                <!-- Bind the source plug-in to Maven's life cycle and perform the goal of the bound source after the life cycle -->
                <executions>
                    <execution>
                        <!-- Bind the source plug-in to Maven lifecycle -->
                        <phase>compile</phase>
                        <!--Execute goals for the bound source plug-in after the lifecycle -->
                        <goals>
                            <goal>jar-no-fork</goal>
                        </goals>
                    </execution>
                </executions>
            </plugin>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-surefire-plugin</artifactId>
                <configuration>
                    <skip>false</skip>
                </configuration>
            </plugin>
            <plugin>
                <groupId>org.apache.maven.plugins</groupId>
                <artifactId>maven-compiler-plugin</artifactId>
                <version>3.5.1</version>
                <configuration>
                    <source>1.8</source>
                    <target>1.8</target>
                </configuration>
            </plugin>

        </plugins>
    </build>
~~~
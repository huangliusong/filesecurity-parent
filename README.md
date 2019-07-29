# filesecurity-parent
filesecurity-parent

[![Maven central](https://img.shields.io/badge/Maven%20central-v1.1-red.svg)](https://search.maven.org/)
[![top](https://img.shields.io/badge/build-top.huangliusong2019-green.svg)]()
[![Sonatype Nexus (Snapshots)](https://img.shields.io/badge/Sonatype%20Nexus-v1.1-blue.svg)](https://oss.sonatype.org/content/repositories/snapshots/top/huangliusong2019/)
[![build](https://img.shields.io/badge/build-passing-brightgreen.svg)](https://github.com/huangliusong1994/filesecurityspringboot)


## spring-starter
[filesecurity-spring-boot](https://github.com/huangliusong1994/filesecurityspringboot)

## Requirements

* Java 8+ and 
* Spring Boot 1.5.7+
* Maven 3.3.9+


## Quick Start

~~~
<dependency>
  <groupId>top.huangliusong2019</groupId>
  <artifactId>filesecurity-parent</artifactId>
  <version>1.1.2-SNAPSHOT</version>
  <type>pom</type>
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
                <!-- 绑定source插件到Maven的生命周期,并在生命周期后执行绑定的source的goal -->
                <executions>
                    <execution>
                        <!-- 绑定source插件到Maven的生命周期 -->
                        <phase>compile</phase>
                        <!--在生命周期后执行绑定的source插件的goals -->
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
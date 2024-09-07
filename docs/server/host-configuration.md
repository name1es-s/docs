---
sidebar_position: 1
---

# Конфигурация сервера

## Конфигурация выделенного сервера:
- **CPU:** Intel® Core™ i5-13500
- **RAM:** 64 GB DDR4
- **SSD:** 2 x 512 TB NVMe
- **Сеть:** 1 Gbit/s
- **ОС:** Ubuntu 22.04.3 LTS
- **Местоположение:** Германия

## Ядро сервера:
Сервер запущен на ядре [SparklyPaper](https://github.com/SparklyPower/SparklyPaper).

## Параметры запуска Java:
Сервер запущен на [GraalVM](https://www.graalvm.org/) 21 JDK 
```
java -Xms12288M -Xmx12288M -Dfile.encoding=UTF8 -XX:ConcGCThreads=3 -XX:MaxRAMPercentage=95.0 -XX:+EagerJVMCI
-XX:+UnlockExperimentalVMOptions -XX:+UnlockDiagnosticVMOptions -XX:+AlwaysActAsServerClassMachine -XX:+UseNUMA
-XX:+DisableExplicitGC -XX:AllocatePrefetchStyle=3 -XX:NmethodSweepActivity=1 -XX:ReservedCodeCacheSize=400M
-XX:NonNMethodCodeHeapSize=12M -XX:ProfiledCodeHeapSize=194M -XX:NonProfiledCodeHeapSize=194M
-XX:-DontCompileHugeMethods -XX:+PerfDisableSharedMem -XX:+AlwaysPreTouch -XX:+UseFastUnorderedTimeStamps
-XX:+UseCriticalJavaThreadPriority --add-modules=jdk.incubator.vector -jar server.jar
```
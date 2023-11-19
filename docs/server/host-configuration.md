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
Сервер выживания запущен на тестовом ядре [Folia](https://papermc.io/software/folia) от разработчиков [Paper](https://papermc.io/).

## Параметры запуска Java:
Сервер запущен на [GraalVM](https://www.graalvm.org/) 17 EE 
```
java -Xms32768M -Xmx32768M -Dfile.encoding=UTF8 -XX:ConcGCThreads=3 -XX:MaxRAMPercentage=95.0 --add-modules=jdk.incubator.vector 
-XX:+UnlockExperimentalVMOptions -XX:+UnlockDiagnosticVMOptions -XX:+AlwaysActAsServerClassMachine -XX:+AlwaysPreTouch 
-XX:+DisableExplicitGC -XX:+UseNUMA -XX:AllocatePrefetchStyle=3 -XX:NmethodSweepActivity=1 -XX:ReservedCodeCacheSize=400M 
-XX:NonNMethodCodeHeapSize=12M -XX:ProfiledCodeHeapSize=194M -XX:NonProfiledCodeHeapSize=194M -XX:-DontCompileHugeMethods 
-XX:+PerfDisableSharedMem -XX:+UseFastUnorderedTimeStamps -XX:+UseCriticalJavaThreadPriority -XX:+EagerJVMCI 
-Dgraal.TuneInlinerExploration=1 -Dgraal.CompilerConfiguration=enterprise -jar server.jar
```
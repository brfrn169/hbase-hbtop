# hbase-hbtop for hbase1

`hbtop` is an official real-time monitoring tool like Unix’s top command in HBase. 
However, some CDH/HDP versions or other older versions don't have this tool. 
This project can build hbtop jars for those versions.

## How to build
1. Change the HBase version to your HBase version in pom.xml:
```
        <hbase.version>{Yor HBase version}</hbase.version>
``` 

2. Build the hbtop jar:
```
mvn clean package
```

3. You can get the hbtop jar under the `target` directory:
```
./target/hbase-hbtop-hbase1.jar
```

## Usage
You can run hbtop as follows:
```
CLASSPATH=/etc/hbase/conf:/etc/hadoop/conf:hbase-hbtop-hbase1.jar ${JAVA_HOME}/bin/java org.apache.hadoop.hbase.hbtop.HBTop
```

## See also:
- https://blogs.apache.org/hbase/entry/introduction-hbtop-a-real-time
- https://hbase.apache.org/book.html#hbtop

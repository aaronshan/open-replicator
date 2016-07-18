open-replicator
===============

Open Replicator is a high performance MySQL binlog parser written in Java. It unfolds the possibilities that you can parse, filter and broadcast the binlog events in a real time manner.

### release

current release version `1.4.3`

see [release logs](https://github.com/aaronshan/open-replicator/master/CHANGES.md) for more detail.

### parsers

BinlogEventParser is plugable. All available implementations are registered by default, but you can register only the parsers you are interested in.

![Alt text](http://dl.iteye.com/upload/attachment/0070/3054/4274ab64-b6d2-380b-86b2-56afa0de523d.png)

### Use

#### 1. generate target jar file.

```
git clone https://github.com/aaronshan/open-replicator.git
cd open-replicator
mvn clean package -DskipTests
```

#### 2. install jar file to local maven repository.

```
mvn install:install-file -Dfile=./target/open-replicator-1.4.3.jar -DgroupId=com.zendesk -DartifactId=open-replicator -Dversion=1.4.2 -Dpackaging=jar
```

#### 3. add dependency to your project.

```
<dependency>
        <groupId>com.zendesk</groupId>
        <artifactId>open-replicator</artifactId>
        <version>${version}</version>
</dependency>
```

#### 4. usage

```
final OpenReplicator or = new OpenReplicator();
or.setUser("root");
or.setPassword("123456");
or.setHost("localhost");
or.setPort(3306);
or.setServerId(6789);
or.setBinlogPosition(4);
or.setBinlogFileName("mysql_bin.000001");
or.setBinlogEventListener(new BinlogEventListener() {
    public void onEvents(BinlogEventV4 event) {
        // your code goes here
    }
});
or.start();

System.out.println("press 'q' to stop");
final BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
for(String line = br.readLine(); line != null; line = br.readLine()) {
    if(line.equals("q")) {
        or.stop();
        break;
    }
}
```

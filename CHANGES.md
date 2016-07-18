### release logs
=================

*2016-03-01* `1.4.2`

* Implment server-sent heartbeats and an API to check up on them.

*2016-01-29* `1.4.1`

* pickup a couple of upstream fixes -- Gtid event parsing and something around closing the stream

*2016-01-06* `1.4.0`

* support GIS extensions via vividsolution's 'jts' library

*2015-12-14* `1.3.6`

* bug-fix: Fix issue with binlog_row_image = MINIMAL parsing overruns

*2015-11-04* `1.3.5`

* bug-fix: don't emit format description events unless asked for in file replication
* bug-fix: support checksums even if the consumer didn't ask for format description events

*2015-11-03* `1.3.4`

* bug-fix: support mysql 5.6 file-based replication when the offset is greater than 4

*2015-10-30* `1.3.3`

* support 5.6 checksums in file-based replication

*2015-10-07* `1.3.2`

* bugfix for a big-endian issue that was corrupting BIT() columns longer than 2 bytes

*2015-09-28* `1.3.1`

* provide a helpful error message when an old authentication scheme is detected

*2015-09-09* `1.3.0`

* support mysql 5.6 and binlog_checksums

*2015-06-16* `1.2.1`

* notify io reader thread on exception from buffered stream reader, so it doesn't wait infinitely

*2015-03-08* `1.2.0`

* preserve invalid datetime values (0000-00-00, anyone?) as longs inside the datetime


*2015-02-20* `1.1.2`

* expose binlog filename in event stream
* rescue EOFException around doParse(); it's normal when the stream is closed

*2014-05-12* `1.0.7`

* support signed tinyint, smallint, mediumint, int, bigint

*2014-05-08* `1.0.6`

* remove dependency commons-lang, log4j
* support MYSQL_TYPE_TIMESTAMP2, MYSQL_TYPE_DATETIME2, MYSQL_TYPE_TIME2

*2011-12-29* `1.0.0`

* release 1.0.0
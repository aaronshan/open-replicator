### releases
1.4.2

    release: 2016-03-01
    Implment server-sent heartbeats and an API to check up on them.

1.4.1

    release: 2016-01-29
    pickup a couple of upstream fixes -- Gtid event parsing and something around closing the stream

1.4.0

    release: 2016-01-06
    support GIS extensions via vividsolution's 'jts' library

1.3.6

    release: 2015-12-14
    bug-fix: Fix issue with binlog_row_image = MINIMAL parsing overruns

1.3.5

    release: 2015-11-04
    bug-fix: don't emit format description events unless asked for in file replication
    bug-fix: support checksums even if the consumer didn't ask for format description events

1.3.4

    release: 2015-11-03
    bug-fix: support mysql 5.6 file-based replication when the offset is greater than 4

1.3.3

    release: 2015-10-30
    support 5.6 checksums in file-based replication

1.3.2

    release: 2015-10-07
    bugfix for a big-endian issue that was corrupting BIT() columns longer than 2 bytes

1.3.1

    release: 2015-09-28
    provide a helpful error message when an old authentication scheme is detected

1.3.0

    released: 2015-09-09
    support mysql 5.6 and binlog_checksums

1.2.1

    released: 2015-06-16
    notify io reader thread on exception from buffered stream reader, so it doesn't wait infinitely

1.2.0

    released: 2015-03-08
    preserve invalid datetime values (0000-00-00, anyone?) as longs inside the datetime


1.1.2

    released: 2015-02-20
    expose binlog filename in event stream
    rescue EOFException around doParse(); it's normal when the stream is closed

1.0.7

    release date: 2014-05-12
    support signed tinyint, smallint, mediumint, int, bigint

1.0.6

    release date: 2014-05-08
    remove dependency commons-lang, log4j
    support MYSQL_TYPE_TIMESTAMP2, MYSQL_TYPE_DATETIME2, MYSQL_TYPE_TIME2

1.0.0

    release date: 2011-12-29
Third Party Libraries
=====================

This directory holds libraries that the Scalyr team has included from other projects.  Some of these 
libraries have been forked to allow for them to be linked into the Scalyr Agent 2, while some are just
straight copies so that our customers do not need to separately install these dependencies.  These libraries
are released under their respective licenses which are included in the directories.

Library details
================

The following libraries are included:

  * [tcollector](#tcollector)
  * [PyMySQL](#PyMySQL)
  * [uuid](#uuid)
  * [redis-py](#redis-py)
  * [Requests](#requests)
  * [PySNMP](#pysnmp)
  * [PyASN1](#pyasn1)
  * [PySMI](#pysmi)
  * [PLY](#ply)

## tcollector<a name="tcollector">

A project that enables adhoc metric collection by writing simple collectors, similar to ScalyrMonitors.
For additional details, please visit the
[tcollector project page](http://opentsdb.net/docs/build/html/user_guide/utilities/tcollector.html).

This library has been forked by the Scalyr team.  It is used by the `linux_system_metrics` Monitor Plugin.


## PyMySQL<a name="PyMySQL">

A pure Python implementation of a MySQL client library.  For additional details, please visit the
[PyMySQL project page](http://www.pymysql.org/).

The `mysql_monitor` depends on this library.
 
Currently, this library is just a straight copy, but we may wish to fork it in the future.  The original
library only supports Python 2.6 and higher, whereas the agent attempts to support Python 2.4 and higher.  If
there is enough customer demand to allow the `mysql_monitor` to run with Python 2.4 or 2.5, we may fork and
invest the time to make the necessary modifications.

## uuid<a name="uuid">

UUID object and generation functions compatible with Python 2.4.  The standard Python uuid module only supports
Python 2.5 and higher but was based on a package available from [pypi](https://pypi.python.org/pypi/uuid/).  
That package still supports earlier versions of Python and so this is just a straight copy from that package.

## redis-py<a name="redis-py">

A redis client for Python.  For additional details, please visit the [redis-py github repository](https://github.com/andymccurdy/redis-py).

The `redis_monitor` depends on this library.

Currently this library is just a straight copy, but we may wish to fork it in the future.  The original
library only supports Python 2.6 or higher.  If there is enough customer demand to allow the `redis_monitor`
to run with earlier versions of Python we may fork and invest the time to make the necessary modifications.

## Requests<a name="requests-py">

Improved HTTP request handling.  For additional details, please visit the [requests homepage](http://docs.python-requests.org/).

This is a straight copy from the main Requests git repository.  Currently this library is just a straight
copy, but we may wish to fork it in the future.  The original library only supports Python 2.6 or higher.
If there is enough customer demand to allow Requests to run with earlier versions of Python we may fork
and invest the time to make the necessary modifications.

## PySNMP<a name="pysnmp">

A pure Python SNMP library used by scalyr_agent.builtin_monitors.snmp_monitor

Currently this library is just a straight copy, and has support for Python 2.4 and later.

## PyASN1<a name="pyasn1">

A pure Python ASN.1 library.

Used by PySNMP.

## PySMI<a name="pysmi">

A pure Python library for parsing and conversion of SNMP/SMI MIBs.

Used by PySNMP

##PLY<a name="ply">

A pure Python implementation of lex and yacc.

Used by PySMI.

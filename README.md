# sqlblockedprocesses
SQL Server Blocked Process Report Viewer

*Purpose*

SQL Server's tracing tools generate blocked process reports to give more information about potential concurrency problems on a database server. But they are difficult to read. SQL Server Blocked Process Report Viewer organizes and presents this information in a useful way.

*Syntax*

`sp_blocked_process_report_viewer [@Source = ] 'SourceOfTraceOrSessionTarget' [ , [ @Type = ] 'BPRFormat' ]`

*Arguments*

`[@Source = ] 'SourceOfTraceOrSessionTarget'`

If the blocked process reports you'd like to examine came from a trace file, then this parameter specifies the name of the trace table or trace file that holds the blocked process reports. 

If the blocked process reports you'd like to examine are in an extended events session, then this parameter specifies the name of the session (not the session target).

If you are using extended events as a source, the target must either be a ring_buffer or an event_file.

`[@Trace = ] 'BPRFormat'`

Is the type of file referenced by SourceOfTraceOrSessionTarget. Values can be TABLE, FILE, XMLFILE or XESESSION. The default is FILE
 
Remember: When it comes to concurrency problems, _you don’t have to guess what’s wrong!!!_

Project Architecture
====================

The application includes two parts, first is host and another is plugin, which
communicates by standard input and output.

Application life cycle could be described as:

1. client starts a host application
2. _host_ application invokes _plugin_
3. after initialization _plugin_ sends to _host_ set to be searched in
4. _host_ takes input from client and searches in set by given keystroke
5. _host_ sends the search result to _plugin_
6. _plugin_ reformats the search results and sends it back to _host_
7. _host_ represent reformatted search results and allow client to chose one
8. client chose a result and _host_ sends final result for _plugin_
9. _host_ closes GUI and waits while _plugin_ completes action
10. _plugin_ does something with search result, then terminates

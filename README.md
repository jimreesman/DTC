# DTC
voter data tools

## VAN export format

VAN claims to support exports in .xls format. They are readable by Excel and Numbers (Mac). They are *not* readable by the Python library xlrd, and as a result are not readable by the csvkit utility in2csv. Specifically, they are a tab-delimited text file but with certain cell values represented as e.g. =(2031231234).

For the time being, we load files manually into Excel (or Numbers) and Save | Export as CSV. This of course will be untenable for any repetitive work, but while we're doing one-off tasks we can tolerate it.

VAN also supports .txt format exports. These files are tab-delimited text (almost). They are emitted with Windows-style line-endings (CRLF) *and* critically they contain occasional NUL characters.

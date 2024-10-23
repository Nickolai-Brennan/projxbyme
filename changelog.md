##Sample Guideline

2019-08-29  Noam Postavsky  <npostavs@gmail.com>

	Handle completely undecoded input in term (Bug#29918)

	* lisp/term.el (term-emulate-terminal): Avoid errors if the whole
	decoded string is eight-bit characters.  Don't attempt to save the
	string for next iteration in that case.
	* test/lisp/term-tests.el (term-decode-partial)
	(term-undecodable-input): New tests.

2019-06-15  Paul Eggert  <eggert@cs.ucla.edu>

	Port to platforms where tputs is in libtinfow

	* configure.ac (tputs_library): Also try tinfow, ncursesw (Bug#33977).

2019-02-08  Eli Zaretskii  <eliz@gnu.org>

	Improve documentation of 'date-to-time' and 'parse-time-string'

	* doc/lispref/os.texi (Time Parsing): Document
	'parse-time-string', and refer to it for the description of
	the argument of 'date-to-time'.

	* lisp/calendar/time-date.el (date-to-time): Refer in the doc
	string to 'parse-time-string' for more information about the
	format of the DATE argument.  (Bug#34303)

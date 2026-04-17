\# SQL Injection Detection



\## Find the possible vulnerable entry points

They can be found in:

* URL parameters
* Cookies / headers
* API requests
* Forms(login, search)



\## Do basic tests

Testing by injecting:

'

"

Look the response of the server (errors, page breaks, weird behavior)



\## Do boolean tests (Blind SQLI)

1. Boolean-based:

&#x20; 1 AND 1=1 -> true condition

&#x20; 1 AND 1=2 -> false condition

2\. Time-based:

&#x20; 1 AND SLEEP(10)

If response changes -> possible SQLI



\## Error-based 

Observe the server's response to see if it displays:

* SQL errors
* database names
* or other sensitive data



\### Confirmation SQL Injection (Conclusion)

SQLI likely confirmed if:

* behavior changes
* errors appear
* delay occurs


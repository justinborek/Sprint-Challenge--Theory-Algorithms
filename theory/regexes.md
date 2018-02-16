* Single regex that matches either of these:

    antelope rocks out
    antelopes rock out

** /antelopes*\srocks*\sout

* Regex that matches either of:

    goat
    moat

    but not:

    boat

**** /[^b]oat/

* Regex that matches dates in YYYY-MM-DD format. (Year can be 1-4 digits, and
    month and day can each be 1-2 digits). This does not need to verify the date
    is correct (e.g 33333-33-33 can match).

    2000-10-12
    1999-1-20
    1999-01-20
    812-2-10

**** /\d+-\d{1,2}-\d{1,2}/

* ESC[12;45f
* ESC[1m

* Come up with regexes for the two above sequences. The one to set the 
    cursor position should accept any digits for the row and column. The
    bold sequence need only accept `1` (and is a trivial regex). (ESC is
    a single character which can be represented with `\e` in the regex.)

**** /\e\[\d+\;\d+f/
**** /\e\[1m/
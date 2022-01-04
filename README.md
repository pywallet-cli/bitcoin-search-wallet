# Search bitcoins using Hexadecimal

It has three capabilities for searching.
-Search for bytes using hexidecimal
-Search for a plain text string
-Search for a smaller binary file

Syntax:
  search-cli -p A081853081820201P

EXAMPLES
  Search for the hex bytes "FF14DE" in the file gamefile.db:
  $ ./search-cli -p "FF14DE" gamefile.db
  Match at offset:            907          38B in  gamefile.db
  Match at offset:           1881          759 in  gamefile.db
  Match at offset:           7284         1C74 in  gamefile.db
  Match at offset:           7420         1CFC in  gamefile.db
  Match at offset:           8096         1FA0 in  gamefile.db


The printed offsets are listed in decimal and hexidecimal formats.
You can also search for unknown patterns with "??". Just insert them where ever you have an unknown byte:
  $ ./search-cli -p "A081853081820201P" wallet.dat


# Options of SearchBin:

  $ ./search-cli --help

  Optional Arguments:
    -h, --help            show help message and exit
    -f FILE, --file FILE  file to read search pattern from
    -t PATTERN, --text PATTERN
                          a (non-unicode case-sensitive) text string to search
                          for
    -p PATTERN, --pattern PATTERN
                          a hexidecimal pattern to search for
    -b NUM, --buffer-size NUM
                          read buffer size (in bytes). default is 8388608 (8MB)
    -s NUM, --start NUM   starting position in file to begin searching
    -e NUM, --end NUM     end search at this position, measuring from beginning
                          of file
    -m NUM, --max-count NUM
                          maximum number of matches to find
    -l FILE, --log FILE   write matched offsets to FILE, instead of standard
                          output
    -v, --verbose         verbose, output the number of bytes searched after
                          each buffer read
    -V, --version         print version information




# cyrillic2c_hex
This tool allows to use Cyrillic symbols in Unicode source files (like used in Keil) when target system expects Cyrillic to be encoded in CP1251.

## Usage
1. Add this line to your source code:

`//CYRILLIC STRING [UNIQUE_STRING_NAME]=[Привет, мир!\r\n]`

2. When you need this string, call it by name (UNIQUE_STRING_NAME in example above):

`uart0_printf(UNIQUE_STRING_NAME);`

3. Handle source files with the cyrillic2c_hex.py script before compiling:

`python cyrillic2c_hex.py source.c`

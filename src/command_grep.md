# grep command

### To search a file for a pattern
```bash
grep <pattern> <file>
```
### To perform a case-insensitive search (with line numbers)
```bash
grep -in <pattern> <file>
```
### To recursively grep for `string <pattern> in <dir>`
```bash
grep -R <pattern> <dir>
```
### Read search patterns from a file (one per line)
```bash
grep -f <pattern-file> <file>
```
### Find lines NOT containing pattern
```bash
grep -v <pattern> <file>
```
### To grep with regular expressions
```bash
grep "^00" <file>                                               # Match lines starting with 00
grep -E "[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}" <file> # Find IP add
```
### To find all files that match `<pattern> in <dir>`
```bash
grep -rnw <dir> -e <pattern>
```
### To exclude grep from your grepped output of ps
(`Add [] to the first letter. Ex: sshd -> [s]shd`)
```bash
ps aux | grep '[h]ttpd'
```
### Colour in red {bash} and keep all other lines
```bash
ps aux | grep -E --color 'bash|$'
```

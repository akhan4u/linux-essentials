# sed command

### To replace all occurrences of "day" with "night" and write to stdout
```bash
sed 's/day/night/g' <file>
```
### To replace all occurrences of "day" with "night" within <file>
```bash
sed -i 's/day/night/g' <file>
```
### To replace all occurrences of "day" with "night" on stdin
```bash
echo 'It is daytime' | sed 's/day/night/g'
```
### To remove leading spaces
```bash
sed -i -r 's/^\s+//g' <file>
```
### To remove empty lines and print results to stdout
```bash
sed '/^$/d' <file>
```
### To replace newlines in multiple lines
```bash
sed ':a;N;$!ba;s/\n//g' <file>
```
### To insert a line before a matching pattern
```bash
sed '/Once upon a time/i\Chapter 1'
```
### To add a line after a matching pattern
```bash
sed '/happily ever after/a\The end.'
```

# cp command

### To copy a file
```bash
cp ~/Desktop/foo.txt ~/Downloads/foo.txt
````
### To copy a directory
```bash
cp -r ~/Desktop/cruise_pics/ ~/Pictures/
```
### To create a copy but ask to overwrite if the destination file already exists
```bash
cp -i ~/Desktop/foo.txt ~/Documents/foo.txt
```
### To create a backup file with date
```bash
cp foo.txt{,."$(date +%Y%m%d-%H%M%S)"}
```
---

# cat command

### To display the contents of a file
```bash
cat <file>
```
### To display file contents with line numbers
```bash
cat -n <file>
```
### To display file contents with line numbers (blank lines excluded)
```bash
cat -b <file>
```

---

# tee command

### To tee stdout to <outfile>
```bash
ls | tee <outfile>
```
### To tee stdout and append to <outfile>
```bash
ls | tee -a <outfile>
```
### To tee stdout to the terminal, and also pipe it into another program for further processing
```bash
ls | tee /dev/tty | xargs printf "\033[1;34m%s\033[m\n"
```
---

# sort command


### To sort a file
```bash
sort <file>
```
### To sort a file by keeping only unique
```bash
sort -u <file>
```
### To sort a file and reverse the result
```bash
sort -r <file>
```
### To sort a file randomly
```bash
sort -R <file>
```

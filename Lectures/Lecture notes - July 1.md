## Commands

cat command
cut command
tail command
head command
awk command (is asked on interviews a lot)
grep command (is asked on interviews a lot)
egrep command
diff command
mv command - move
tar command - archive
gzip command

## Few examples

`echo "hello world" | awk '{gsub(/world/, "moon"); print}'`
prints "hello moon"

`grep hello file.txt`
searches for "hello" in file.txt (case sensitive)

`grep -i hello file.txt`
searches for "hello" in file.txt (not case sensitive)

`diff file1.txt file2.txt`

`tar -cvf files.tar`
create an archive from files in the directory

`tar -xvf files.tar`
extract contents of archive files.tar

`gzip files.tar`

`ls -alh files.tar.gz`

`gunzip files.tar.gz`

`gzip files.tar`


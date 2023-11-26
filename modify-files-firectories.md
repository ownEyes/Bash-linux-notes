# modify-files-directories
Notes on modifying files and directories in linux

![IMG_29BAAF801B32-1](https://user-images.githubusercontent.com/58792/146691100-78f4abbc-e22f-41fd-bc9f-fbde67ffc92c.jpeg)

## Create, Copy, Move and Sync Data

```bash

# Make a directory
mkdir foo

# Make many directories 
mkdir -p bar/bam/biz

# Create files
touch bar/one.txt && touch bam/two.txt && touch biz/three.txt

# Move files
mv bar /tmp/

# copy files
cp -r bam /tmp/

# sync files (keeps both directories the same)
rsync -av foo/ newspot/foo/

# delete directory
mkdir noneDir
rmdir noneDir

# remove folder
rm -rf biz

```

## Permissions

```bash
Name    Owner   Group   Other
access  r w x   r w x   r w x
binary  4 2 1   4 2 1   4 2 1
enabled 1 1 1   1 0 1   1 0 0

result  4 2 1   4 0 1   400

total     7       5       4       
```

## Archiving

### Zip

```
# archive
zip -r archives/foo.zip foo
cd archives
#unarchive
unzip foo.zip
```

### Tar

```
# archive
tar -zcvf archives/foo.tgz foo

#unarchive
tar -zxvf foo.tgz
```









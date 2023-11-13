# unix-streams
standard input/output/error

![Output](https://user-images.githubusercontent.com/58792/143476648-735c106b-3679-4f2d-b1ae-d718347ad68c.png)

## Standard Out

* Filtering examples:  Sort and Uniq

echo -e "Apple\nCarrot\nBanana" | sort
echo -e "Apple\nCarrot\nBanana\nApple" | sort | uniq -c 

* Grep

echo -e "Apple\nCarrot\nBanana\nApple" | sort | uniq -c | grep Apple

ps -ef | grep python

* Rev

echo 1993
echo 1993 | rev

## Standard Input

* Ask for user input

read -p 'File: ' FILENAME

* put it into a script

 less < fruit.txt

## Standard Error

* Create Error
ls -l /var/FAKEDIR

* Write error to a file
ls -l /var/FAKEDIR 2>error.txt

* Throw Error away
ls -l /var/FAKEDIR 2>/dev/null

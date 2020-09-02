# Shell-data-processing

### This is the link used to retrive words

[Romeo and Juliet](http://shakespeare.mit.edu/romeo_juliet/full.html)


## How to retrieve text from URL

* Curl command : ```curl "http://shakespeare.mit.edu/romeo_juliet/full.html" -O data.txt```

## How to process text data in data.txt

* Transform each space ' ' into a return character '\12' : ```tr ' ' '\12' < data.txt```
* Sorting the data : ```tr ' ' '\12' < data.txt | sort```
* Sorting the output based on uniqueness : ```tr ' ' '\12' < data.txt | sort | uniq -c```
* Pipe the reduced output to sort with -nr flag : ```tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr```
* Redirect the output to result.txt : ```tr ' ' '\12' < data.txt | sort | uniq -c | sort -nr > result.txt```

## About Bash shell

*  Up arrow in your bash shell is used to get previous executed commands
* "-n" - To sort the data by comparing with numerical value.
* "-r" - To reverse the results. 
* one dash is used for single letter flag, and two dash for more than one.
* ```ls > newfile.txt``` is used to redirect output into a file.
* ```ls >> newfile.txt``` is used to redirect and append the output into a file.






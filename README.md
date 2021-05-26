
# cURL (curl) commands list

This is a demo to test and practice frequently used cURL commands in most programming projects. A <code>Git bash</code> can be used to run most Linux-like commands in Windows and thus is used to test curl here.

A fake REST API testing web is used here:

	https://jsonplaceholder.typicode.com/

## curl GET request

* Show all different cmds for curl.

	curl -- help

* Get info from a REST GET request

	<code> curl https://jsonplaceholder.typicode.com/posts </code> <br>
	<code> curl https://jsonplaceholder.typicode.com/posts/2 </code>

* Add parameter to add head info in a curl GET request

	curl -i https://jsonplaceholder.typicode.com/posts/2 <br>
	
* If we just want to print head info in a curl GET request

	curl -I https://jsonplaceholder.typicode.com/posts/2, or <br>
	curl --head https://jsonplaceholder.typicode.com/posts/2

* Save response info into a local file

	curl -o test.txt https://jsonplaceholder.typicode.com/posts <br>
	read the file by typing <code>cat test.txt</code>
	
* Download a file from the server

	curl -O https://jsonplaceholder.typicode.com/posts

* Download an image from the server

	curl -O https://i.imgur.com/IBItATn.png


## curl POST request

* POST request to create a new resource

	curl --data "title=Hello&body=Hello world&userId=101" https://jsonplaceholder.typicode.com/posts

* PUT request to update an existing resource

	curl -X PUT -d "title=Hello put request" https://jsonplaceholder.typicode.com/posts/3

* DELETE request to remove an existing resource

	curl -X DELETE "title=Hello put request" https://jsonplaceholder.typicode.com/posts/4


## curl inpute username/password for security authentication

* Input username/password in a curl request

	curl -u username:password http://xxx.com

## Add "-L" to follow a moved webpage

	curl google.com (which showed the webpage moved to a new address), so use:<br>
	curl -L google.com

## Use curl to update/download FTP files

	Upload a file: <code>curl -u test@traversymedia.com:password -T filename.txt ftp://ftp.traversmedia.com</code> <br>
	Download a file: <code>curl -u test@traversymedia.com:password -O ftp://ftp.traversmedia.com/filename.txt</code>

# Note:

A YouTube video to follow for all the listed demo cmds is called "Basic cURL Tutorial" at:

	https://www.youtube.com/watch?v=7XUibDYw4mc
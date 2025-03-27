# Types of links
## Softlink
## Hard link

### Use of links in maintaining versions of lib or other shared resouces/files
filename : foo  
filename with version : foo-2.6  
filename with version is preferred for maintaining versions of various files e.g. library files.  

If version changes so filename will change.  
Then need to track down every program that might use it and change it to look for a new name at every new version release.  

If we make soft link (foo-> foo-2.6) the above problem is solved.  
Also it has benifit :  
If 2.6 does not work we can degrade to old version 2.5 and point to previous working version (foo-> foo-2.5)  
Also we can keep all versions avaialble and point using soft link to the correct one whenever needed.  

libc.so.6 -> libc-2.6.so  
libc.so.6 that points to a shared library file called libc-2.6.so  
This means that programs looking for libc.so.6 will actually get the file libc-2.6.so.   

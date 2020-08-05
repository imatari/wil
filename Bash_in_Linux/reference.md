- list only directories  
`ls -d */`

- list all folders under one folder  
`ls -d MG/*/`

- find all files that have a filename containing the string 'rea'  
`find . -iname '*rea*'`  
notes:  
    - the dot (`.`) means current folder
    - this instruction will work recursively
    - `-iname` makes the search case insensitive  

<img src="./images/find.jpg" alt="using the find command" width="600" />

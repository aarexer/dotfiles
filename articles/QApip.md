## Some usefull commands in python 3
**NOTE**: I have two python versions in my OS - and pip for python 3 is pip3.

* How to update pip?

```pip3 install --upgrade pip```

* Using pip when you want to install external library, for example - requests?

 ```pip3 install requests```

  **NOTE**: If you don't want to install library as global, you should use virtualenv.
  See more below.

* How i can see what libraries have been installed by pip?
 
 ```pip3 freeze```

* How i can use virtualenv?
  
  First of all you should install it by pip:
  ```pip3 install virtualenv```

  After first step you should create virtual environment:
  ```virtualenv dirname -p python3```

  By executing this command you create directory with name `dirname` and isolated python3 environment inside.
  And you can start working by:
  ```source dirname/bin/activate```

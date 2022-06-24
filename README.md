# Linux env programming tips and tricks

## Docker

**Go into a runnnig docker**

First of all get the name of the **container** with 
```
docker ps
```
and paste the name into this command 
```
docker exec -i -t <container> /bin/bash
```

## Python programming

Get the current directory of the runnig script

```
print("CURRENT DIRECTOR : %s", str(Path(__file__).parent.absolute()))
```
Or the absolute path to the script itself
```
print("CURRENT DIRECTOR : %s", str(Path(__file__).absolute()))
```

This might be useful to manage the path string: in this case the script has to load a file which is in ../media wrt him that's inside scripts folder. The way i do successfully is to modify the path string
```
curr_directory = str(Path(__file__).parent.absolute())
# removing scripts from the string
curr_directory = curr_directory[0:len(curr_directory)-len("scripts")]
# adding the last part to sthe string
curr_directory += "media"
```

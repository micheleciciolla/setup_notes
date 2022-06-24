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

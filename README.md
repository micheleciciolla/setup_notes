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


### containers

The containers command lists all containers on the local machine.  

```
Usage: spoon containers <options>

<options> available:
      --csv                  Print output with tab-separated columns
  -l, --latest               List the most recently created container
  -n=VALUE                   List the 'n' most recently created containers
      --no-trunc             Don't truncate output
```

Command line flags for the `containers` flag serve to modify or filter the command's results. 

```
# Only show most recently created container
> spoon containers -l

ID            Images                  Command      Created               Status
--            ------                  -------      -------               ------
db4d5baff206  spoonbrew/scratch                    9/3/2014 11:26:35 AM  Stopped

# Show last 'n' created containers
> spoon containers -n=3
ID            Images                  Command      Created               Status
--            ------                  -------      -------               ------
db4d5baff206  spoonbrew/scratch                    9/3/2014 11:26:35 AM  Stopped
b5c63c6d242e  spoonbrew/node          node app.js  9/3/2014 11:25:18 AM  Running
b92981a3dd27  spoonbrew/node          node app.js  9/3/2014 11:05:36 AM  Stopped
```

If the value specified for `-n` is greater than the number of containers present on the local machine, all of the containers are listed (same result as running `spoon containers`). 

#### Formatting Results

The table that is returned by the containers command is space-formatted. If you wish to return the table with tabs between each column then use the `--csv` flag. 

```
> spoon containers --csv
```

Data in the table returned by the containers command is truncated so that it prints nicely and is easily readable in a command prompt. If you wish to view the untruncated data in each column, use the `--no-trunc` flag. 

```
> spoon containers --no-trunc
```

The `--no-trunc` flag includes additional columns in the output, **Ports** and **Settings**, as seen below.

	ID                                Images       Command  Created               Status   Ports      Settings
	--                                ------       -------  -------               ------   -----      --------
	df6ac93f8b6147b986d4c7849c3dcef0  ghost:0.5.1           8/26/2014 3:27:17 PM  Running  8080:2368  SpawnVm
	d6e44ae706c44ed1bd75a0830bed3239  ghost:0.5.1           8/26/2014 3:22:14 PM  Stopped             SpawnVm

The **Ports** column contains active port mappings. See the `spoon netstat` command for more information.
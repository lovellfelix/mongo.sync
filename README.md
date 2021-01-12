# mongo sync

To clone in real time using mongo stream a cluster into another cluster with the option to change the database name and the collection name.

## How to run it

- Create a file similar to options.json at the root folder and set the right configuration 
- Set an environment variable to point to this file
- run the code

here is a bash script example 
```bash
export SOAJS_MONGO_SYNC_OPTIONS=./options.json

node main.js
```

### Environment variables
ENV Variable | Description | Default
--- | ----- | :---:
SOAJS_MONGO_SYNC_OPSTIME | 0 = turned off, 1 = start from yesterday, 2 = use time from options.json | 0
SOAJS_MONGO_SYNC_DEBUG | 0 = turned off, 1 = turned on | 0
SOAJS_MONGO_SYNC_OPTIONS | check options.json | no default, required

### Example
by setting SOAJS_MONGO_SYNC_OPSTIME=1 and adding copy=true in options.json, all document will be copied first and sync will start from yesterday's date

### License
*Copyright SOAJS All Rights Reserved.*

Use of this source code is governed by an Apache license that can be found in the LICENSE file at the root of this repository.

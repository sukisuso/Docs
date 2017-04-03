## MONGO DB

#### Mongo dump: crete backup of mongo
###### full data base
```
$ mongodump --db=example-dump
```

###### One Collection
```
$ mongodump --db=<old_db_name> --collection=<collection_name>
```

###### Restore full data base
```
$ mongorestore dump/
```

###### Restore one collection
```
$ mongorestore -d some_other_db -c some_or_other_collection dump/some_collection.bson
```


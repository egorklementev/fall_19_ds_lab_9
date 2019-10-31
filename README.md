# fall_19_ds_lab_9
I used the chat from here:
https://github.com/ezesundayeze/anonymouse-realtime-chat-app

status and config before primary node got down:
```
rs.status()
{
        "set" : "rs0",
        "date" : ISODate("2019-10-31T19:03:38.828Z"),
        "myState" : 1,
        "term" : NumberLong(1),
        "syncingTo" : "",
        "syncSourceHost" : "",
        "syncSourceId" : -1,
        "heartbeatIntervalMillis" : NumberLong(2000),
        "majorityVoteCount" : 2,
        "writeMajorityCount" : 2,
        "optimes" : {
                "lastCommittedOpTime" : {
                        "ts" : Timestamp(1572548617, 1),
                        "t" : NumberLong(1)
                },
                "lastCommittedWallTime" : ISODate("2019-10-31T19:03:37.548Z"),
                "readConcernMajorityOpTime" : {
                        "ts" : Timestamp(1572548617, 1),
                        "t" : NumberLong(1)
                },
                "readConcernMajorityWallTime" : ISODate("2019-10-31T19:03:37.548Z"),
                "appliedOpTime" : {
                        "ts" : Timestamp(1572548617, 1),
                        "t" : NumberLong(1)
                },
                "durableOpTime" : {
                        "ts" : Timestamp(1572548617, 1),
                        "t" : NumberLong(1)
                },
                "lastAppliedWallTime" : ISODate("2019-10-31T19:03:37.548Z"),
                "lastDurableWallTime" : ISODate("2019-10-31T19:03:37.548Z")
        },
        "lastStableRecoveryTimestamp" : Timestamp(1572548597, 1),
        "lastStableCheckpointTimestamp" : Timestamp(1572548597, 1),
        "electionCandidateMetrics" : {
                "lastElectionReason" : "electionTimeout",
                "lastElectionDate" : ISODate("2019-10-31T18:15:16.562Z"),
                "termAtElection" : NumberLong(1),
                "lastCommittedOpTimeAtElection" : {
                        "ts" : Timestamp(0, 0),
                        "t" : NumberLong(-1)
                },
                "lastSeenOpTimeAtElection" : {
                        "ts" : Timestamp(1572545706, 1),
                        "t" : NumberLong(-1)
                },
                "numVotesNeeded" : 2,
                "priorityAtElection" : 1,
                "electionTimeoutMillis" : NumberLong(10000),
                "numCatchUpOps" : NumberLong(27017),
                "newTermStartDate" : ISODate("2019-10-31T18:15:17.463Z"),
                "wMajorityWriteAvailabilityDate" : ISODate("2019-10-31T18:15:18.331Z")
        },
        "members" : [
                {
                        "_id" : 0,
                        "name" : "inst1:27017",
                        "ip" : "172.31.44.56",
                        "health" : 1,
                        "state" : 1,
                        "stateStr" : "PRIMARY",
                        "uptime" : 2993,
                        "optime" : {
                                "ts" : Timestamp(1572548617, 1),
                                "t" : NumberLong(1)
                        },
                        "optimeDate" : ISODate("2019-10-31T19:03:37Z"),
                        "syncingTo" : "",
                        "syncSourceHost" : "",
                        "syncSourceId" : -1,
                        "infoMessage" : "",
                        "electionTime" : Timestamp(1572545716, 1),
                        "electionDate" : ISODate("2019-10-31T18:15:16Z"),
                        "configVersion" : 1,
                        "self" : true,
                        "lastHeartbeatMessage" : ""
                },
                {
                        "_id" : 1,
                        "name" : "inst2:27017",
                        "ip" : "172.31.33.14",
                        "health" : 1,
                        "state" : 2,
                        "stateStr" : "SECONDARY",
                        "uptime" : 2912,
                        "optime" : {
                                "ts" : Timestamp(1572548617, 1),
                                "t" : NumberLong(1)
                        },
                        "optimeDurable" : {
                                "ts" : Timestamp(1572548617, 1),
                                "t" : NumberLong(1)
                        },
                        "optimeDate" : ISODate("2019-10-31T19:03:37Z"),
                        "optimeDurableDate" : ISODate("2019-10-31T19:03:37Z"),
                        "lastHeartbeat" : ISODate("2019-10-31T19:03:37.814Z"),
                        "lastHeartbeatRecv" : ISODate("2019-10-31T19:03:37.814Z"),
                        "pingMs" : NumberLong(0),
                        "lastHeartbeatMessage" : "",
                        "syncingTo" : "inst1:27017",
                        "syncSourceHost" : "inst1:27017",
                        "syncSourceId" : 0,
                        "infoMessage" : "",
                        "configVersion" : 1
                },
                {
                        "_id" : 2,
                        "name" : "inst3:27017",
                        "ip" : "172.31.34.75",
                        "health" : 1,
                        "state" : 2,
                        "stateStr" : "SECONDARY",
                        "uptime" : 2912,
                        "optime" : {
                                "ts" : Timestamp(1572548617, 1),
                                "t" : NumberLong(1)
                        },
                        "optimeDurable" : {
                                "ts" : Timestamp(1572548617, 1),
                                "t" : NumberLong(1)
                        },
                        "optimeDate" : ISODate("2019-10-31T19:03:37Z"),
                        "optimeDurableDate" : ISODate("2019-10-31T19:03:37Z"),
                        "lastHeartbeat" : ISODate("2019-10-31T19:03:37.590Z"),
                        "lastHeartbeatRecv" : ISODate("2019-10-31T19:03:36.995Z"),
                        "pingMs" : NumberLong(0),
                        "lastHeartbeatMessage" : "",
                        "syncingTo" : "inst1:27017",
                        "syncSourceHost" : "inst1:27017",
                        "syncSourceId" : 0,
                        "infoMessage" : "",
                        "configVersion" : 1
                }
        ],
        "ok" : 1,
        "$clusterTime" : {
                "clusterTime" : Timestamp(1572548617, 1),
                "signature" : {
                        "hash" : BinData(0,"AAAAAAAAAAAAAAAAAAAAAAAAAAA="),
                        "keyId" : NumberLong(0)
                }
        },
        "operationTime" : Timestamp(1572548617, 1)
}
```
---
```
rs.conf()
{
        "_id" : "rs0",
        "version" : 1,
        "protocolVersion" : NumberLong(1),
        "writeConcernMajorityJournalDefault" : true,
        "members" : [
                {
                        "_id" : 0,
                        "host" : "inst1:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                },
                {
                        "_id" : 1,
                        "host" : "inst2:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                },
                {
                        "_id" : 2,
                        "host" : "inst3:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                }
        ],
        "settings" : {
                "chainingAllowed" : true,
                "heartbeatIntervalMillis" : 2000,
                "heartbeatTimeoutSecs" : 10,
                "electionTimeoutMillis" : 10000,
                "catchUpTimeoutMillis" : -1,
                "catchUpTakeoverDelayMillis" : 30000,
                "getLastErrorModes" : {

                },
                "getLastErrorDefaults" : {
                        "w" : 1,
                        "wtimeout" : 0
                },
                "replicaSetId" : ObjectId("5dbb24aa8b0680b67bd4b1ab")
        }
}
```

Screenshot: https://imgur.com/a/yVffVoM

The status and config after primary node got down:

```
rs.status()
{
        "set" : "rs0",
        "date" : ISODate("2019-10-31T19:16:29.472Z"),
        "myState" : 1,
        "term" : NumberLong(2),
        "syncingTo" : "",
        "syncSourceHost" : "",
        "syncSourceId" : -1,
        "heartbeatIntervalMillis" : NumberLong(2000),
        "majorityVoteCount" : 2,
        "writeMajorityCount" : 2,
        "optimes" : {
                "lastCommittedOpTime" : {
                        "ts" : Timestamp(1572549385, 1),
                        "t" : NumberLong(2)
                },
                "lastCommittedWallTime" : ISODate("2019-10-31T19:16:25.578Z"),
                "readConcernMajorityOpTime" : {
                        "ts" : Timestamp(1572549385, 1),
                        "t" : NumberLong(2)
                },
                "readConcernMajorityWallTime" : ISODate("2019-10-31T19:16:25.578Z"),
                "appliedOpTime" : {
                        "ts" : Timestamp(1572549385, 1),
                        "t" : NumberLong(2)
                },
                "durableOpTime" : {
                        "ts" : Timestamp(1572549385, 1),
                        "t" : NumberLong(2)
                },
                "lastAppliedWallTime" : ISODate("2019-10-31T19:16:25.578Z"),
                "lastDurableWallTime" : ISODate("2019-10-31T19:16:25.578Z")
        },
       "lastStableRecoveryTimestamp" : Timestamp(1572549375, 1),
        "lastStableCheckpointTimestamp" : Timestamp(1572549375, 1),
        "electionCandidateMetrics" : {
                "lastElectionReason" : "stepUpRequestSkipDryRun",
                "lastElectionDate" : ISODate("2019-10-31T19:14:15.372Z"),
                "termAtElection" : NumberLong(2),
                "lastCommittedOpTimeAtElection" : {
                        "ts" : Timestamp(1572549247, 1),
                        "t" : NumberLong(1)
                },
                "lastSeenOpTimeAtElection" : {
                        "ts" : Timestamp(1572549247, 1),
                        "t" : NumberLong(1)
                },
                "numVotesNeeded" : 2,
                "priorityAtElection" : 1,
                "electionTimeoutMillis" : NumberLong(10000),
                "priorPrimaryMemberId" : 0,
                "numCatchUpOps" : NumberLong(27017),
                "newTermStartDate" : ISODate("2019-10-31T19:14:15.572Z"),
                "wMajorityWriteAvailabilityDate" : ISODate("2019-10-31T19:14:15.986Z")
        },
        "members" : [
                {
                        "_id" : 0,
                        "name" : "inst1:27017",
                        "ip" : "172.31.44.56",
                        "health" : 0,
                        "state" : 8,
                        "stateStr" : "(not reachable/healthy)",
                        "uptime" : 0,
                        "optime" : {
                                "ts" : Timestamp(0, 0),
                                "t" : NumberLong(-1)
                        },
                        "optimeDurable" : {
                                "ts" : Timestamp(0, 0),
                                "t" : NumberLong(-1)
                        },
                        "optimeDate" : ISODate("1970-01-01T00:00:00Z"),
                        "optimeDurableDate" : ISODate("1970-01-01T00:00:00Z"),
                        "lastHeartbeat" : ISODate("2019-10-31T19:16:24.932Z"),
                        "lastHeartbeatRecv" : ISODate("2019-10-31T19:14:15.873Z"),
                        "pingMs" : NumberLong(0),
                        "lastHeartbeatMessage" : "Error connecting to inst1:27017 (172.31.44.56:27017) :: caused by :: No route to host",
                        "syncingTo" : "",
                        "syncSourceHost" : "",
                        "syncSourceId" : -1,
                        "infoMessage" : "",
                        "configVersion" : -1
                },
                {
                        "_id" : 1,
                        "name" : "inst2:27017",
                        "ip" : "172.31.33.14",
                        "health" : 1,
                        "state" : 1,
                        "stateStr" : "PRIMARY",
                        "uptime" : 3729,
                        "optime" : {
                                "ts" : Timestamp(1572549385, 1),
                                "t" : NumberLong(2)
                        },
                        "optimeDate" : ISODate("2019-10-31T19:16:25Z"),
                        "syncingTo" : "",
                        "syncSourceHost" : "",
                        "syncSourceId" : -1,
                        "infoMessage" : "",
                        "electionTime" : Timestamp(1572549255, 1),
                        "electionDate" : ISODate("2019-10-31T19:14:15Z"),
                        "configVersion" : 1,
                        "self" : true,
                        "lastHeartbeatMessage" : ""
                },
                {
                        "_id" : 2,
                        "name" : "inst3:27017",
                        "ip" : "172.31.34.75",
                        "health" : 1,
                        "state" : 2,
                        "stateStr" : "SECONDARY",
                        "uptime" : 3682,
                        "optime" : {
                                "ts" : Timestamp(1572549385, 1),
                                "t" : NumberLong(2)
                        },
                        "optimeDurable" : {
                                "ts" : Timestamp(1572549385, 1),
                                "t" : NumberLong(2)
                        },
                        "optimeDate" : ISODate("2019-10-31T19:16:25Z"),
                        "optimeDurableDate" : ISODate("2019-10-31T19:16:25Z"),
                        "lastHeartbeat" : ISODate("2019-10-31T19:16:29.401Z"),
                        "lastHeartbeatRecv" : ISODate("2019-10-31T19:16:27.908Z"),
                        "pingMs" : NumberLong(0),
                        "lastHeartbeatMessage" : "",
                        "syncingTo" : "inst2:27017",
                        "syncSourceHost" : "inst2:27017",
                        "syncSourceId" : 1,
                        "infoMessage" : "",
                        "configVersion" : 1
                }
        ],
        "ok" : 1,
        "$clusterTime" : {
                "clusterTime" : Timestamp(1572549385, 1),
                "signature" : {
                        "hash" : BinData(0,"AAAAAAAAAAAAAAAAAAAAAAAAAAA="),
                        "keyId" : NumberLong(0)
                }
        },
        "operationTime" : Timestamp(1572549385, 1)
}
```
---
```
rs.conf()
{
        "_id" : "rs0",
        "version" : 1,
        "protocolVersion" : NumberLong(1),
        "writeConcernMajorityJournalDefault" : true,
        "members" : [
                {
                        "_id" : 0,
                        "host" : "inst1:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                },
                {
                        "_id" : 1,
                        "host" : "inst2:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                },
                {
                        "_id" : 2,
                        "host" : "inst3:27017",
                        "arbiterOnly" : false,
                        "buildIndexes" : true,
                        "hidden" : false,
                        "priority" : 1,
                        "tags" : {

                        },
                        "slaveDelay" : NumberLong(0),
                        "votes" : 1
                }
        ],
        "settings" : {
                "chainingAllowed" : true,
                "heartbeatIntervalMillis" : 2000,
                "heartbeatTimeoutSecs" : 10,
                "electionTimeoutMillis" : 10000,
                "catchUpTimeoutMillis" : -1,
                "catchUpTakeoverDelayMillis" : 30000,
                "getLastErrorModes" : {

                },
                "getLastErrorDefaults" : {
                        "w" : 1,
                        "wtimeout" : 0
                },
                "replicaSetId" : ObjectId("5dbb24aa8b0680b67bd4b1ab")
        }
}
```

Screenshot: https://imgur.com/a/DPnCzsi


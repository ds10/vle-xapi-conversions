## Core variable
```
   uriBase = 'http://vle.jisc.ac.uk/'
   appurl = 'http://vle.jisc.ac.uk/'
   homepage = "http://vle.jisc.ac.uk/";
   info = 'University of Jisc Moodle';
   appsummary= 'Jisc VLE'
   appname = 'Jisc VLE';
   lang = 'en';
```

##Moodle

The moodle plugin is a log file extension, and therefore can only use items in the log file.  The table definition is as follows:


   field | type | more | xapi 
   ---|---|---|---
   `id` |bigint(10) |AUTO_INCREMENT | NOT USED
 `eventname`|  varchar(255) |  | used by plugin to determine verb
  `component`|  varchar(100)|  | used to construct part of object ID
  `action`|  varchar(100) |  | used to construct part of object ID
  `target`|  varchar(100)|  | NOT USED
  `objecttable` | varchar(50)|  | NOT USED
  `objectid` | bigint(10) | | NOT USED
  `crud` | varchar(1) | | NOT USED
  `edulevel` | tinyint(1) | | NOT USED
  `contextid`|  bigint(10)|  | NOT USED
  `contextlevel` | bigint(10)|  | NOT USED
  `contextinstanceid` | bigint(10)|  | NOT USED
  `userid` | bigint(10)|  internal Moodle ID| actor.account.name
  `courseid` | bigint(10) | internal moodle id | maps to courseid
  `relateduserid`|  bigint(10) |  | NOT USED
  `anonymous` | tinyint(1)|   | NOT USED
  `other`|  longtext| ,| NOT USED
  `timecreated` | bigint(10) | Unix timestamp | timestamp
  `origin`|  varchar(10)|  | NOT USED
  `ip` | varchar(45) |  | NOT USED
  `realuserid`|  bigint(10)|  DEFAULT NULL, | NOT USED
  
```
"actor": {
        "objectType": "Agent",
        "name": [Not provided],
        "account": {
            "name": "[moodle.userid]",
            "homePage": "[core.appurl]"
        }
```



##Blackboard

Docs for activity_accumulator
(http://library.blackboard.com/ref/1cd128b5-9264-4afa-bb75-ec72ad211158/tables/as_core/activity_accumulator.html#column-event_type)
    
    field | type | more|xapi
   ---|---|---|---
  pk1	  |  int		 |   This is the surrogate primary key for the table
  event_type| 	   varchar(30)	| 	either COURSE_ACCESS or CONTENT_ACCESS		
  user_pk1	|    int	| 	referencing the primary key of the [AS_CORE].users table. 
  course_pk1| 	int	|    referencing the primary key of the [AS_CORE].course_main table.
  group_pk1	 |   int	| 	referencing the primary key of the group table. 
  forum_pk1	 |   int	 |   primary key of the forum table. | Not NULL means it's a forum activity
  internal_handle	 |   varchar(255)	| internal_handle column of the [AS_CORE].navigation_item table. 
  content_pk1	 |   int	| 	primary key of the content table. 
  data| 	nvarchar(255)| 			
  timestamp	| datetime| ISO format	
  status| 	numeric	| 			
  messages| 	ntext	| 				
  session_id	| int	| 			


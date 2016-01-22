##Moodle

The moodle plugin is a log file extension, and therefore can only use items in the log file.  The table definition is as follows:


   field | type | more | xapi 
   ---|---|---|---
   `id` |bigint(10) |NOT NULL AUTO_INCREMENT | not used
 `eventname`|  varchar(255) | NOT NULL DEFAULT '', | used by plugin to determine verb
  `component`|  varchar(100)|  NOT NULL DEFAULT '', | used to construct part of object ID
  `action`|  varchar(100) | NOT NULL DEFAULT '', | used to construct part of object ID
  `target`|  varchar(100)|  NOT NULL DEFAULT '',
  `objecttable` | varchar(50)|  DEFAULT NULL,
  `objectid` | bigint(10) | DEFAULT NULL,
  `crud` | varchar(1) | NOT NULL DEFAULT '',
  `edulevel` | tinyint(1) | NOT NULL,
  `contextid`|  bigint(10)|  NOT NULL,
  `contextlevel` | bigint(10)|  NOT NULL,
  `contextinstanceid` | bigint(10)|  NOT NULL,
  `userid` | bigint(10)|  NOT NULL,| actor.account.name
  `courseid` | bigint(10) | DEFAULT NULL 
  `relateduserid`|  bigint(10) | DEFAULT NULL,
  `anonymous` | tinyint(1)|  NOT NULL DEFAULT '0',
  `other`|  longtext| ,
  `timecreated` | bigint(10) | NOT NULL,| timestamp
  `origin`|  varchar(10)|  DEFAULT NULL,
  `ip` | varchar(45) | DEFAULT NULL,
  `realuserid`|  bigint(10)|  DEFAULT NULL,


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
  timestamp	| datetime| 	
  status| 	numeric	| 			
  messages| 	ntext	| 				
  session_id	| int	| 			


##Moodle



##Blackboard

Docs for activity_accumulator
(http://library.blackboard.com/ref/1cd128b5-9264-4afa-bb75-ec72ad211158/tables/as_core/activity_accumulator.html#column-event_type)

pk1	int		This is the surrogate primary key for the table.
event_type	varchar(30)				false	false	
user_pk1	int		This is a Foreign Key referencing the primary key of the [AS_CORE].users table. 
course_pk1	int	This is a Foreign Key referencing the primary key of the [AS_CORE].course_main table.
group_pk1	int		This is a Foreign Key referencing the primary key of the group table. 
forum_pk1	int		This is a Foreign Key referencing the primary key of the forum table. 
internal_handle	varchar(255)	This is a Foreign Key referencing the internal_handle column of the [AS_CORE].navigation_item table. 
content_pk1	int		This is a Foreign Key referencing the primary key of the content table. 
data	nvarchar(255)			
timestamp	datetime	This is the date and/or time at which this event occurred.
status	numeric				
messages	ntext					
session_id	int				

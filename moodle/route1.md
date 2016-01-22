### A1 - demouser login

**Moodle**

``1	'\\core\\event\\user_loggedin'	'core'	'loggedin'	'user'	'user'	3	'r'	0	1	10	0	3	0	NULL	0	'a:1:{s:8:\"username\";s:8:\"demouser\";}'	1453204740	'web'	'86.156.130.212'	NULL``

* [xapi - moodle via xapi plugin](manual/A1.js)
* [xapi moodle via log convertor](auto/A1.js)

**Blackboard**

No equivalent logfile event

###A2 demouser views a course

**Moodle**

http://moodle.data.alpha.jisc.ac.uk/course/view.php?id=3

``2	'\\core\\event\\course_viewed'	'core'	'viewed'	'course'	NULL	NULL	'r'	2	26	50	3	3	3	NULL	0	'N;'	1453204748	'web'	'86.156.130.212'	NULL``

* [xapi - moodle via xapi plugin](manual/A2.js)
* [xapi moodle via log convertor](auto/A2.js)

** Blackboard**

The following is currently a similar, but not identifical, event:

```CONTENT_ACCESS,0000184D8,BRM4520,NULL,NULL,NULL,367159,NULL,2015-04-22 09:56:13.527,1,9023282```

###A3 demouser views a page

http://moodle.data.alpha.jisc.ac.uk/mod/page/view.php?id=5

``3	'\\mod_page\\event\\course_module_viewed'	'mod_page'	'viewed'	'course_module'	'page'	2	'r'	2	33	70	5	3	3	NULL	0	'N;'	1453204773	'web'	'86.156.130.212'	NULL``

* [xapi - moodle via xapi plugin](manual/A3.js)
* [xapi moodle via log convertor](auto/A3.js)

###A4 demouser views a URL

http://moodle.data.alpha.jisc.ac.uk/mod/url/view.php?id=6

``4	'\\mod_url\\event\\course_module_viewed'	'mod_url'	'viewed'	'course_module'	'url'	1	'r'	2	34	70	6	3	3	NULL	0	'N;'	1453204798	'web'	'86.156.130.212'	NULL```

* [xapi - moodle via xapi plugin](manual/A4.js)
* [xapi moodle via log convertor](auto/A4.js)

###A5 demouser views a word document

http://moodle.data.alpha.jisc.ac.uk/mod/resource/view.php?id=7 

``5	'\\mod_resource\\event\\course_module_viewed'	'mod_resource'	'viewed'	'course_module'	'resource'	1	'r'	2	35	70	7	3	3	NULL	0	'N;'	1453204818	'web'	'86.156.130.212'	NULL``

* [xapi - moodle via xapi plugin](manual/A5.js)
* [xapi moodle via log convertor](auto/A5.js)

###A6  demouser views a forum

**Moodle**

``6	'\\mod_forum\\event\\course_module_viewed'	'mod_forum'	'viewed'	'course_module'	'forum'	3	'r'	2	32	70	4	3	3	NULL	0	'N;'	1453204837	'web'	'86.156.130.212'	NULL``

* [xapi - moodle via xapi plugin](manual/A6.js)
* [xapi moodle via log convertor](auto/A6.js)
* 
**Blacboard**

``COURSE_ACCESS,0000184D8,BRM4520,NULL,NULL,discussion_board,NULL,Discussion Board,2015-04-22 09:56:35.537,1,9023282``


###A7 demouser logs out

``7	'\\core\\event\\user_loggedout'	'core'	'loggedout'	'user'	'user'	3	'r'	0	1	10	0	3	0	NULL	0	'a:1:{s:9:\"sessionid\";s:26:\"74v3jdh5ld2ps3eaearq3re7j5\";}'	1453205044	'web'	'86.156.130.212'	NULL
``
* [xapi - moodle via xapi plugin](manual/A7.js)
* [xapi moodle via log convertor](auto/A7.js)

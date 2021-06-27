# a10dance-functions

Live Wep API endpoints deployed with documentation written at https://hackmd.io/@KfflL-NrQia-oTecv4EItQ/SJpDEQQ2O

a10dance-functions uses Docker, Python and Flask to create images that can be built on Google Cloud Build containers and then deployed as web service endpoints using Google Cloud Run.

## register_person

### Registers the student into database

POST: https://registerperson-xb4yazikbq-as.a.run.app

Input - formdata containing these fields
* `student_id` : `string`
* `student_name` : `string`
* `image` : `file`

Output - json
* `success` : `boolean`
* `error` : `string`


## take_attendance

### Takes attendance for students detected in frame

POST: https://takeattendance-xb4yazikbq-as.a.run.app

Input - formdata containing these fields
* `image` : `file`

Output - json
* `success` : `boolean`
* `error` : `string`
* `student_id` : `array of strings`
* `student_name` : `array of strings`
* `bounding_boxes` : `array of arrays`

### Software Architecture
![Orbital Architecture](https://user-images.githubusercontent.com/35002411/123557232-5e42de80-d7c2-11eb-97df-e7e4a8648fca.png)

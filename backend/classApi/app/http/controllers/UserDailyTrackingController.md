## UserDailyTrackingController

- This File Contain logic of 
	- [findCourseDetails.](#findcoursedetails)
	- [getDailyTask.](#getdailytask)
	- [getTaskCharters.](#gettaskcharters)
	- [getJamSession.](#getjamsession)
	- [getTaskById.](#gettaskbyid)
	- [getSubmissionDetails.](#getsubmissiondetails)
	- [getTaskChartersVideo.](#gettaskchartersvideo)
	- [downloadSubmissionInZip.](#downloadsubmissionInzip)
	- [getDisscussionDetails.](#getdisscussiondetails)
	- [getOverAllAttendanceForCamp.](#getoverallattendanceforcamp)
	- [getWeekAttendance.](#getweekattendance)
	- [getUserByCourseId.](#getuserbycourseId)
	- [getAttendenceReportByUser.](#getattendencereportbyuser)
	- [getReportAsExcel.](#getreportasexcel)

### Dependencies 
```` php
use App\Core\Util\Message;
use App\ExpertsModels\GotoMeetingRecording;
use App\Http\Controllers\Course\UserCourseTrackingController;
use App\Models\CourseTracking;
use App\UserDailyAttendence;
use App\UserLiveAttendence;
use App\UserRecordedAttendence;
use Illuminate\Http\Request;
use Illuminate\Support\Facades\DB;
use App\ExpertsModels\AppUser;
use App\ExpertsModels\ExpertMeeting;
use App\ExpertsModels\Group;
use App\ExpertsModels\Program;
use App\ExpertsModels\ProgramGroup;
use App\ExpertsModels\Task;
use App\ExpertsModels\Team;
use App\ExpertsModels\UserSubmission;
use App\ExpertsModels\UserSubmissionFiles;
use App\ExpertsModels\TaskCharters;
use App\ExpertsModels\UserDailySubmission;
use App\ExpertsModels\JamSession;
use App\Http\Controllers\User\AuthController;
use App\ExpertsModels\MeetingTeam;
use App\MaskedURL;
use App\Models\SubmissionsEmailType;
use App\Models\VersionedCourse;
use App\Notifications\AccomplishmentJournalNotification;
use App\Notifications\FeedbackMeetingNotification;
use App\Notifications\ManualTriggerNotification;
use App\Notifications\SubmissionDeadlineNotification;
use App\TaskReSubmissionRequest;
use App\User;
use App\UserActivity;
use Carbon\Carbon;
use GuzzleHttp\Client;
use Illuminate\Support\Facades\Auth;
use Illuminate\Support\Facades\Log;
use Illuminate\Support\Facades\Mail;
use Illuminate\Support\Facades\Notification;
use App\Models\UserSubscription;
use JWTAuth;
use ZipArchive;
````

#### findCourseDetails
This Function use to find the course type to filter the program on the basis of that for example filter the program between submission hub,pBM Camp and Dialy
```` php
/*
	*params 
	@request->course_id
*/
public function findCourseDetails(Request $request)
{
	....
}
````
##### Api Url: http://api.kraftshala.com/daily-tracking/find-course
This api used at a time of course creation on expert admin platform
````javascript
 http://api.kraftshala.com/daily-tracking/find-course
````

### getDailyTask
This function is use to send the details of upcoming/completed based for a user on the basis of submission type
```` php
/*
	*params
	@req->course_id
	@req->submission_type
*/
public function getDailyTask(Request $req)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/daily-tracking/task/
This api is used on Dashboard and Submission Tab on learn platform new UI for PBM and Daily Course
````javascript
 http://api.kraftshala.com/daily-tracking/task/
````

### uploadSubmission
This function is used to submit the file uploaded by user for a daily course task
```` php
/*
	*params
	@auth token
	@request->submission_id
	@request->file
	@request->course_id
*/
public function uploadSubmission(Request $request)
{
	......
}
````

##### Api Url: http://api.kraftshala.com/daily-tracking/submission
This api ise used on learn platform new ui for daily course at a time of upload/resubmit submission
````javascript
 http://api.kraftshala.com/daily-tracking/submission/
````
### getTaskCharters
This function is used to send the details task charter
```` php
/*
	*params
	@auth token
	@request->task_id
*/
public function getTaskCharters(Request $request)
{
	......
}
````

##### Api Url: http://api.kraftshala.com/daily-tracking/charters/
````javascript
 http://api.kraftshala.com/daily-tracking/charters/
````
### getJamSession
This function is used to send the details of upcoming/past jam session based on type
```` php
/*
	*params
	@req->type
	@req->course_id
*/
public function getJamSession(Request $req)
{
	......
}
````

##### Api Url: http://api.kraftshala.com/daily-tracking/jam-session
This api is used on Dashboard and Submission Tab on learn platform new UI for PBM and Daily Course
````javascript
 http://api.kraftshala.com/daily-tracking/jam-session
````
### getTaskById
This function is used to send the details of task including guidelines , description and deadline 
```` php
/*
	*params
	@auth token
	@task_id
*/
public function getTaskById(Request $request,$task_id)
{
	......
}
````

##### Api Url: http://api.kraftshala.com/daily-tracking/task/{task_id}
This api is used to fetch the task details on learn platform new UI for PBM and Daily Course
````javascript
 http://api.kraftshala.com/daily-tracking/task/{task_id}
````
### getSubmissionDetails
This function is used to find the submission details for a specific task id ,means it is used to find that user is uploaded the submission for that task or not if submitted then submitted on time or not
```` php
/*
	*params
	@auth token
	@request->task_id
*/
public function getSubmissionDetails(Request $request, $task_id)
{
	......
}
````

##### Api Url: http://api.kraftshala.com/daily-tracking/submission/{task_id}
Used on learn platform new ui for PBM and daily course
````javascript
 http://api.kraftshala.com/daily-tracking/submission/{task_id}
````
### getTaskChartersFiles
Used to send the details of task charters including file link and video link
```` php
/*
	*params
	@auth token
	@task_id
*/
public function getTaskChartersFiles(Request $request,$task_id)
{
	......
}
````

##### Api Url: http://api.kraftshala.com/daily-tracking/charters/files/{task_id}
Used on learn platform for daily and New pbm course to fetch the charters files s3 link
````javascript
 http://api.kraftshala.com/daily-tracking/charters/files/{task_id}
````
### getTaskChartersVideo
```` php
/*
	*params
	@task_id
*/
public function getTaskChartersVideo($task_id)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/daily-tracking/charters/video/{task_id}
Used on learn platform for daily and New pbm course to fetch the charters videos s3 link
````javascript
 http://api.kraftshala.com/daily-tracking/charters/video/{task_id}
````
### downloadSubmissionInZip
This function is used to download the submission of a specific task in a zip file
```` php
/*
	*params
	@auth token
	@task_id
*/
public function downloadSubmissionInZip($task_id, Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/daily-tracking/submission/download/{task_id}
Used on learn platform new ui for daily and new PBM course
````javascript
 http://api.kraftshala.com/daily-tracking/submission/download/{task_id}
````
### getDisscussionDetails
```` php
/*
	*params
	@task_id
*/
public function getDisscussionDetails($task_id)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/daily-tracking/discussion/{task_id}
````javascript
 http://api.kraftshala.com/daily-tracking/discussion/{task_id}
````
### getOverAllAttendanceForCamp
```` php
/*
	*params
	@course_id
	@user
*/
public function getOverAllAttendanceForCamp($course_id,$user)
{
	......
}
````
### getOverAllAttendance
```` php
/*
	*params
	@request->course_id
*/
public function getOverAllAttendance(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/daily-tracking/attendance/
````javascript
 http://api.kraftshala.com/daily-tracking/attendance/
````
### getWeekAttendance
```` php
/*
	*params
	@auth token
*/
public function getWeekAttendance(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/daily-tracking/attendance/week
````javascript
 http://api.kraftshala.com/daily-tracking/attendance/week
````
### getUserByCourseId
```` php
/*
	*params
	@request->course_id
*/
public function getUserByCourseId(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/daily-tracking/getdata/
````javascript
 http://api.kraftshala.com/daily-tracking/getdata/
````
### getAttendenceReportByUser
```` php
/*
	*params
	@user_id
	@from
	@to
	@course_id (default = "5fb5198540b75e98348b4567")
*/
 public function getAttendenceReportByUser($user_id, $from, $to, $course_id = "5fb5198540b75e98348b4567")
{
	......
}
````
### getReportAsExcel
```` php
/*
	*params
	@report
	@to
	@from
*/
public function getReportAsExcel($report,$to,$from)
{
	......
}
````

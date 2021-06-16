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
This api is used on Dashboard and Submission Tab on learn new UI for PBM and Daily Course
````javascript
 http://api.kraftshala.com/daily-tracking/task/
````

### uploadSubmission
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
````javascript
 http://api.kraftshala.com/daily-tracking/submission/
````
### getTaskCharters
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
````javascript
 http://api.kraftshala.com/daily-tracking/jam-session
````
### getTaskById
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
````javascript
 http://api.kraftshala.com/daily-tracking/task/{task_id}
````
### getSubmissionDetails
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
````javascript
 http://api.kraftshala.com/daily-tracking/submission/{task_id}
````
### getTaskChartersFiles
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
````javascript
 http://api.kraftshala.com/daily-tracking/charters/video/{task_id}
````
### downloadSubmissionInZip
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

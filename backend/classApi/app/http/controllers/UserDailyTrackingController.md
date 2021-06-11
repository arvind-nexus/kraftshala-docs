## UserDailyTrackingController

- This File Contain logic of 
	- [User Deadline Extension Dashboard.](#index-function)
	- [Request Approved/Reject Api.](#request-function)
	- [From To submit during approval/reject by deadline extension mail Api.](#requestprocess-function)

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
````javascript
 http://api.kraftshala.com/daily-tracking/find-course
````

### getDailyTask
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
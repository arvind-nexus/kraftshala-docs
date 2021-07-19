## TaskController

### Dependencies 
```` php
use App\ExpertsModels\AppUser;
use App\ExpertsModels\ExpertMeeting;
use App\ExpertsModels\Group;
use App\ExpertsModels\Program;
use App\ExpertsModels\ProgramGroup;
use App\ExpertsModels\Task;
use App\ExpertsModels\Team;
use App\ExpertsModels\UserDailySubmission;
use App\ExpertsModels\UserSubmission;
use App\ExpertsModels\UserSubmissionFiles;
use App\ExpertsModels\TaskCharters;
use App\ExpertsModels\UserWeeklyTracking;
use App\Http\Controllers\User\AuthController;
use App\ExpertsModels\MeetingTeam;
use App\MaskedURL;
use Exception;
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
use Illuminate\Http\Request;
use Illuminate\Support\Facades\Auth;
use Illuminate\Support\Facades\Log;
use Illuminate\Support\Facades\Mail;
use Illuminate\Support\Facades\Notification;
use JWTAuth;
use Illuminate\Support\Facades\DB;

ini_set('max_execution_time', 9000);
````
#### getTasksByCourseID
```` php
/*
	*params 
	@request
*/
public function getTasksByCourseID(Request $request)
{
	....
}
````
##### Api Url: https://api.kraftshala.com/task/by-course
````javascript
https://api.kraftshala.com/task/by-course
````
#### getTaskCharters
```` php
/*
	*params 
	@request
*/
public function getTaskCharters(Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/taskcharter
````javascript
https://api.kraftshala.com/task/taskcharter
````
#### taskSubmission
```` php
/*
	*params 
	@request
*/
public function taskSubmission(Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/submit
````javascript
 https://api.kraftshala.com/task/submit
````
#### finalFeedback
```` php
/*
	*params 
	@request
*/
public function finalFeedback(Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/final/feedback
````javascript
https://api.kraftshala.com/task/final/feedback
````
#### updateFinalFeedBack
```` php
/*
	*params 
	@request
*/
public function updateFinalFeedBack(Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/store/feedback
````javascript
https://api.kraftshala.com/task/store/feedback
````
#### contentSubmission
```` php
/*
	*params 
	@request
*/
public function contentSubmission(Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/show/content/submission
````javascript
https://api.kraftshala.com/task/show/content/submission
````
#### getSubmittedFile
```` php
/*
	*params 
	@request
*/
public function getSubmittedFile(Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/show/file
````javascript
https://api.kraftshala.com/task/show/file
````
#### lockSubmission
```` php
/*
	*params 
	@request
*/
public function lockSubmission(Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/lock/submission
````javascript
https://api.kraftshala.com/task/lock/submission
````
#### unlockSubmission
```` php
/*
	*params 
	@request
*/
public function unlockSubmission(Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/unlock/submission
````javascript
https://api.kraftshala.com/task/unlock/submission
````
#### extendDeadlineSubmission
```` php
/*
	*params 
	@request
*/
public function extendDeadlineSubmission(Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/extedn/deadline/submission
````javascript
https://api.kraftshala.com/task/extedn/deadline/submission
````
#### reSubmission
```` php
/*
	*params 
	@request
*/
public function reSubmission(Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/re/submission
````javascript
https://api.kraftshala.com/task/re/submission
````
#### manualTriggerNotification
```` php
/*
	*params 
	@request
*/
public function manualTriggerNotification(Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/manual-triger/notifiaction
````javascript
https://api.kraftshala.com/task/manual-triger/notifiaction
````
#### getRatingByType
```` php
/*
	*params 
	@request
*/
public function getRatingByType(Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/submission-rating/type
````javascript
https://api.kraftshala.com/task/submission-rating/type
````
#### getMeetingTaskSubmissions
```` php
/*
	*params 
	@request
*/
public function  getMeetingTaskSubmissions(Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/submissions
````javascript
https://api.kraftshala.com/task/submissions
````
#### resubmissionRequests
```` php
public function resubmissionRequests()
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/submissions/re-submission
````javascript
https://api.kraftshala.com/task/submissions/re-submission
````
#### getReSubmissionRequests
```` php
/*
	*params 
	@request
*/
public function getReSubmissionRequests(Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/submissions/re-submission-list
````javascript
https://api.kraftshala.com/task/submissions/re-submission-list
````
#### getReSubmissionRequestBySubmissionID
```` php
/*
	*params 
	@request
*/
public function getReSubmissionRequestBySubmissionID(Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/submissions/get-request
````javascript
https://api.kraftshala.com/task/submissions/get-request
````
#### processExpertResubmission
```` php
/*
	*params 
	@request
*/
public function processExpertResubmission(Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/submissions/re-submission-request
````javascript
https://api.kraftshala.com/task/submissions/re-submission-request
````
#### getActiveSubmissionsByWeek
```` php
/*
	*params 
	@request
	@course_id
*/
public function getActiveSubmissionsByWeek( $course_id,Request $request)
{
	....
}
````
##### Api url: https://api.kraftshala.com/task/submissions/{course_id}
````javascript
https://api.kraftshala.com/task/submissions/{course_id}
````







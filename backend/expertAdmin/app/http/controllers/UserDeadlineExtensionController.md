## UserDeadlineExtensionController

- This File Contain logic of 
	- [User Deadline Extension Dashboard.](#index-function)
	- [Request Approved/Reject Api.](#request-function)
	- [From To submit during approval/reject by deadline extension mail Api.](#requestprocess-function)

### Dependencies 
```` php
use Illuminate\Http\Request;
use App\UserDeadlineApproval;
use App\AppUser;
use App\UserSubmission;
use Mail;
use \Illuminate\Database\QueryException;
````

#### SendMail function to send mail 
```` php
/*
	*params 
	@template --->blade template for email
	@data  ---> Data for email template
	@email ---> sender email id
	@name ---> sender name
	@subject ---> email subject
*/
public function sendMail($template, $data, $email, $name, $subject)
{
	....
}
````

### index function
```` php
/*
	*UserExtensionDeadline Dashboard index page
	*view ---> deadlineExtension/index.blade.php
*/
public function index()
{
	......
}
````
##### Url:  http://expertadmin.kraftshala.com/deadline
````javascript
http://expertadmin.kraftshala.com/deadline
````

### request function
```` php
/*
	*params
	@request->status ---> approved/reject
	@request->message (optional)
	@request->name ---> approver name
	@request->email ---> approver email
*/
public function request($kid, $task_id,Request $request)
{
	......
}
````
##### Api Url: http://expertadmin.kraftshala.com/deadline/request/{kid}/{task_id}/	(from mail)
##### Api Url: http://expertadmin.kraftshala.com/deadline/request/form/{kid}/{task_id}/ (from dashboard)
````javascript
http://expertadmin.kraftshala.com/deadline/request/{kid}/{task_id}/ (from mail)
````
````javascript
http://expertadmin.kraftshala.com/deadline/request/form/{kid}/{task_id}/ (from dashboard)
````

### requestProcess function	
```` php
/*
	*params
	@kid
	@task_id
	@email ---> approver email
	@name ---> approver name
*/
public function requestProcess($kid, $task_id, $email, $name)
 {
   ....
 }
````
##### Api Url: http://expertadmin.kraftshala.com/deadline/request/process/{kid}/{task_id}/{email}/{name}
````javascript
http://expertadmin.kraftshala.com/deadline/request/process/{kid}/{task_id}/{email}/{name}
````
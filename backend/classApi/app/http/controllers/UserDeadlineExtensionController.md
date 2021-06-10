## UserDeadlineExtensionController

- This File Contain logic of 
	- [Deadline extension store Api.](#store-function)
	- [Get status of a specific user specific task have extension Api.](#getstatus-function)
	- [Get task_ids of the tasks of a specific user which are pending Api.](#getpendingsubmission-function)

### Dependencies 
```` php
    use Illuminate\Http\Request;
	use App\ExpertsModels\UserDeadlineApproval;
	use App\ExpertsModels\UserSubmission;
	use App\ExpertsModels\AppUser;
	use App\Http\Controllers\User\AuthController;
	use App\Models\UserSubscription;
	use App\User;
	use Mail;
	use \Illuminate\Database\QueryException;
	use Illuminate\Support\Facades\DB;
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

### store function
To store the deadline extension request
```` php
/*
	*params
	@auth token --->bearer token
	@request->task_id
	@request->extension_date
	@request->reason (optional)
*/
public function store(Request $request)
{
	......
}
````
##### Api Url:  http://api.kraftshala.com/deadline/store?task_id={task_id}&extension_date={date}&reason={reason}
````javascript
http://api.kraftshala.com/deadline/store?task_id={task_id}&extension_date={date}&reason={reason}
````

### getStatus function
To get the status of user for a specific task have extension or not.
	
```` php
/*
	*params
	@auth token
	@task_id
*/
public function getStatus($task_id, Request $request)
 {
   ....
 }
````
##### Api Url: http://api.kraftshala.com/deadline/status/{task_id}
````javascript
http://api.kraftshala.com/deadline/status/{task_id}
````
### getPendingSubmission function
To get the pending submission of task_ids of specific user for a specific course which tasks don't have extensions.
```` php
/*
	*params
	@auth token
*/
public function getPendingSubmission(Request $request)
 {
	 ....
 }
````
##### Api Url:  http://api.kraftshala.com/deadline/pending
```` javascript
http://api.kraftshala.com/deadline/pending
````



## WorkingLeadsController

### Dependencies 
```` php
use App\ContactKraftshala;
use App\CounsellingSlot;
use App\Http\Controllers\EverWebinarController;
use App\Http\Controllers\LeadOwnerController;
use App\Http\Controllers\MailController;
use App\Http\Controllers\TextLocalController;
use App\Http\Controllers\TigerSheetUpdateQueryController;
use App\Http\Controllers\WhatsAppScriptController;
use App\KraftshalaApplicant;
use App\Http\Controllers\Controller;
use App\LeadOwner;
use App\WebinarCampaigns;
use Carbon\Carbon;
use Illuminate\Http\Request;
use Mail;
use App\Models\WorkingLeads;
use Hash;
use Config;
use App\Core\Exotel\SMS;
use Log;
use App\Models\ApplyNowRecommendation;
use Exception;
use App\Http\Controllers\EmailEditorController;
use App\Models\GoogleInvitationLead;
use App\Http\Controllers\KraftshalaCRMController;
use App\Http\Controllers\WebinarController;
````

#### submit_working_leads_data
```` php
/*
	*params 
	@request
*/
public function submit_working_leads_data(Request $request)
{
	....
}
````
##### Api Url: http://api.kraftshala.com/submit_working_leads_data
````javascript
 http://api.kraftshala.com/submit_working_leads_data
````

### mailCronJob
```` php
/*
	*params
	@request
*/
public function mailCronJob(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/testCorn
##### Api Url: http://api.kraftshala.com/testmailcronjob
##### Api Url: http://api.kraftshala.com/checkMailCronJob
````javascript
http://api.kraftshala.com/testCorn
http://api.kraftshala.com/testmailcronjob
http://api.kraftshala.com/checkMailCronJob
````

### registerPBM
```` php
/*
	*params
	@request
*/
public function registerPBM(Request $request)
{
	......
}
````

##### Api Url: http://api.kraftshala.com/registerPBM
````javascript
 http://api.kraftshala.com/registerPBM
````
### program_leads_custom
```` php
/*
	*params
	@request
*/
public function program_leads_custom(Request $request)
{
	......
}
````

##### Api Url: http://api.kraftshala.com/program_leads_custom
````javascript
 http://api.kraftshala.com/program_leads_custom
````
### program_leads_data
```` php
/*
	*params
	@request
*/
public function program_leads_data(Request $request)
{
	......
}
````

##### Api Url: http://api.kraftshala.com/program_leads_data
````javascript
 http://api.kraftshala.com/program_leads_data
````
### findSlotBookedCount
```` php
/*
	*params
	@request
*/
public function findSlotBookedCount(Request $request)
{
	......
}
````

##### Api Url: http://api.kraftshala.com/findSlotBookedCount
````javascript
 http://api.kraftshala.com/findSlotBookedCount
````
### webinar_leads
```` php
/*
	*params
	@request
*/
public function webinar_leads(Request $request)
{
	......
}
````

##### Api Url: http://api.kraftshala.com/webinar_leads
````javascript
 http://api.kraftshala.com/webinar_leads
````
### save_webinar_leads
```` php
/*
	*params
	@request
	@event
*/
public function save_webinar_leads(Request $request, $event)
{
	......
}
````
### common_leads_data
```` php
/*
	*params
	@request
*/
public function common_leads_data(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/common_leads_data
````javascript
 http://api.kraftshala.com/common_leads_data
````
### common_leads_send_invite
```` php
/*
	*params
	@request
*/
public function common_leads_send_invite(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/common_leads_send_invite
````javascript
 http://api.kraftshala.com/common_leads_send_invite
````
### saveRecommendations
```` php
/*
	*params
	@request
*/
public function saveRecommendations(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/saveRecommendations
````javascript
 http://api.kraftshala.com/saveRecommendations
````
### downloadWorkingLeadsShow
```` php
public function downloadWorkingLeadsShow()
{
	......
}
````
##### Api Url: http://api.kraftshala.com/export
````javascript
 http://api.kraftshala.com/export
````
### downloadWorkingLeads
```` php
/*
	*params
	@request
*/
public function downloadWorkingLeads(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/export (POST)
````javascript
 http://api.kraftshala.com/export (POST)
````
### getColumns
```` php
/*
	*params
	@name
*/
public function getColumns($name)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/columns/{db_name}
````javascript
 http://api.kraftshala.com/columns/{db_name}
````
### tigersheetCurlRequest
```` php
/*
	*params
	@url
	@data
*/
private function tigersheetCurlRequest($url, $data)
{
	......
}
````
### saveContactKraftshala
```` php
/*
	*params
	@request
*/
 public function saveContactKraftshala(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/contact_kraftshala
````javascript
 http://api.kraftshala.com/contact_kraftshala
````
### saveJobApplications
```` php
/*
	*params
	@request
*/
public function saveJobApplications(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/apply_kraftshala
````javascript
 http://api.kraftshala.com/apply_kraftshala
````
### getDropoutLeads
```` php
/*
	*params
	@request
*/
public function getDropoutLeads(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/getDropoutLeads
````javascript
 http://api.kraftshala.com/getDropoutLeads
````
### isUserRegisteredToProgram
```` php
/*
	*params
	@request
*/
public function isUserRegisteredToProgram(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/isUserRegisteredToProgram
````javascript
 http://api.kraftshala.com/isUserRegisteredToProgram
````
### allPrograms
```` php
public function allPrograms()
{
	......
}
````
##### Api Url: http://api.kraftshala.com/programs
````javascript
 http://api.kraftshala.com/programs
````
### programDropouts
```` php
/*
	*params
	@program_name
*/
public function programDropouts($program_name)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/program/{program_name}
````javascript
 http://api.kraftshala.com/program/{program_name}
````
### createSlots
```` php
/*
	*params
	@slots
	@start
	@end
	@interval
*/
private function createSlots($slots, Carbon $start, Carbon $end, $interval)
{
	......
}
````
### getEnrolledSlotsByDate
```` php
/*
	*params
	@slotDate
*/
private function getEnrolledSlotsByDate($slotDate)
{
	......
}
````
### slotsFilled
```` php
/*
	*params
	@request
*/
public function slotsFilled(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/slotsFilled
````javascript
 http://api.kraftshala.com/slotsFilled
````
### getAllPrograms
```` php
public static function getAllPrograms()
{
	......
}
````
### programStagingEmailsFromTigersheet
```` php
/*
	*params
	@request
*/
public function programStagingEmailsFromTigersheet(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/tigersheet/send-email
````javascript
 http://api.kraftshala.com/tigersheet/send-email
````
### programStagingEmailsSMS
```` php
/*
	*params
	@request
*/
public function programStagingEmailsSMS(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/tigersheet/process
````javascript
 http://api.kraftshala.com/tigersheet/process
````
### form_to_show
```` php
/*
	*params
	@request
*/
public function form_to_show(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/form_to_show
````javascript
 http://api.kraftshala.com/form_to_show
````
### counsellingCallReminder
```` php
/*
	*params
	@request
*/
public function counsellingCallReminder()
{
	......
}
````
##### Api Url: http://api.kraftshala.com/test-date
````javascript
 http://api.kraftshala.com/test-date
````
### getLeadsByEmail
```` php
/*
	*params
	@request
*/
public function getLeadsByEmail(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/get_leads_data/by-email
````javascript
 http://api.kraftshala.com/get_leads_data/by-email
````

### getLeadsByEmailTest
```` php
/*
	*params
	@request
*/
public function getLeadsByEmailTest(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/get_leads_data/by-email/test
````javascript
 http://api.kraftshala.com/get_leads_data/by-email/test
````
### deleteLeadsByEmailTest
```` php
/*
	*params
	@request
*/
public function deleteLeadsByEmailTest(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/delete_lead/by-email
````javascript
 http://api.kraftshala.com/delete_lead/by-email
````
### updateLeadsDataByEmail
```` php
/*
	*params
	@request
*/
public function updateLeadsDataByEmail(Request $request)
{
	......
}
````
##### Api Url: http://api.kraftshala.com/update_lead/by-email
````javascript
 http://api.kraftshala.com/update_lead/by-email
````
### sendCalenderInviteToPBMLeads
```` php
public static function sendCalenderInviteToPBMLeads()
{
	......
}
````
### sendDay3And4LeadMlpEmail
```` php
/*
	*params
	@request
*/
public static function sendDay3And4LeadMlpEmail()
{
	......
}
````
### sendWhatsAppSMSToPBMLeads
```` php
public static function sendWhatsAppSMSToPBMLeads()
{
	......
}
````
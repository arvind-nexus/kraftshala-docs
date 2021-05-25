# App Layout File
#### This file contains the logic which gets executed on every page

1. App Header and Footer gets executed here

2. This file also contains the feedback rating logic
    * [Mentor Rating](#mentor-rating)
    * [Webinar Feedback](#webinar-feedback)
    * [Expert Rating](#expert-rating)
    * [Charter Rating](#charter-rating)
    * [Peer Rating](#peer-rating)
    * [Personal User Details](#personal-user-details)
    * [Reflection Form](#reflection-form)


## Mentor Rating
Code for this can be found inside this function
```javascript
async checkMeeting() {
   ...
}
```
API Used : https://interactions.kraftshala.com/api/is_pending_feedback

```javascript
   `https://interactions.kraftshala.com/api/is_pending_feedback/${userID}`
```

## Webinar Feedback
Code for this can be found inside this function
```javascript
async checkMeeting() {
   ...
}
```
API Used : https://interactions.kraftshala.com/api/is_pending_feedback

```javascript
   `https://interactions.kraftshala.com/api/is_pending_feedback/${userID}`
```


## Expert Rating
Code for this can be found inside this function
```javascript
async checkMeeting() {
   ...
}
```
API Used : https://interactions.kraftshala.com/api/is_pending_feedback

```javascript
   `https://interactions.kraftshala.com/api/is_pending_feedback/${userID}`
```

## Charter Rating
Code for this can be found inside this function
```javascript
async checkMeeting() {
   ...
}
```
API Used : https://interactions.kraftshala.com/api/is_pending_feedback

```javascript
   `https://interactions.kraftshala.com/api/is_pending_feedback/${userID}`
```

## Peer Rating
Code for this can be found inside this function
```javascript
async checkMeeting() {
   ...
}
```
API Used : https://interactions.kraftshala.com/api/is_pending_feedback

```javascript
   `https://interactions.kraftshala.com/api/is_pending_feedback/${userID}`
```

## Personal User Details
Code for this can be found inside this function
```javascript
async personalForm() {
   ...
}
```
API Used : https://api.kraftshala.com/form/personal

```javascript
      const header = {
          headers: {
            authorization: 'Bearer ' + localStorage.getItem('auth_token'),
          },
        };

      const res = await Axios.get(`https://api.kraftshala.com/form/personal`, header);
```

## Reflection Form
Code for this can be found inside this function
```javascript
   async reflectionForm() {
      ...
   }
```
API Used : https://api.kraftshala.com/form/reflection

```javascript
      const header = {
          headers: {
            authorization: 'Bearer ' + localStorage.getItem('auth_token'),
          },
        };

      const res = await Axios.get(`https://api.kraftshala.com/form/reflection`, header);
```

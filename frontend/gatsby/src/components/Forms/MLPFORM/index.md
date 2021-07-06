# This file contains the main code for MLP Form

### Follwing are the components that gets imported in this page

1. Input - for all the input tags like:- Name, Email, Phone etc.
2. Select - for all the dropdown tags like:- Studying/Working, Degree, Year of completion
3. Slotdate - for choose your slot tag
4. Thankyou - for thank you screen that comes after the form is submitted successfully for the eligible users
5. InEligible - for ineligible  screen that comes after the form is submitted successfully for the ineligible users


### Following are the React state that this page holds 

```javascript
  const [visitorLoading, setVisitorLoading] = useState(false);
  const [detectDropOut, setdetectDropOut] = useState(false);
  const [btnClicked, setBtnClicked] = useState(false);
  const [btnLoading, setBtnLoading] = useState(false);
  const [showForm, setShowForm] = useState(true);
  const [showThankYou, setShowThankYou] = useState(false);
  const [showInEligible, setShowInEligible] = useState(false);
  const [formFields, setFormFields] = useState(formData);
  const [checkType, setType] = useState(false);
  const [scrollValidation, setScrollValidation] = useState(false);
  const [allFilled, setAllFilled] = useState(false);
  const [wpOptin, setWpOptin] = useState(true);
  const [emailAlreadyExists, setEmailAlreadyExists] = useState(false);
```

### Following are the React UseEffect lifecycle method that we use in this page

```javascript
  useEffect(() => {}, [checkType]); //this accepts checktype as its dependency and this checks for the type of user whether they studying or working or something else
  
    useEffect(() => {
  }, [scrollValidation]); //this accepts scrollValidation as its dependency and this one checks which input to scroll to when left empty by the user
  
  
    useEffect(() => {
  }, []); //this accepts empty dependecny array this one checks whether we already have a users information or not when they have their email id on the url'
  
  

```

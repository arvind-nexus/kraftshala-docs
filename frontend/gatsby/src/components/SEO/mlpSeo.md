# This file shows how we are using specific SEO for MLP Main Page

### It uses the same React Helment that we are using for all the pages

The only difference is that we are managing Course and FAQ structered data in this component

**Code Snippt for Course Structured Data**

```javascript
  let courseSnipptJSON = `{
    "@context": "https://schema.org",
    "@type": "Course",
    "name": "The Marketing Launchpad",
    "description": "A  Pay After Placement Online Digital Marketing Course with 8 week Internship. ",
    "provider": {
      "@type": "Organization",
      "name": "Kraftshala",
      "sameAs": "https://kraftshala.com/marketing-launchpad/"
    }
  }
`;
```

**Code Snippt for FAQS Structured Data**


```javascript
  let faqSnipptJSON = `  {
    "@context": "https://schema.org",
    "@type": "FAQPage",
    "mainEntity": [{
      "@type": "Question",
      "name": "What kind of questions can I expect in the screening test? How many rounds will be there? What is the selection criteria?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "<p>Stage 1: The Screening Test will happen on 2 fixed slots: 4th April / 11th April. This test will have 4 sections: Quant, Logical, Verbal and Marketing Acumen.
You can find some prep material in the link here: http://bit.ly/MLP-Prep-Material
For the Marketing Acumen Section, you will be shown proprietary videos from Kraftshala and you will need to attempt the questions to apply those concepts. Through this we are checking your overall acumen and your learnability.
Stage 2 of the Admission Process: The shortlisted candidates will then appear for the SOP round. You will need to send in your responses to explain your reason for joining the program. Since the program requires high effort / intent, we need to make sure that your overall motivation is aligned with us. You will get a total of 2-3 days to submit this. Some sample questions for this round can also be found in the above link. You will also be required to submit your educational details and location preferences (for internships / final roles) at this stage. We will release the final offers post this stage.</p>"
      }
    }, {
      "@type": "Question",
      "name": "What if I dont get selected into the program?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "In case you do not get selected into the launchpad, you will always have the option of applying again to the program again next year."
      }
}, {
      "@type": "Question",
      "name": "How do you build the curriculum of the Marketing Launchpad?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The curriculum for our programs is a synthesis of a series of discussions, inspirations, experiences, and expectations from the top performance and branding experts. It focuses on only those skills which are relevant for you to become a top-notch marketer in today’s digital age.
Our curriculum managers partner with hiring managers and subject matter experts from leading companies to figure the skills to be demonstrated at the workplace. The Marketing Launchpad is designed to build these skills through a thorough understanding of the roles and the responsibilities that you will be managing.
We also have a strong feedback loop where the data on candidates’ performance goes into improving the learning experience continuously."
      }
}, {
      "@type": "Question",
      "name": "Can I have a demo class before I get enrolled?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The value of Kraftshala programs comes from the Projects + Interactions + Content + recruiter recommendations + network. On content, we work with the experts mentioned on the website to create both frameworks that help build concepts and examples and cases. Perhaps you can look through some of the testimonials on the website to get a flavour- many of them speak specifically about Kraftshala content.
You will however, get a flavour of the kind of content we create through the screening test since that involves going through some of our proprietary frameworks to attempt the questions.
Apart from this, you can also attend the session on Marketing Careers being taken by Varun Satia, Founder of Kraftshala to get more information on how we teach. You will get access to this if you apply for the program."
      }
}, {
      "@type": "Question",
      "name": "I have a bachelor's degree in marketing already. How will this course be different from that?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Our curriculums are designed in close partnership with the industry. We start from the roles and back-track to teach only those concepts which will help you in your careers for the next 5 years.
Our programs are thus taken up by marketing students of BSchools as well – this includes all IIMs, XLRI, MDI, SPJAIN. Infact, even existing brand and marketing teams have taken up our programs to upskill themselves. Thus, everything that you learn with us will make you ready for the job!"
      }
}, {
      "@type": "Question",
      "name": "Will I have to go physically for the internship?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "By the time your internship starts, it’ll be around July. So if things are better by then in terms of COVID and the companies require you to come down, you have to go. If not, you will have a well structured experience crafted out for you virtually, so that you get the right kind of exposure that is required. During the internships, you will be spending your weekdays as a digital marketing intern, and Sundays with us to further sharpen your skill sets.
At the end of the internship, you might also have a chance to get confirmed in a full time role with the same company as well."
      }
}, {
      "@type": "Question",
      "name": "Will the internship have a stipend?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Mostly Yes. But we will prioritise your roles and the kind of exposure you get during these 8 weeks of internship. Please note that the final call on the internship duration would depend on the company you intern with."
      }
}, {
      "@type": "Question",
      "name": "Do I get a job guarantee?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "You will not be paying us till you get a job of 4.5 lakhs and above within 12 months of your program completion. If you don't get a job, we don't get paid. Hence we will dedicate every last resource to help you get the opportunities you deserve."
      }
}, {
      "@type": "Question",
      "name": "By the end of the launchpad, what kind of roles can I expect to find?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "On completion of this program, you would be well equipped in the marketing field to take on roles which are both strategy and execution driven. You can expect to be working with rapidly growing companies where there would be an extensive scope of growth. You would be a qualified candidate to apply to many roles such as Digital Marketing Analyst / Manager, Performance Marketing Analyst / Manager, SEO Analyst / Manager, Client Manager, Account Manager, Marketing analyst / executive, etc. You can check out the roles of our last batch on the website page."
      }
}, {
      "@type": "Question",
      "name": "I have just taken my final exams and have not received my degree yet. Can I still apply?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. You can discuss this with your Admissions Counsellor. To be eligible for the program, you need to be available for the next 20 weeks for a full time training & full time employment after completion of the program."
      }
}, {
      "@type": "Question",
      "name": "Will my previous experience in a non-marketing role be a hindrance in cracking a job?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The Marketing Launchpad is designed for individuals who are looking to kickstart their careers in the marketing field, irrespective of their previous background. We will train you from scratch and will make sure that by the end of the program, you possess all the skill sets to launch your bright marketing career."
      }
}, {
      "@type": "Question",
      "name": "I am working in a full time role and will not be able to attend the full-time classes. Can I self pace the program?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "No. The program is an extensive functional and behavioural training which can only be taken up by candidates who are willing to pursue it full time. Since it requires a lot of group work, live sessions, group feedbacks, self pace is not an option. The last 8 weeks of the program will be an internship which will again require the candidates to be present full time."
      }
}, {
      "@type": "Question",
      "name": "I am preparing for MBA 2021 intake, but I am not sure of my result. Can I withdraw from the program after I receive my result?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "If you have plans of pursuing higher education within the next 2 years, we would recommend that you don't apply for the program. The program is focused on getting you high potential roles without an MBA and in case you need more help in making that decision and understanding the career trajectories, you can discuss this with your counsellor. We will be happy to help, irrespective of whether you take the program or not! "
      }
}, {
      "@type": "Question",
      "name": "If I choose to pay 1.5lacs instead of going for post program payment, can I still opt for EMI?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes. You can discuss this with your admissions counsellor to kickstart the process for you – once you get selected,that is."
      }
}, {
      "@type": "Question",
      "name": "After getting a job, how much time will I have to make the fee payment?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Once you secure a job offer, you’d have 2 options to make the fee payment. You can either choose to pay the entire fee in one go, the same has to be deposited within a week of receiving an offer. Or you can choose the EMI option, for which you’d be required to complete all the formalities with our NBFC partners within a week of receiving the job offer."
      }
}, {
      "@type": "Question",
      "name": "
Will my fee amount be determined based on my in-hand salary or CTC??",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "The fee which is 3 months of your salary will be determined on your CTC. Your final fees will be your 3 months salary + the registration fee that was paid at the start of the program."
      }
}, {
      "@type": "Question",
      "name": "Is there a registration fee associated with the program? Why?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Yes, if you get selected for the course, you need to pay Rs. 14,000 + GST as a registration fee. This ensures that students who go forward are committed to the process. Since there are limited seats available, we would hate for deserving candidates to not get an offer because someone else has erroneously blocked their seat. It is completely refundable in the following 2 situations –
– if you are unable to clear the program assessment OR if decide to opt out of the course within the first 4 weeks
– if you do not get a job with a minimum CTC of Rs. 4.5 lakhs within 12 months of program completion."
      }
}]
}
`;

```


**Inside the React Helmet Tag we are emebeding the Course and FAQ Snippt as a JSON inside <script> tags**

```javascript
      <Helmet>
      <meta charSet="utf-8" />
      <meta property="og:title" content={title} />
      <meta property="og:type" content="website" />
      <meta property="og:description" content={description} />
      <meta
        property="og:image"
        content="https://kraftshala.com/wp-content/uploads/2020/04/white_ArtboardKraftshala.png"
      />
      <meta property="og:url" content={url} />
      <title>{title}</title>
      <script type="application/ld+json">{courseSnipptJSON}</script>
      <script type="application/ld+json">{faqSnipptJSON}</script>
    </Helmet>

```





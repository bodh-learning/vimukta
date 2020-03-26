# *Vimuktā*

> Educate, Organise, Agitate.
> - [B R Ambedkar](https://en.wikipedia.org/wiki/B._R._Ambedkar)

> Education is Freedom.
> - [Paulo Freire](https://en.wikipedia.org/wiki/Paulo_Freire)

Vimuktā is a Sanskrit word which means liberated or freed. Vimuktā is a free addon for LifterLMS that allows Free, Open and Anonymous LifterLMS Courses. It provides a *Free Mode* that can be enabled and disabled on any course.

## What is Free Mode?

In the Free Mode, a Student can

 * Enroll into the course without registration and payment.
 * Enroll into the course completely anonymously, without providing any personal information.
 * Mark Lessons as Complete.</li><li>Attempt Quizzes and view Grades.
 * View overall progress, completion and grades.
 * Save progress and resume later at their convenience using a unique key.
 * [Planned/Future Versions] Register at any point and transfer all the existing progress to their account.</li></ul>

An Instructor can

 * Get overall aggregated reports of anonymous users.
 * [Planned/Future Versions] Get detailed reports for each anonymous user. </li><li>Grade anonymous quiz attempts.
  
> Free Mode does not disable the checkout process and Access Plans on the course, so your students could choose to register if you add an Access Plan, free or paid.

## A Quick Technical Introduction for Non-Technical Humans

On activation, Vimuktā creates a special new user (a bot) on your WordPress site with fine-tuned capabilities and permissions. When you activate Free Mode on a course, this bot user is automatically enrolled in the course.

When a visitor is takes the course, this bot user becomes the current user, without logging in or receiving any special privileges. Since, the bot is not logged in, the visitor stays a visitor and can't do anything else on your site that a logged in user can.

As far as LifterLMS is concerned, this bot is a proper student. In effect, the bot takes the course *on behalf of* visitors. So, all LifterLMS restrictions come off and an anonymous visitor can also attempt quizzes (via the bot).

At the same time, the visitor is anonymously identified through their [device's unique fingerprint](https://en.wikipedia.org/wiki/Device_fingerprint). This fingerprint is used to track completion of lessons and is associated with particular quiz attempts in a custom table.

## Effects on Reporting

As of now, the LifterLMS reports will show all this information as if a single user (the bot) has been attempting quizzes multiple times.  Since we've been bypassing completion, all lessons will stay incomplete (this) and the course progress will stay at 0%.

I'm working on changing that and in subsequent versions, you should be able to see more detailed reports. All the necessary data is available in the database, so whenever this feature is added, you'd be able to see back dated reports too.

Finally, in another planned feature, this bot will be excluded from regular reports so as to not pollute the existing reporting.

## Effects on Student Dashboard

Visitors won't have access to the dashboard and trying to access it will prompt them to login or register. This means that they can't see the courses they're enrolled in (My Courses). This also means that they can't see their grades or full progress report (My Grades).

In a subsequent version, custom screens will be added to display them.

## Resuming Courses and Cross-Device Tracking

Since Vimuktā tracks a visitors' device fingerprint, if a user returns to the course on the same device, progress can be resumed from where they left off.

At the same time, it provides a hashed key that the visitor can copy and use to maintain progress across devices. Without the key, there's no way to recognize that two devices belong to the same user.

In a future version, we'll add a form where visitors could enter their email address to send a custom access link (with the key) and a custom link to reports so that they can view them at any time. The email address will only be used to send the links and will not be stored anywhere (for full anonymity).

## Politics

This addon is a deeply political work that enables true and complete freedom in online learning and education.

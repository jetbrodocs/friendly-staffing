# Rohan's Working Notes on Friendly Staffing (2026-10-26)

Raw notes as written by Rohan on 2026-10-26, before the Q&A clarifications. Kept verbatim. Some points were later corrected (for example, pay rate and bill rate are hourly rates before deductions, and the promoter's name is Tejash Jain); see `10-observations/qa-2026-10-26-rohan-scope-clarifications.md`.

---

Here is a transcript of the meeting we had with the promoter of friendly-staffing in Canada, Tejas Chen. Right now in this transcript, he was accessing the meeting with another name, which is Priya Jain.

So here's my understanding so far: Tejas runs a recruitment firm in Canada. Majority of the employees or workers that get benefited out of this organization are looking for temporary work—mostly immigrants who, before they find a permanent job and after coming to Canada, might be looking for something that runs their house and makes them bread and butter. Having said that, 95% and above of his clients, employees, or workers are referral based; someone who's already worked with friendly-staffing may recommend his relatives, friends, or family to take on their services and probably take up a small job.

Now here's how it works: most of the employees or workers right now would fill out a small form about themselves, about their visa status, their capabilities, their past role, etc. And then based on that, they get saved in a database at friendly-staffing. friendly-staffing has two offices in Canada. Both of them right now are operating in silos, so the database that is in one of the locations is not accessed by the other location, right?

Simultaneously, when a client or an employer calls friendly-staffing, they look up their database and try to find candidates, employees, and workers in their database that might fit the role. Then an intimation is sent from their side to the employees for a potential role that is up for grabs—the pay, the location, etc. If everything is agreed on, then the employee details are shared with the employer, who can review it and then get a final understanding of who's going to arrive at their location and whether they're okay with that profile or not.

A separate timekeeping module is kept by the employers usually to address the timeliness as well as discipline of these employees and workers who have been working at their location. Most of the roles that come up from the employer side are temporary and small duration, though sometimes it can be large duration or long duration as well. Since they can attain services of multiple employers, the payment from the employers gets released to friendly-staffing on a weekly basis.

There are two types of rates: there's a bill rate and there's a pay rate. A pay rate is something that, after all deductions, is paid by friendly-staffing to the employees, and bill rate is something that gets paid by the client or employer to friendly-staffing based on all deductions. Typically they differ a little bit, and the difference is basically friendly-staffing's margin.

Now, the way we want to create an architecture for this system is:
* Give employees an ability to fill in forms for roles and their details, and other details, online via friendly-staffing's website, so they get validated and stored in a database accurately.
* Simultaneously, we also keep a track of which employees and workers we are sending out to which roles. This potentially helps us create relations between jobs and employees, eventually helping us in future recommendations.

Other details are present in the transcript that I've shared. Additionally, I'm going to share a summary that is created by Fathom as well.

From an employer's perspective, employers should be able to put in requests online and directly to friendly-staffing as well. friendly-staffing's team is responsible, or will be responsible, to monitor who we are recommending based on what and filter out the right candidates for a potential opening. Eventually, they'll be responsible for reaching out to these employees over WhatsApp, email, and SMS to make sure that the right people are shortlisted for the role, eventually selected for a particular role, and then those details are communicated with the employers who are going to attain the services of these employees.

Payroll management and timesheet management is also something that we are putting into the picture, and we're making sure that we have these features and functions available.


##########################################
Reusing Course Content
##########################################

EdX is a learning tool interoperability (LTI) tool provider. You can use this capability to present components from a course created in Studio in any campus or institutional system that is an LTI consumer. As a result, edX course content can be reused in contexts other than the edX LMS, including Canvas, Blackboard, and many other learning systems. 

Learners who use a campus-based learning system are presented with high quality edX content in the same context as their other learning experiences.

Typically, edX content appears in-frame on the page. This makes the edX content appear seamlessly in LMS

- Only the requested module will be shown
– No navigation or other clutter

Prerequisites

* Enrollment: You manage the course roster entirely on your campus system. You do not need to pre-register or pre-enroll learners on the edX system.

* Authentication: After initialization, learners who sign in to a campus system can access edX content. They do not need to navigate to a separate web site or sign in again.

* Grades: Learner responses to edX problems are graded by the edX platform and then automatically transferred to the campus system's gradebook. 
  
  The edX platform remembers each learner's' progress in the course material since their last visit.



Check with your system administrator [or partner manager] for information about how they have configured your Open edX implementation.

For example, your system administrator might direct you to use a different Studio website for the courses you want to 

courseware
including videos and problems, 


Benefits for Instructors & Institutions

* Instructors can harness the power and flexibility of edX to deliver high quality learning experiences while maintaining their use of campus systems in which rosters and grades are managed by the institution.



Benefits for Campus Learners

The student experience is streamlined and easy; 
edX course materials available within LMS course -- no need to navigate to edX Web site to register or enroll as a separate activity
All student state is preserved for LTI-linked materials -- students start, stop, resume work the same way they would if using the course materials directly from edX
Grades from edX assignments are shown in LMS in near real time





Use the LTI 1.1 standard to return a grade or completion




Assumption is that you are NOT using a live, active course — export the course, import with a new name to use a course that’s running now

we ignore course enrollment, start, and end dates, and “not visible to students”

but we do watch out for “unpublished” — the assumption is that such content just isn’t ready yet.

remove discussion boards





DevOps (from OPS-959):

Set ENABLE_LTI_PROVIDER to True
create a separate domain or microsite (to isolate LTI requests from regular LMS sessions)

The reason for this is that LTI supports anonymous usage by creating and logging in dynamically generated users for the purposes of displaying course content. If they are allowed to share session information with the regular site, then students using both the LTI content as well as the normal site would see themselves auto-logged in as a pseudo-anonymous user. 

Two types of user authentication

1.

2.


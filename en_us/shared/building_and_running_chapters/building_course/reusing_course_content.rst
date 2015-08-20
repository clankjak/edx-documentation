
##########################################
Reusing Course Content
##########################################

EdX is a learning tool interoperability (LTI) tool provider. You can use this
capability to present content from a course created in Studio in any system
that is an LTI consumer. As a result, you can reuse edX course content in
contexts other than the edX LMS, including courses in Canvas, Blackboard, and
other learning systems.

For learners who are already using another learning system, edX content, including advanced problem types and videos, is integrated into the familiar context seamlessly, typically in an IFrame on the page. Only the content, without repetitive navigation or other controls, appear. 
 

Prerequisites 

* Enrollment: You manage the course roster entirely on the remote learning
  system. You do not need to pre-register or pre-enroll learners separately in
  the edX LMS.

* Authentication: After initialization, learners who sign in to a campus system
  can access content from that system and from edX. Learners do not need to
  navigate to a different web site or sign in again.

* Grades: Learner responses to edX problem components are graded by the edX
  platform and then transferred automatically to the campus system's gradebook.

  Each learner's progress in through the edX content is saved. Learners can
  start, stop, and resume work in the remote learning system in the same way
  that they would in the edX LMS.


Check with your system administrator [or partner manager] for information about how they have configured your Open edX implementation.

For example, your system administrator might direct you to use a different Studio website for the courses you want to 




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


To include the content of an existing course in another system, course teams   use the LMS to view data about the XBlock they want to include. 

They will use a link (like) Staff Debug to get the URL of the specific component, unit, or subsection, and then paste that URL into the course on the receiving (Blackboard or Canvas, tool consumer) side.

- everything contained within the selected course element is included (can select a single video, but can't include an entire unit except for one video)
- there is currently an issue with grading, which would require each graded problem to be added individually. Grade aggregation may be resolved by eoAugust, AND they can still view everything in the TC, even if grades don’t go over.
- Users viewing the content in an external system are not enrolled in the course, they do not belong to a cohort. 
- grade transfer is near-ish real time, not instantaneous. We can recover from link failure (state is retained, will need to do some manual fixup)



DevOps (from OPS-959):

Set ENABLE_LTI_PROVIDER to True
create a separate domain or microsite (to isolate LTI requests from regular LMS sessions)

The reason for this is that LTI supports anonymous usage by creating and logging in dynamically generated users for the purposes of displaying course content. If they are allowed to share session information with the regular site, then students using both the LTI content as well as the normal site would see themselves auto-logged in as a pseudo-anonymous user. 

Two types of user authentication

1.

2.


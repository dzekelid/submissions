---
swagger: "2.0"
x-collection-name: Instructure
x-complete: 0
info:
  title: Instructure Canvas Courses API Submit captured events
  description: Submit captured events.
  termsOfService: https://www.canvaslms.com/policies/api-policy
  version: v1
host: canvas.instructure.com
basePath: /api/v1
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /courses/{course_id}/assignments/assignment_id/submissions:
    get:
      summary: List assignment submissions
      description: List assignment submissions.
      operationId: list-assignment-submissions
      x-api-path-slug: coursescourse-idassignmentsassignment-idsubmissions-get
      parameters:
      - in: query
        name: grouped
        description: If this argument is true, the response will be grouped by student
          groups
      - in: query
        name: include[]
        description: Associations to include with the group
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
      - Submissions
    post:
      summary: Submit an assignment
      description: Submit an assignment.
      operationId: submit-an-assignment
      x-api-path-slug: coursescourse-idassignmentsassignment-idsubmissions-post
      parameters:
      - in: query
        name: comment[text_comment]
        description: Include a textual comment with the submission
      - in: query
        name: submission[body]
        description: Submit the assignment as an HTML document snippet
      - in: query
        name: submission[file_ids][]
        description: Submit the assignment as a set of one or more previously uploaded
          filesnresiding in the submitting user&#39;s files section (or the group&#39;snfiles
          section, for group assignments)
      - in: query
        name: submission[media_comment_id]
        description: The media comment id to submit
      - in: query
        name: submission[media_comment_type]
        description: The type of media comment being submitted
      - in: query
        name: submission[submission_type]
        description: The type of submission being made
      - in: query
        name: submission[url]
        description: Submit the assignment as a URL
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
      - Submissions
  /courses/{course_id}/assignments/assignment_id/submissions/update_grades:
    post:
      summary: Grade or comment on multiple submissions
      description: Grade or comment on multiple submissions.
      operationId: grade-or-comment-on-multiple-submissions
      x-api-path-slug: coursescourse-idassignmentsassignment-idsubmissionsupdate-grades-post
      parameters:
      - in: query
        name: grade_data[student_id][file_ids][]
        description: See documentation for the comment[] arguments in thenSubmissions
          Update documentation
      - in: query
        name: grade_data[student_id][group_comment]
        description: no description
      - in: query
        name: grade_data[student_id][media_comment_id]
        description: no description
      - in: query
        name: grade_data[student_id][media_comment_type]
        description: 'no descriptionnn        n        n          Allowed values:
          audio, video'
      - in: query
        name: grade_data[student_id][posted_grade]
        description: See documentation for the posted_grade argument in thenSubmissions
          Update documentation
      - in: query
        name: grade_data[student_id][rubric_assessment]
        description: See documentation for the rubric_assessment argument in thenSubmissions
          Update documentation
      - in: query
        name: grade_data[student_id][text_comment]
        description: no description
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
      - Submissions
      - Update
      - Grades
  /courses/{course_id}/assignments/assignment_id/submissions/{submission_id}/peer_reviews:
    delete:
      summary: Create Peer Review
      description: Create peer review.
      operationId: create-peer-review
      x-api-path-slug: coursescourse-idassignmentsassignment-idsubmissionssubmission-idpeer-reviews-delete
      parameters:
      - in: query
        name: user_id
        description: user_id to delete as reviewer on this assignment
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
      - Submissions
      - Submission
      - Id
      - Peer
      - Reviews
    get:
      summary: Get all Peer Reviews
      description: Get all peer reviews.
      operationId: get-all-peer-reviews
      x-api-path-slug: coursescourse-idassignmentsassignment-idsubmissionssubmission-idpeer-reviews-get
      parameters:
      - in: query
        name: include[]
        description: Associations to include with the peer review
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
      - Submissions
      - Submission
      - Id
      - Peer
      - Reviews
    post:
      summary: Create Peer Review
      description: Create peer review.
      operationId: create-peer-review
      x-api-path-slug: coursescourse-idassignmentsassignment-idsubmissionssubmission-idpeer-reviews-post
      parameters:
      - in: query
        name: user_id
        description: user_id to assign as reviewer on this assignment
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
      - Submissions
      - Submission
      - Id
      - Peer
      - Reviews
  /courses/{course_id}/assignments/assignment_id/submissions/{user_id}:
    get:
      summary: Get a single submission
      description: Get a single submission.
      operationId: get-a-single-submission
      x-api-path-slug: coursescourse-idassignmentsassignment-idsubmissionsuser-id-get
      parameters:
      - in: query
        name: include[]
        description: Associations to include with the group
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
      - Submissions
      - User
      - Id
    put:
      summary: Grade or comment on a submission
      description: Grade or comment on a submission.
      operationId: grade-or-comment-on-a-submission
      x-api-path-slug: coursescourse-idassignmentsassignment-idsubmissionsuser-id-put
      parameters:
      - in: query
        name: comment[file_ids][]
        description: Attach files to this comment that were previously uploaded using
          thenSubmission Comment API&#39;s files action
      - in: query
        name: comment[group_comment]
        description: Whether or not this comment should be sent to the entire group
          (defaults tonfalse)
      - in: query
        name: comment[media_comment_id]
        description: Add an audio/video comment to the submission
      - in: query
        name: comment[media_comment_type]
        description: The type of media comment being added
      - in: query
        name: comment[text_comment]
        description: Add a textual comment to the submission
      - in: query
        name: include[visibility]
        description: Whether this assignment is visible to the owner of the submission
      - in: query
        name: rubric_assessment
        description: Assign a rubric assessment to this assignment submission
      - in: query
        name: submission[excuse]
        description: Sets the u201cexcusedu201d status of an assignment
      - in: query
        name: submission[posted_grade]
        description: Assign a score to the submission, updating both the u201cscoreu201d
          and u201cgradeu201dnfields on the submission record
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
      - Submissions
      - User
      - Id
  /courses/{course_id}/assignments/assignment_id/submissions/{user_id}/comments/files:
    post:
      summary: Upload a file
      description: Upload a file.
      operationId: upload-a-file
      x-api-path-slug: coursescourse-idassignmentsassignment-idsubmissionsuser-idcommentsfiles-post
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
      - Submissions
      - User
      - Id
      - Comments
      - Files
  /courses/{course_id}/assignments/assignment_id/submissions/{user_id}/files:
    post:
      summary: Upload a file
      description: Upload a file.
      operationId: upload-a-file
      x-api-path-slug: coursescourse-idassignmentsassignment-idsubmissionsuser-idfiles-post
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
      - Submissions
      - User
      - Id
      - Files
  /courses/{course_id}/assignments/assignment_id/submissions/{user_id}/read:
    delete:
      summary: Mark submission as unread
      description: Mark submission as unread.
      operationId: mark-submission-as-unread
      x-api-path-slug: coursescourse-idassignmentsassignment-idsubmissionsuser-idread-delete
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
      - Submissions
      - User
      - Id
      - Read
    put:
      summary: Mark submission as read
      description: Mark submission as read.
      operationId: mark-submission-as-read
      x-api-path-slug: coursescourse-idassignmentsassignment-idsubmissionsuser-idread-put
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Assignments
      - Assignment
      - Id
      - Submissions
      - User
      - Id
      - Read
  /courses/{course_id}/gradebook_history/date/graders/{grader_id}/assignments/assignment_id/submissions:
    get:
      summary: Lists submissions
      description: Lists submissions.
      operationId: lists-submissions
      x-api-path-slug: coursescourse-idgradebook-historydategradersgrader-idassignmentsassignment-idsubmissions-get
      parameters:
      - in: query
        name: assignment_id
        description: The ID of the assignment for which you want to see submissions
      - in: query
        name: course_id
        description: The id of the contextual course for this API call
      - in: query
        name: date
        description: The date for which you would like to see submissions
      - in: query
        name: grader_id
        description: The ID of the grader for which you want to see submissions
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Gradebook
      - History
      - Date
      - Graders
      - Grader
      - Id
      - Assignments
      - Assignment
      - Id
      - Submissions
  /courses/{course_id}/quizzes/quiz_id/submissions:
    get:
      summary: Get all quiz submissions.
      description: Get all quiz submissions..
      operationId: get-all-quiz-submissions
      x-api-path-slug: coursescourse-idquizzesquiz-idsubmissions-get
      parameters:
      - in: query
        name: include[]
        description: Associations to include with the quiz submission
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Quizzes
      - Quiz
      - Id
      - Submissions
    post:
      summary: Create the quiz submission (start a quiz-taking session)
      description: Create the quiz submission (start a quiz-taking session).
      operationId: create-the-quiz-submission-start-a-quiztaking-session
      x-api-path-slug: coursescourse-idquizzesquiz-idsubmissions-post
      parameters:
      - in: query
        name: access_code
        description: Access code for the Quiz, if any
      - in: query
        name: preview
        description: Whether this should be a preview QuizSubmission and not count
          towards thenuser&#39;s course record
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Quizzes
      - Quiz
      - Id
      - Submissions
  /courses/{course_id}/quizzes/quiz_id/submissions/self/files:
    post:
      summary: Upload a file
      description: Upload a file.
      operationId: upload-a-file
      x-api-path-slug: coursescourse-idquizzesquiz-idsubmissionsselffiles-post
      parameters:
      - in: query
        name: name
        description: The name of the quiz submission file
      - in: query
        name: on_duplicate
        description: How to handle duplicate names
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Quizzes
      - Quiz
      - Id
      - Submissions
      - Self
      - Files
  /courses/{course_id}/quizzes/quiz_id/submissions/{id}:
    get:
      summary: Get a single quiz submission.
      description: Get a single quiz submission..
      operationId: get-a-single-quiz-submission
      x-api-path-slug: coursescourse-idquizzesquiz-idsubmissionsid-get
      parameters:
      - in: query
        name: include[]
        description: Associations to include with the quiz submission
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Quizzes
      - Quiz
      - Id
      - Submissions
      - Id
    put:
      summary: Update student question scores and comments.
      description: Update student question scores and comments..
      operationId: update-student-question-scores-and-comments
      x-api-path-slug: coursescourse-idquizzesquiz-idsubmissionsid-put
      parameters:
      - in: query
        name: attempt
        description: The attempt number of the quiz submission that should be updated
      - in: query
        name: fudge_points
        description: Amount of positive or negative points to fudge the total score
          by
      - in: query
        name: questions
        description: A set of scores and comments for each question answered by the
          student
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Quizzes
      - Quiz
      - Id
      - Submissions
      - Id
  /courses/{course_id}/quizzes/quiz_id/submissions/{id}/complete:
    post:
      summary: Complete the quiz submission (turn it in).
      description: Complete the quiz submission (turn it in)..
      operationId: complete-the-quiz-submission-turn-it-in
      x-api-path-slug: coursescourse-idquizzesquiz-idsubmissionsidcomplete-post
      parameters:
      - in: query
        name: access_code
        description: Access code for the Quiz, if any
      - in: query
        name: attempt
        description: The attempt number of the quiz submission that should be completed
      - in: query
        name: validation_token
        description: The unique validation token you received when this Quiz Submission
          wasncreated
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Quizzes
      - Quiz
      - Id
      - Submissions
      - Id
      - Complete
  /courses/{course_id}/quizzes/quiz_id/submissions/{id}/events:
    get:
      summary: Retrieve captured events
      description: Retrieve captured events.
      operationId: retrieve-captured-events
      x-api-path-slug: coursescourse-idquizzesquiz-idsubmissionsidevents-get
      parameters:
      - in: query
        name: attempt
        description: The specific submission attempt to look up the events for
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Quizzes
      - Quiz
      - Id
      - Submissions
      - Id
      - Events
    post:
      summary: Submit captured events
      description: Submit captured events.
      operationId: submit-captured-events
      x-api-path-slug: coursescourse-idquizzesquiz-idsubmissionsidevents-post
      parameters:
      - in: query
        name: quiz_submission_events[]
        description: The submission events to be recorded
      responses:
        200:
          description: OK
      tags:
      - Courses
      - Course
      - Id
      - Quizzes
      - Quiz
      - Id
      - Submissions
      - Id
      - Events
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---


## Team

TEAM-NAME: MRI-Team-PPS

MEMBER-LABELS: Mark Ijeoma Precious, Awal Salamatu Junior, Kamanu Prosper Ugonna

TEAM-WORK: Member1 runs the first command and edits the brief, Member2 reviews the project-boundary decisions, and Member3 reviews the risk and testable behaviour. The team rotates who controls the keyboard after the first check, and any problem that stops progress is reported to the whole team before continuing.

## Fixed Course Facts

- The project is a brain-MRI object-detection workflow.
- The input is one RGB brain-MRI image.
- The provided dataset annotates regions as `glioma`, `meningioma`, or `pituitary`. A `notumor` image is a valid negative example with no boxes.
- The result is zero or more labeled boxes for human review.
- This is non-clinical coursework and not a diagnosis.
- The full dataset is introduced in Lab 04. Do not download it for Lab 01.

These are supplied facts, not questions. Do not rewrite them.

## Project Boundary

SYSTEM-DOES: The workflow receives one RGB brain-MRI image, performs object detection for regions annotated as glioma, meningioma, or pituitary, and returns zero or more labeled bounding boxes for human review.

SYSTEM-DOES-NOT: The workflow does not diagnose a brain tumor or authorize any automatic medical treatment, diagnosis, or other clinical decision.

REVIEWER: A designated human reviewer receives and reviews every model output before the result is considered further.

## Risk And Testable Behaviour

RISK: The workflow could incorrectly place a bounding box on a normal region of a brain-MRI image and label it as one of the tumor categories.

RESPONSE: Every result is sent to the designated human reviewer, who can identify and reject an incorrect box, and no model output triggers an automatic medical action.

TESTABLE-BEHAVIOUR: Given a valid `notumor` brain-MRI image with no annotated tumor boxes, When the workflow processes the image, Then it can return zero labeled boxes and the result is still sent for human review.

## Initial Contributions

INITIAL-CONTRIBUTIONS: Member1 ran the start command and entered the first draft of the brief; Member2 checked the project boundary and non-clinical wording; Member3 drafted and checked the risk, response, and testable behaviour.
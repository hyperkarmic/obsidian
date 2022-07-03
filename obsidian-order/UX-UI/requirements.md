# requirements
Put simply, a requirement is a single statement that describes a necessary system property, feature, characterization, or usage. While user needs and user stories are written from the perspective of the user and in the language of the user, requirements should be written from the perspective and in the language of the engineer. They are intended to specify "what" the system needs to do in order to meed the needs of stakeholders. They should be stated in quantitative language that can be objectively measured and tested.

A user need may state;

_"The user needs the product to support the ability of performing payment transfers to partner devices."_

Which may lead to some requirements like;

_"The product shall support BLE communications for version 4.0 and beyond."_

_"The product shall provide controls for users to select which device to send a payment to."_

It is important to keep in mind that when creating a requirement it is something the system _must_ do in order to meet its intended use, and it is something the team _must_ test.

### Requirement Syntax
Using a structured syntax when writing requirements will create consistency and improve the review process. Using a framework can also help simplify the process of thinking about requirements. One key part included in every requirement is _shall_. If it states _shall_ then it must be done. Alternatively, _should_ can be used in the event of a suggestion or recommendation. The following is a good structure to work within:

[**Noun**] _shall_ [**Action Verb**] [**Description**] and/or [**Conditions**]

-   **Noun** - the product being developed or addressed in the requirement
-   **Action Verb** - the action the product will perform
-   **Description** - Describes in more detail about who, what, and where the product will perform this action
-   **Conditions** - Describes the conditions under which the action will take place

### Negative Requirements

I want to briefly touch on negative requirements as these can be more common than you would imagine. Negative requirements should not be written as a general rule of thumb. The burden of proof for a negative requirement is far greater, more difficult, and may be impossible. Alternatively, stating the functionality of the system in the positive form; inhibit, perform, or prevent, is a better strategy.

**Negative requirement examples:**

-   The device software shall not fail.
-   The software shall not allow database calls when a non-recoverable error is present.

**Positive requirement examples:**

-   The device software shall allow for 96 hours of continuous operation.
-   The software shall inhibit database calls after the occurrence of a non-recoverable error.

### Requirements of Requirements



The irony, there are requirements for writing a requirement.

Requirements should be unambiguous, verifiable, complete, and non-conflicting. While some aspects of writing a requirement are flexible these four are fundamental and if not met then you have broken requirements.

Everybody likes a checklist right!? If there is one thing you take with you from this post, it should be this checklist.

-   Unambiguous, the requirement is concise, consistent and correct. Only one interpretation is possible.
-   Verifiable, objectively verifiable whether it be through [inspection, demonstration, analysis, or testing](https://www.modernanalyst.com/Careers/InterviewQuestions/tabid/128/ID/1168/What-are-the-four-fundamental-methods-of-requirement-verification.aspx).
-   Complete, fully stated in one place and there is no missing information.
-   Non-conflicting, it doesn't contradict another requirement, it is possible to satisfy all requirements.
-   Attainable, or technically feasible, and can be achieved with existing design concepts.
-   Rationale provided with reasoning for the need, the assumptions, and relevant design decisions.
-   Necessary, if removed a deficiency in the system would occur.
-   Implementation free and states "what" and not "how".
-   If possible, traced to a higher level user need or requirement (standards, regulation, interface, etc.).

![[requirements.jpg]]
#requirements
#ux #UX 
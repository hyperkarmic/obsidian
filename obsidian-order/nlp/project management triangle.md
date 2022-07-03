# project management triangle

# Software “Virtues”

You may be familiar with the [Project Management Triangle](https://en.wikipedia.org/wiki/Project_management_triangle), where the quality of work is determined by the deadlines, scope, and budget. Any modification to one of those requires a reassessment of the other two. Engineers also have their iron triangle, and frequently repeat the mantra, “faster, better, cheaper: choose two.” In reality, it is more flexible but there are clear tradeoffs and a natural tension between them. It would be nice if software development was as simple as teasing out our priorities using just three parameters.

> “The Project Management Triangle is clearly insufficient as a model of project success because it omits crucial dimensions of success including impact on stakeholders, learning, and user satisfaction.” — Wikipedia, [Project Management Triangle](https://en.wikipedia.org/wiki/Project_management_triangle)

![](https://miro.medium.com/max/1400/0*cUCuz_Z6gJqIOIiL)

[Samuel Zeller](https://unsplash.com/@samuelzeller?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

So what are some priorities that compete in software development that need to be assessed for teams, projects, and phases of a project? Think of these as the “virtues” of software. They are also known as [System Quality Attributes](https://en.wikipedia.org/wiki/List_of_system_quality_attributes). Here are some that should be considered. Not all of them are immediately apparent or represented without careful thought. There are others that should also be on the list but these are the ones commonly competing. When looking at the full list [here](https://en.wikipedia.org/wiki/List_of_system_quality_attributes), consider how they may be grouped together or nested as secondary virtues.

## Virtues

-   **Usability/Simplicity** — Can the software be used by the user to accomplish their needs?
-   **Originality/Innovation** — Does the project have a differentiation from other software?
-   **Stability/Reliability** — Is the software stable and reliable?
-   **Urgency/Timeliness** — Will the software be delivered in time?
-   **Efficiency/Scalability** — How fast can the software perform under load?
-   **Maintainability/Manageability** — Can the project be continued by a new team?
-   **Versatility/Adaptability** — How narrow is the use case and can it be used for similar tasks?
-   **Interoperability** — How much effort is required for the user’s data to be used with related software? The reverse?
-   **Affordability/Sustainability** — Can the user afford the software? Is the cost of delivering the software sustainable?
-   **_Reality_** — How realistic are the goals of this software?

Not all virtues are directly applicable for each project. Others may be missing and need to be added. For example financial software highly values [auditability](https://en.wikipedia.org/wiki/Auditability). Software for power users will likely prioritize [customizability](https://en.wiktionary.org/wiki/customizability). Developers, engineers, and architects have concerns that need to be further prioritized, such as debugability, [deployability](https://en.wiktionary.org/wiki/deployability), [extensibility](https://en.wikipedia.org/wiki/Extensibility), [recoverability](https://en.wiktionary.org/wiki/recoverability), [securability](https://en.wiktionary.org/wiki/securability), [testability](https://en.wikipedia.org/wiki/Testability). Some are completely ignored purposely depending on the phase. Many of them have natural enemies and careful consideration should be taken to balancing them. Some of them even have subcomponents that can be further prioritized. These secondary virtues may be assessed by the development team once they understand the primary virtues.

![](https://miro.medium.com/max/1400/0*PnASm4lyFzVvOSvA)

[Ron McClenny](https://unsplash.com/@ronmcclenny?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

## Usability/Simplicity

[Usability](https://en.wikipedia.org/wiki/Usability) of software is directly tied to the effectiveness of the user’s ability to use the software. Manuals and walkthroughs help address gaps in usability but greatly compromise maintainability. Intuitive interfaces address the root issue. Keeping the software as simple as possible helps remove unnecessary complexity. Learnability can be described as the difficulty for a user to learn the software and can be coerced as a secondary virtue. It can also refer to the software itself learning.

The natural enemies of usability are originality, urgency, and versatility. New innovative features are rarely understood enough to be simplified and showcase a natural tension between these virtues. Urgency leads to rushing or even skipping user testing. Versatility invites ambiguity that may undermine intuitiveness.

Usability should gain a higher priority as the project matures.

![](https://miro.medium.com/max/1400/0*ZQ1oNpTfdQ6KBKh0)

[Eddie Kopp](https://unsplash.com/@fiveohfilms?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

## Originality/Innovation

Innovation in software can sometimes steal the limelight and temptingly overshadow other virtues. Original ideas are how most projects start and make it easier to sell the project to investors. These new approaches are usually what gives the projects their intrinsic value.

The natural enemies of originality are usability and stability. Many times usability and stability suffer at first but as the approach is tested and usage is studied, both can be improved.

Innovation’s priority typically declines as the project matures. This does not mean that the project can no longer be innovative but each new innovative functionality should repeat the process.

![](https://miro.medium.com/max/1400/0*DxMHuIEezlBWUmCx)

[Luca Bravo](https://unsplash.com/@lucabravo?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

## Stability/Reliability

[Stability](https://en.wikipedia.org/wiki/Stability_Model) covers the typical freezes and crashes associated with software bugs. Reliability is associated with the ability to recover without the loss of data. These may be treated as one or as two primary virtues depending on the need. There may be times where reliability is mandatory but crashes are acceptable.

Stability’s natural enemies are urgency and originality. Rushing something out of the door increases the chances for bugs. New innovative approaches are inherently less tested in the real world and consequences are unknown.

The priority of stability has a direct relationship to the maturity of the project. Expecting stability and reliability in a proof of concept or alpha release is unrealistic. It pulls a lot more weight in a prototype or beta release but is expected to be mandatory in a production release. This is why patch releases happen so quickly after a major release.

![](https://miro.medium.com/max/1400/0*4EGnMMKDXTt4LvYM)

[Karen Lau](https://unsplash.com/@pic_parlance?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

## Urgency/Timeliness

[Urgency](https://en.wikipedia.org/wiki/Timeliness) ensures that the project is delivered in time to meet the users need before they solve their issues another way. In production software, the tyranny of the urgent needs to be kept in check. In preproduction software, it may not be prioritized enough. Some users cannot wait for releases and move ahead on a similar path that might not be parallel. This can lead to more work of interoperability if they choose other software in their workflow. Rushing to meet their timeline may sacrifice other priorities. Harness the missed opportunity to study the use case to help a future user base.

Urgency’s natural enemies are maintainability, efficiency, and usability. Rushing leaves little to no time for ensuring that code is either maintainable or efficient. User testing also takes time and may lead to redesign.

The priority of urgency prevails throughout all phases but typically increases as the project matures. Unsurprisingly, there always seems to be more time available at the start of a project.

![](https://miro.medium.com/max/1400/0*dug8YV6Z4JZSL1dQ)

[imgix](https://unsplash.com/@imgix?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

## Efficiency/Scalability

[Efficiency](https://en.wiktionary.org/wiki/efficiency) can keep hardware costs down as more work can be done on less hardware. As long as the software performs at a pace that keeps up with users development time is wasted on optimization. Efficiency is a never-ending quest. There are always ways to increase performance and architect a better solution. This is what many developers value most. [Scalability](https://en.wikipedia.org/wiki/Scalability) is a form of efficiency under changing load and can prevent wasted hardware resources from going idle while not under load. [Serverless computing](https://en.wikipedia.org/wiki/Serverless_computing) is a great example of this. It is easy to think this is only a concern of developers and engineers but needs to be prioritized by all stakeholders.

Efficiency’s natural enemies are urgency, maintainability, and versatility. Many times refactors sacrifice one or two of these.

The priority of efficiency should be assessed when the performance impedes the user. Rarely is it a priority in the early phases and usually the highest priority once all other major issues are addressed.

![](https://miro.medium.com/max/1400/0*xa1erZrhWR035lN1)

[rawpixel](https://unsplash.com/@rawpixel?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

## Maintainability/Manageability

[Maintainability](https://en.wikipedia.org/wiki/Maintainability) is widely underappreciated and covers a wide gamut of secondary virtues. This can include code understandability, modularity, testability, and hire-ability, among others. Primarily this focuses on the project transcending a few contributors holding the keys to the project. This also affects the ability to add more team members to the same project. Understandability allows other developers to quickly read and intuitively know what the code does and how to work with it. Modularity allows more parts of the project to be worked on simultaneously as well as reuse of code. Testability can help verify that the existing code acts as intended and ensures future changes are less likely to break previously working code. Hire-ability is assessing how likely your choices affect finding a qualified developer to work on this project. Avoid obscure languages and frameworks unless the use case demands it.

The natural enemies of maintainability are urgency and efficiency. Rushing to get features out the door or obsessing over performance typically trap a project from achieving long-term maintainability. Technical debt is a common side effect of not prioritizing this virtue.

Placing a priority on this early on a project slows the natural progression and increases waste. As a project matures it’s maintainability should increase.

![](https://miro.medium.com/max/1400/0*gBV-N0CHHlhDpehf)

[Paul Felberbauer](https://unsplash.com/@servuspaul?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

## Adaptability/Versatility

[Adaptability](https://en.wikipedia.org/wiki/Adaptation_(computer_science)) is the ability to adapt or be adapted to multiple use cases. There is a balance to applying this versatility. Attempting to make software that is too versatile can reduce its effectiveness for any single use case. Designing software workflows to handle too few use cases limit the usability in related use cases. Studying related use cases help identify areas of natural versatility without sacrificing focus or effectiveness.

The natural enemies of versatility are usability and efficiency. The more a usability workflow and code efficiency are optimized for a particular use case the less versatile it becomes.

The priority of versatility typically increases as the project matures. Applying this too early and it makes the project lack focus. Sometimes but rarely versatility is reduced to limit applicable use cases unless it was to provide needed focus.

![](https://miro.medium.com/max/1400/0*T1s7APZTxBpL35aB)

[Ed Derrico](https://unsplash.com/@edderrico?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

## Interoperability

[Interoperability](https://en.wikipedia.org/wiki/Interoperability) is the ability to import, export, and use data between separate software systems. This can increase applicable use cases and market share for users that already rely on or would like to integrate other related software in their workflow.

The natural enemies of interoperability are originality and urgency. Innovation can be stifled if too much focus is placed on interoperability. Rushing to meet deadlines can sometimes lead to skipping the study and integration of existing standards.

The priority of interoperability should be considered throughout all phases of the software development but will naturally increase as the project matures.

![](https://miro.medium.com/max/1400/0*8APoOOYPoPJfAVZO)

[rawpixel](https://unsplash.com/@rawpixel?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

## Affordability/Sustainability

[Affordability](https://en.wiktionary.org/wiki/affordability) is addressed from two angles. The price of the software to the user and the development team. [Sustainability](https://en.wikipedia.org/wiki/Sustainability) is the intersection of the two. If a team can not afford to deliver the software from the income of the software, they must fund the project by another means. This is common in open source software and can be done in different ways. Assessing the costs ensures pet projects are kept in check and that each project’s invested effort is proportionate to the vision and mission of the team.

Affordability’s natural enemies are nearly every other virtue as they each incur a cost. Theoretically, they should pay off once implemented. Usability testing reduces support costs and should grow a user base. Efficiency keeps hardware costs down. Maintainability reduces technical debt. Other priorities are kept in check by their return on investment with sustainability in mind.

The priority of affordability should be underlying every other virtue and keep them in check.

![](https://miro.medium.com/max/1400/0*nOA-kL2kh0DUKbaC)

[Guilherme Stecanella](https://unsplash.com/@guilhermestecanella?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

# Reality Assessment

All of the above virtues have to be balanced with reality. Some problems just take time to solve especially to accomplish it in a stable way. Since software development takes time it also costs money. Inexperienced users may take time to learn a new piece of software and initial usability testing might be misleading. Choosing the wrong userbase during testing may lead to ineffective software for the intended users. Is it realistic to or advantageous to focus on interoperability? Does this project really need maintainability or is it a small enough scope to rewrite it if there is no one who can maintain it? Reality helps ensure costs are assessed and that there is enough budgeted to complete the project.

-   Costs (effort and resources)
-   Benefits (advantages of success)
-   Risks (probability of failure)
-   Dependencies (requirements)
-   Penalties (consequences of not)
-   Compliance (regulatory requirements)

The natural enemies of reality are originality, versatility, and urgency. Sometimes innovation purposefully ignores known realities to address what is thought of as impossible. Many times it is unrealistic to achieve broad versatility. Chasing the tyranny of the urgent can ignore realistic timelines to deliver a stable product.

The priority of reality should be balanced and help keep everything in check. Placing too high of a priority on perceived realities can stifle innovation and delay timelines. Not placing a high enough priority is unsustainable.

# Prioritizing Virtues

Each team member holds different values it is important for the team to collaborate and agree on the aggregate values of the team. Prioritization should be repeated for each project and again at new milestones such as [promoting from one phase of development to another](https://medium.com/@klappy/lean-expectations-poc-prototype-mvp-140749383fd4).

![](https://miro.medium.com/max/1400/0*21xGLVEqZAQvq76H)

[Nikolay Vorobyev](https://unsplash.com/@nikolayv?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com/?utm_source=medium&utm_medium=referral)

One simple approach to sorting the virtues for a team, project, and phase is the [MoSCoW method](https://en.wikipedia.org/wiki/MoSCoW_method). Allow everyone to label each virtue as Must (mandatory), Should (high priority), Could (preferred but not necessary), or Would (can be postponed). Associate a point value of 4, 3, 2, and 1 respectively. Once everyone has labeled them, sort them by the most points and assess if they properly reflect the necessary values. Take time to discuss the order and if adjustments need to be made, repeat the process until a consensus is found. Sometimes anomalies occur and everyone can agree on manual order adjustments.

There are [other approaches to prioritizing](https://apiumhub.com/tech-blog-barcelona/software-requirements-prioritization-techniques/) such as the Hundred Dollar Method where everyone gets a fictitious $100 to spend on each virtue. This one is simple and helps reduce indecision and lengthy debates. It also prevents sticky notes from falling off the wall from being moved too many times. A simple [Google Form](https://docs.google.com/forms/d/e/1FAIpQLSe_-X7SVHCavwfGYMmZvcnr0Pn6Xf1hCy2mewmrdmCM8fS0BQ/viewform) can be created to list each virtue with the options of MoSCoW as a linear scale of 1 (would) to 4 (must). Using Google Sheets to sum the values of the entries and sort the virtues by totals should also be a straightforward task.

Once these Software “Virtues” are set, there may be less need for prioritizing individual features in a lengthy assessment because this acts as a lens to naturally sort them. Then realities such as cost, benefit, risk, dependency, penalty, and compliance can take over.

# Summary

To be able to prioritize the virtues of software, we first had to understand where to apply them, what they are, and how to assess and sort them. Knowing where to apply them gives us context since that can be unique to each team, project, and phase of each project. While there are many software virtues, it is important to focus on which ones are applicable to the project. Many of them have a natural tension with each other. Reality is what keeps the virtues in check. Assessing the software virtues in able to sort them can be an arduous task for any team. There are a few to try and should help the team to come to a consensus.

[Some rights reserved](https://creativecommons.org/licenses/by-sa/4.0/)

[Project management triangle - Wikipedia](https://en.wikipedia.org/wiki/Project_management_triangle)

#nlp #project-management-triangle
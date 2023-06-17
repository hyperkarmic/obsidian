# clean architecture
Clean Architecture, is architectural pattern manifested into this world by non other than Uncle Bob([Robert C. Martin)](https://en.wikipedia.org/wiki/Robert_C._Martin). The rings represent each layer of an application, the outermost layers are systems/frameworks of an application, whereas, the inner circles are rules, and policies of an application. The pattern follows the dependence rule, which states that:

> Source code dependencies should point inwards

Which, means foreach outer layer, each outer layer should only reference the closest most inner layer to itself, whereas foreach inner layer, each inner layer should not reference/know anything in any other outer layer, which would include anything from functions, classes and variables or any other data structures.

-   **Entities** - these are core business objects and logic, they contain rules & policies of an application. These can be models, functions or classes.
-   **Use Cases** - these allow for the traversal of data from the Entities to Controllers, Gateways or Presenters.
-   **Interface Adapters** - these convert data most useful to for entities and use-cases to data most convenient to next layer.
-   **UI, External Interfaces, DB, Web, Devices** - this layer includes frameworks/databases. In this layer, you write code that connects to UI frameworks and databases, this code is kept in the outermost layer to ensure that you can change UI and databases and have you application perform as intended.

### Why Clean Architecture

-   **Platform agnostic** - meaning, this architectural pattern is not specific to any platform for which you want to build an application whether it be Android, iOS, Web and even console applications.
-   **Independent of UI** - meaning, you can easily replace our UI layer, commonly called the Presentation layer in mobile development with any type of UI framework. So, you can switch out your presentation layer frameworks i.e. XML to Jetpack Compose on Android, UIKit to SwiftUI on iOS, vice-versa and have your application work the same because your core business logic doesn’t change.
-   **Testability** - meaning, you can easily test your core business logic since it's separated out and knows nothing of the UI, database or server.
-   **Independent of database** - meaning, you can easily replace our data layer, any type of database to cache your data or any type of networking library to fetch your data.
***
![[clean-arch.jpg]]
***

![[clean-architecture.webp]]



#bob-martin #clean-architecture #architecture
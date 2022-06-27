# The Extensible Web Manifesto

## #extendthewebforward

---

We—[the undersigned](https://extensiblewebmanifesto.org/#signatories)—want to change how web standards committees create and prioritize new features. We believe that this is critical to the long-term health of the web.

We aim to tighten the feedback loop between the editors of web standards and web developers.

Today, most new features require months or years of standardization, followed by careful implementation by browser vendors, only then followed by developer feedback and iteration. We prefer to enable feature development and iteration in JavaScript, followed by implementation in browsers and standardization.

To enable libraries to do more, browser vendors should provide new low-level capabilities that expose the possibilities of the underlying platform as closely as possible.

They should also seed the discussion of high-level APIs through JavaScript implementations of new features (such as [Mozilla’s X-Tags](http://www.x-tags.org/) and [Google’s Polymer](http://www.polymer-project.org/)).

---

Specifically, we offer the following design principles for an Extensible Web Platform:

-   Focus on adding **_new low-level capabilities_** to the web platform that are secure and efficient.
-   Expose low-level capabilities that **_explain existing features_**, such as HTML and CSS, allowing authors to understand and replicate them.
-   Develop, describe and test new high-level features in JavaScript, and allow web developers to iterate on them before they become standardized. This creates a **_virtuous cycle_** between standards and developers.
-   **_Prioritize efforts_** that follow these recommendations and deprioritize and refocus those which do not.

---

By focusing on standardizing **__new low-level capabilities__**, and building new features in terms of them, we:

-   Contain new security surface area.
-   Allow optimizations in browser engines to focus on the stable core, which affects more APIs as they are added. This leads to better performance with less implementation effort.
-   Allow browser vendors and library authors to iterate on libraries that provide developer-friendly, high-level APIs.

---

By explaining existing and new features **__in terms of low-level capabilities__**, we:

-   Reduce the rate of growth in complexity, and therefore bugs, in implementations.
-   Make it possible to polyfill more of the platform's new features.
-   Require less developer education for new features. Educational materials can build off of concepts that are already in the platform.

---

Making new features easy to understand and polyfill introduces a **__virtuous cycle__**:

-   Developers can ramp up more quickly on new APIs, providing quicker feedback to the platform while the APIs are still the most malleable.
-   Mistakes in APIs can be corrected quickly by the developers who use them, and library authors who serve them, providing high-fidelity, critical feedback to browser vendors and platform designers.
-   Library authors can experiment with new APIs and create more cow-paths for the platform to pave.

---

By **__prioritizing efforts__** that follow these principles, we:

-   Free up the standards process (especially in the short-term) to focus on features with security or performance concerns, and features that can only be added at the platform level, such as new hardware.
-   Allow web developers and browser-initiated libraries to take the lead in costly explorations.
-   Simplify and streamline the longer-term process of standardizing new APIs, which will already have implementations and significant real-world usage.

---

We want web developers to write more declarative code, not less. This calls for eliminating the standards bottleneck to introducing new declarative forms, and giving library and framework authors the tools to create them.

In order for the open web to compete with its walled competitors, there must be a clear path for good ideas by web developers to become part of the infrastructure of the web. We must enable web developers to build the future web.
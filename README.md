# CoCreate Client

> **Build experiences, not boilerplate.**
>
> **A lightweight, declarative, JavaScript-native client framework for building reactive, realtime, collaborative, and offline-capable applications.**
>
> Design with HTML. Extend with JavaScript. Build without unnecessary complexity.

**CoCreate Client** is an open-source JavaScript framework that transforms standard HTML into interactive, data-driven applications through a declarative HTML Attribute API and a complementary headless JavaScript API.

Instead of spending time writing repetitive state management, DOM manipulation, form handlers, data bindings, network requests, and synchronization logic, developers can describe application behavior directly in HTML.

CoCreate Client allows developers to focus on what matters most: **design, accessibility, functionality, and user experience.**

Build websites, dashboards, CRMs, ERPs, CMS platforms, e-commerce applications, website builders, collaborative editors, internal tools, PWAs, and AI-assisted interfaces using familiar web technologies.

**One framework. Two interfaces. Unlimited possibilities.**

---

## Table of Contents

- [Why CoCreate Client?](#why-cocreate-client)
- [Quick Start](#quick-start)
- [Core Philosophy](#core-philosophy)
- [Two Ways to Build](#two-ways-to-build)
- [Declarative HTML Attribute API](#declarative-html-attribute-api)
- [Headless JavaScript API](#headless-javascript-api)
- [Unified Data Model](#unified-data-model)
- [Reactive Data Binding](#reactive-data-binding)
- [Forms and Data Management](#forms-and-data-management)
- [Realtime Synchronization](#realtime-synchronization)
- [Offline-First Applications](#offline-first-applications)
- [Collaborative Applications](#collaborative-applications)
- [Components and Rendering](#components-and-rendering)
- [Events and Actions](#events-and-actions)
- [Modular Architecture](#modular-architecture)
- [Performance and Lazy Loading](#performance-and-lazy-loading)
- [Progressive Enhancement](#progressive-enhancement)
- [Framework Interoperability](#framework-interoperability)
- [Accessibility and SEO](#accessibility-and-seo)
- [Application Use Cases](#application-use-cases)
- [Architecture](#architecture)
- [Development Philosophy](#development-philosophy)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [Community](#community)
- [License](#license)

---

## Why CoCreate Client?

Modern frontend development often requires developers to learn and maintain multiple layers of abstraction before building an interface.

A relatively simple application may require:

- A component framework
- State management
- Form management
- Data fetching
- Data synchronization
- Client-side routing
- Event handling
- DOM manipulation
- Realtime communication
- Local storage
- Offline caching
- Build configuration
- Supporting libraries

Each additional layer introduces complexity, dependencies, maintenance requirements, and opportunities for bugs.

CoCreate Client approaches frontend development differently.

**HTML already describes the interface. JavaScript already provides the programming language. The browser already provides the platform.**

CoCreate Client builds upon these native technologies instead of replacing them.

The framework provides reusable browser capabilities that can be activated through HTML attributes or invoked directly through JavaScript.

### Traditional Development

A realtime input may require:

1. Creating application state.
2. Binding state to an input.
3. Listening for changes.
4. Updating local state.
5. Validating the value.
6. Sending a network request.
7. Handling errors.
8. Synchronizing remote changes.
9. Updating other connected interfaces.

### CoCreate Client

```html
<input array="users" object="123" key="name" save />
```

The markup declares the data relationship and desired behavior.

The appropriate CoCreate modules handle the underlying operations.

The developer remains free to customize the interface, behavior, styling, and application logic.

### The Difference

| Traditional Development                | CoCreate Client                          |
| -------------------------------------- | ---------------------------------------- |
| Imperative event handlers              | Declarative HTML attributes              |
| Manual DOM updates                     | Reactive rendering                       |
| Repetitive form logic                  | Attribute-driven forms                   |
| Custom data binding                    | Shared data conventions                  |
| Manual realtime integration            | Reusable synchronization modules         |
| Custom offline handling                | IndexedDB and Service Worker integration |
| Framework-specific component patterns  | Native HTML and reusable components      |
| Multiple disconnected abstractions     | Consistent JavaScript primitives         |
| Application logic coupled to rendering | Headless and declarative interfaces      |

**Less repetitive code. More time building the experience.**

---

## Quick Start

Start using CoCreate Client by including the browser script.

```html
<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="UTF-8" />
		<meta name="viewport" content="width=device-width, initial-scale=1.0" />
		<title>My CoCreate Application</title>
	</head>
	<body>
		<h1>Welcome to CoCreate Client</h1>

		<input
			array="users"
			object="123"
			key="name"
			placeholder="Enter your name"
			save />

		<script src="https://cdn.cocreate.app/latest/CoCreate.min.js"></script>
	</body>
</html>
```

CoCreate Client enhances standard HTML with application behavior.

No JSX is required.

No custom template language is required.

No mandatory build step is required for the browser-script approach.

You can begin with HTML and progressively introduce JavaScript whenever needed.

### Source Code

**GitHub:** https://github.com/CoCreateJS/client

---

## Core Philosophy

CoCreate Client is built around several fundamental principles.

### 1. HTML Is Already a Powerful Interface Language

HTML provides a standardized, accessible, browser-native way to describe interfaces.

CoCreate Client extends HTML with declarative application behavior rather than introducing a replacement language.

### 2. JavaScript Is the Programming Language

Developers should not need to learn a new programming language to build applications.

CoCreate Client uses JavaScript objects, arrays, events, promises, modules, and native browser APIs.

### 3. Declarative and Programmatic APIs Should Complement Each Other

Declarative HTML is ideal for describing interfaces and common behaviors.

JavaScript is ideal for custom logic, advanced integrations, and programmatic control.

Both interfaces should operate on the same underlying capabilities.

### 4. Application State Should Be Reusable

Data should not be unnecessarily coupled to a particular component or rendering mechanism.

The same data can power forms, dashboards, lists, collaborative editors, and other interfaces.

### 5. Realtime and Offline Capabilities Should Be Composable

Applications should be able to integrate realtime synchronization, local persistence, and offline functionality without rebuilding their architecture.

### 6. Load Only What Is Needed

Applications should not need to download an entire ecosystem when they only use a small subset of its capabilities.

CoCreate Client is designed around modularity and lazy loading.

### 7. Native Web Technologies Come First

CoCreate Client embraces:

- HTML
- CSS
- JavaScript
- DOM APIs
- Web Components
- Events
- Promises
- ES Modules
- WebSockets
- IndexedDB
- Service Workers
- Browser storage
- Progressive Web Apps

The goal is to extend the web platform, not hide it.

---

## Two Ways to Build

CoCreate Client provides two complementary development interfaces.

### Declarative HTML

Define behavior directly through HTML attributes.

```html
<input array="customers" object="123" key="email" save />
```

### Headless JavaScript

Use the underlying JavaScript capabilities directly.

This allows developers to build custom interfaces, integrate with existing frameworks, and execute application behavior without requiring CoCreate-specific HTML.

### Use Either or Both

A developer can:

- Build an application primarily with HTML.
- Build an application primarily with JavaScript.
- Combine HTML attributes with custom JavaScript.
- Integrate individual CoCreate modules into another framework.
- Use CoCreate's data and synchronization capabilities without adopting its rendering patterns.

**The HTML Attribute API is an interface to the framework—not a limitation on how the framework can be used.**

---

## Declarative HTML Attribute API

The HTML Attribute API is one of CoCreate Client's defining capabilities.

It allows developers to attach application behavior to standard HTML elements.

Instead of creating custom component syntax, CoCreate Client uses attributes to describe relationships, actions, data, and rendering behavior.

### Example: Data-Bound Input

```html
<input array="users" object="123" key="firstName" save />
```

### Example: Form

```html
<form array="users" object>
	<input key="firstName" placeholder="First name" />
	<input key="lastName" placeholder="Last name" />
	<input key="email" type="email" />

	<button type="submit">Save</button>
</form>
```

### Example: Data-Driven Rendering

```html
<div array="users" render>
	<div>
		<h3 key="name"></h3>
		<p key="email"></p>
	</div>
</div>
```

These examples illustrate the declarative model; the specific modules required for each behavior must be available in the application.

### Why Attributes?

HTML attributes provide several advantages:

**Readable**

The behavior is visible directly on the element.

**Inspectable**

Developers can inspect application behavior through standard browser developer tools.

**Composable**

Multiple capabilities can be combined on the same element.

**Framework-independent**

The attributes operate on browser elements rather than requiring a particular rendering framework.

**Progressive**

Developers can begin with simple HTML and introduce more advanced functionality over time.

**AI-friendly**

Structured HTML attributes provide a predictable interface for generating and modifying application behavior.

### No Proprietary Template Language

CoCreate Client does not require developers to abandon standard HTML.

The goal is to make existing HTML more capable.

---

## Headless JavaScript API

Declarative HTML is only one interface to CoCreate Client.

The underlying modules expose JavaScript capabilities that can be used independently of the HTML Attribute API.

This is especially valuable when building:

- Custom components
- Programmatic interfaces
- Complex interactions
- Advanced data workflows
- Framework integrations
- Reusable application libraries
- Automated interfaces
- AI-generated application behavior

### JavaScript-First Design

CoCreate Client favors familiar JavaScript concepts.

```javascript
const object = {
	firstName: "Jane",
	lastName: "Doe",
	email: "jane@example.com"
};

const array = [object];

const key = "email";

const value = object[key];
```

The same concepts appear throughout CoCreate's data model.

Developers work with familiar structures rather than learning a completely different vocabulary.

### Native Browser Integration

CoCreate modules can use native browser APIs directly.

```javascript
const element = document.querySelector("input");

element.addEventListener("input", (event) => {
	console.log(event.target.value);
});
```

CoCreate Client is intended to complement these APIs, not replace every native browser capability with a proprietary abstraction.

### Declarative and Headless Interoperability

A JavaScript operation can update data consumed by declarative interfaces.

A declarative action can invoke functionality implemented in JavaScript.

Both approaches participate in the same application environment.

---

## Unified Data Model

CoCreate Client uses a consistent vocabulary for addressing application data.

The core concepts include:

| Concept  | Purpose                                    |
| -------- | ------------------------------------------ |
| `array`  | Identifies a logical collection of objects |
| `object` | Identifies or represents an object         |
| `key`    | Identifies a property within an object     |
| `index`  | Identifies a position or indexed reference |
| `value`  | Represents the data associated with a key  |
| `filter` | Describes how data should be selected      |
| `on`     | Describes event-driven behavior            |
| `emit`   | Describes event or action emission         |

These concepts align with JavaScript's native object and array structures.

### Example

```javascript
const users = [
	{
		_id: "123",
		name: "Jane Doe",
		email: "jane@example.com"
	}
];
```

A declarative binding might reference:

```html
<input array="users" object="123" key="email" />
```

The attribute structure communicates which data the element represents.

### Nested Keys

CoCreate's data conventions support nested property paths.

For example:

```javascript
const user = {
	profile: {
		contact: {
			email: "jane@example.com"
		}
	}
};
```

A nested property can be represented through dot notation:

```html
<input array="users" object="123" key="profile.contact.email" />
```

### Why a Shared Vocabulary Matters

Developers should not have to learn unrelated naming conventions for every capability.

The same conceptual model can be used across:

- Forms
- Rendering
- State
- Data binding
- Realtime synchronization
- Offline storage
- Application actions
- Custom modules

This reduces cognitive overhead and encourages reusable functionality.

---

## Reactive Data Binding

Reactive interfaces update in response to changing data.

CoCreate Client provides the foundation for connecting application data with DOM elements.

### Declarative Binding

```html
<input array="products" object="123" key="name" save />
```

The element declares the data it represents.

When the appropriate binding and synchronization modules are active, changes can be propagated between the interface and the underlying data.

### Multiple Views of the Same Data

An application may display the same information in several places:

- An editable form
- A summary card
- A dashboard
- A table
- A detail panel

A shared data model allows these interfaces to remain consistent without requiring each component to independently implement the same synchronization logic.

### Reactive Without Mandatory Component State

CoCreate Client does not require every value to be represented through framework-specific component state.

Instead, it provides reusable data and DOM capabilities that can operate across ordinary HTML elements.

---

## Forms and Data Management

Forms are a fundamental part of most applications.

CoCreate Client simplifies common form operations by associating form elements with structured application data.

### Example: Customer Form

```html
<form array="customers" object>
	<label>
		First Name
		<input key="firstName" required />
	</label>

	<label>
		Last Name
		<input key="lastName" required />
	</label>

	<label>
		Email
		<input key="email" type="email" required />
	</label>

	<button type="submit">Save Customer</button>
</form>
```

### Common Form Capabilities

The modular client ecosystem can support:

- Form serialization
- Data binding
- Validation
- Save actions
- Data updates
- Reusable form behavior
- Asynchronous operations
- Error handling
- Realtime updates
- Offline persistence

### Standard HTML Remains Available

Native HTML features remain useful:

```html
<input type="email" required />

<input type="number" min="0" max="100" />

<input type="date" />

<select>
	<option value="active">Active</option>
	<option value="inactive">Inactive</option>
</select>
```

CoCreate Client builds on browser functionality rather than requiring developers to recreate it.

---

## Realtime Synchronization

Realtime applications need to propagate changes between connected interfaces.

CoCreate Client includes modules and integration patterns for realtime communication and synchronization.

### Realtime Applications

Examples include:

- Collaborative editors
- Messaging interfaces
- Live dashboards
- Customer management systems
- Shared administrative tools
- Activity feeds
- Project management applications
- Multiplayer interfaces
- Live notifications

### Shared Data Relationships

A data-bound interface identifies the information it represents.

```html
<input array="projects" object="123" key="title" save />
```

When connected to a compatible realtime data service, the client can participate in synchronization without requiring every element to implement its own networking logic.

### Transport Independence

Realtime functionality should not require application interfaces to manage low-level transport details individually.

Communication modules can provide reusable abstractions over WebSockets and other supported communication mechanisms.

### Synchronization as a Reusable Capability

Realtime synchronization is not limited to forms.

It can also support:

- Lists
- Tables
- Documents
- Dashboards
- Shared state
- Collaborative components

---

## Offline-First Applications

Reliable applications should account for unstable or unavailable network connections.

CoCreate Client is designed to support offline-capable application experiences using native browser technologies.

### IndexedDB

IndexedDB provides persistent structured storage within the browser.

CoCreate modules can use IndexedDB to support:

- Local application data
- Cached records
- Offline reads
- Pending changes
- Synchronization
- Local-first interactions

### Service Workers

Service Workers can support:

- Asset caching
- Offline application loading
- Network request interception
- Background-oriented browser functionality where supported
- Progressive Web App behavior

### Offline Workflow

A typical offline-capable application may follow this lifecycle:

```text
User opens application
        |
        v
Load cached application assets
        |
        v
Read available local data
        |
        v
User interacts with interface
        |
        v
Store pending changes locally
        |
        v
Network becomes available
        |
        v
Synchronize pending changes
        |
        v
Update local application state
```

The exact synchronization strategy depends on the enabled modules and backend integration.

### Why Offline Matters

Offline support is valuable for:

- Mobile applications
- Field service tools
- Remote work
- Travel applications
- Retail systems
- Collaborative tools
- Unreliable network environments

The objective is to keep applications useful even when connectivity is imperfect.

---

## Collaborative Applications

Collaboration introduces challenges beyond ordinary data fetching.

Multiple users may interact with the same information simultaneously.

CoCreate Client's modular architecture supports collaborative application experiences through shared state and synchronization capabilities.

### Collaborative Use Cases

- Document editing
- Website builders
- Visual editors
- Shared dashboards
- Project management
- Team workspaces
- Form collaboration
- Content management
- Realtime chat

### Collaboration Capabilities

Depending on the modules used, collaborative applications can incorporate:

- Realtime updates
- Shared application state
- Concurrent editing
- Change propagation
- Conflict-handling strategies
- User presence
- Synchronization with persistent storage

### Collaborative Editing

Collaborative text editing may require more sophisticated conflict resolution than ordinary object updates.

CoCreate's broader client ecosystem can support specialized collaboration logic, including CRDT-based approaches where appropriate.

The goal is to make collaboration a reusable application capability rather than a completely separate application architecture.

---

## Components and Rendering

CoCreate Client supports component-oriented interface development without requiring every component to use a proprietary JavaScript rendering language.

### HTML-First Components

HTML remains the primary interface description.

```html
<article class="customer-card">
	<h2 key="name"></h2>
	<p key="email"></p>
</article>
```

Reusable components can combine:

- HTML structure
- CSS styling
- Declarative attributes
- JavaScript behavior
- Data bindings
- Events
- Rendering logic

### Data-Driven Rendering

```html
<div array="customers" render>
	<article>
		<h3 key="name"></h3>
		<p key="email"></p>
	</article>
</div>
```

This illustrates how data relationships and rendering behavior can be described through HTML.

### Rendering Philosophy

CoCreate Client aims to avoid unnecessary rendering work.

Browser-native mechanisms can be used to observe changes and update only the relevant interface elements.

### Browser Observers

The browser provides useful primitives including:

- `MutationObserver`
- `IntersectionObserver`
- `ResizeObserver`

These can support:

- DOM change detection
- Lazy initialization
- Visibility-based behavior
- Responsive component updates
- Dynamic content enhancement

### Native DOM Compatibility

CoCreate Client works with standard DOM elements.

Developers retain access to:

```javascript
document.querySelector();

document.querySelectorAll();

element.setAttribute();

element.getAttribute();

element.addEventListener();

element.dispatchEvent();
```

The framework should make DOM development easier, not prevent developers from using the DOM directly.

---

## Events and Actions

Events are a natural way to coordinate application behavior.

CoCreate Client builds upon browser event concepts and reusable action patterns.

### Native Events

```javascript
const button = document.querySelector("button");

button.addEventListener("click", (event) => {
	console.log("Button clicked", event);
});
```

### Declarative Event-Driven Interfaces

CoCreate's declarative conventions allow behavior to be associated with elements through attributes.

This makes it possible to describe actions in markup while keeping their implementations reusable.

### Structured Actions

Application operations can be represented as structured data.

For example, an application may describe a request using a JavaScript object:

```javascript
const payload = {
	method: "object.read",
	array: "customers",
	object: {
		_id: "123"
	}
};
```

This is an illustrative structured action payload.

The client can hand such operations to compatible modules and services without requiring application code to manually implement every underlying transport or execution detail.

### Why Structured Actions?

Structured actions are:

- Serializable
- Inspectable
- Reusable
- Easy to compose
- Suitable for automation
- Compatible with declarative interfaces
- Suitable for AI-assisted generation

The client remains responsible for user-facing interaction, while the appropriate module or service handles execution.

---

## Modular Architecture

CoCreate Client is designed as a modular JavaScript ecosystem.

Applications can use the capabilities they need without requiring every available module.

### Core Principles

**Independent modules**

Capabilities can be developed and maintained independently.

**Shared conventions**

Modules use consistent naming and data structures.

**Composable behavior**

Multiple modules can cooperate within the same application.

**Lazy loading**

Modules can be loaded when required.

**Native JavaScript**

Modules integrate with browser APIs and standard JavaScript.

**Progressive adoption**

Developers can introduce CoCreate functionality into existing applications incrementally.

### Module Categories

The client ecosystem can include capabilities for:

- Data binding
- CRUD interactions
- Rendering
- Forms
- Events
- Actions
- State
- Components
- Realtime communication
- Synchronization
- IndexedDB
- Service Workers
- Files
- Uploads
- Navigation
- Collaboration
- UI interactions
- Application utilities

Not every application needs every category.

### Composable Applications

A simple landing page might use only basic interaction and rendering modules.

A CRM may use forms, CRUD, tables, realtime synchronization, and offline storage.

A website builder may combine rendering, components, drag-and-drop interactions, collaborative editing, and persistent data.

The framework scales in capability according to application needs.

---

## Performance and Lazy Loading

Performance is an important design consideration for CoCreate Client.

The framework aims to provide substantial functionality while minimizing unnecessary initial JavaScript.

### Lightweight Initial Runtime

Historical client size targets have been approximately:

| Configuration                  | Approximate Size |
| ------------------------------ | ---------------: |
| Initial client runtime         |            70 KB |
| Complete lazy-loaded ecosystem |           410 KB |

These figures are project targets or historical estimates, not verified measurements of the current release. Actual sizes depend on the build, enabled modules, and compression method.

### Lazy Loading

Modules can be loaded only when their functionality is required.

This reduces unnecessary work during initial application startup.

### Performance Priorities

- Small initial payload
- Modular loading
- Efficient DOM operations
- Reusable data bindings
- Reduced repetitive event handling
- Browser-native APIs
- Minimal unnecessary dependencies
- Efficient synchronization
- Local caching
- Progressive initialization

### Performance Is More Than Bundle Size

A small JavaScript bundle is useful, but runtime performance also depends on:

- DOM operations
- Rendering frequency
- Network activity
- Memory consumption
- Event handling
- Data access
- Synchronization overhead
- Application architecture

CoCreate Client aims to improve performance across the complete application lifecycle.

---

## Progressive Enhancement

CoCreate Client embraces progressive enhancement.

Developers can begin with standard HTML and add functionality incrementally.

### Start with HTML

```html
<form>
	<label>
		Email
		<input type="email" required />
	</label>

	<button type="submit">Save</button>
</form>
```

### Add Declarative Data Behavior

```html
<form array="customers" object>
	<label>
		Email
		<input key="email" type="email" required />
	</label>

	<button type="submit">Save</button>
</form>
```

### Extend with JavaScript

```javascript
document.querySelector("form").addEventListener("submit", (event) => {
	console.log("Form submitted", event);
});
```

Developers can adopt CoCreate features without abandoning standard web development.

### No Mandatory Rewrite

Existing HTML applications can introduce CoCreate functionality where it provides value.

The entire interface does not need to be rewritten into a new component format.

---

## Framework Interoperability

CoCreate Client is designed to work with native web technologies and can be integrated with applications using other frontend frameworks.

Potential integration environments include:

- React
- Vue
- Angular
- Svelte
- Solid
- Web Components
- Vanilla JavaScript
- Server-rendered HTML
- Static websites
- Custom frontend frameworks

### Headless Integration

Applications can consume CoCreate modules programmatically without adopting the declarative HTML API.

### DOM Integration

Applications can also use CoCreate attributes on compatible DOM elements.

When combining CoCreate DOM behavior with another framework, developers should coordinate ownership of DOM updates to avoid conflicting rendering operations.

### Adopt Only What You Need

CoCreate Client does not require developers to replace their existing frontend stack to benefit from individual modules.

---

## Accessibility and SEO

CoCreate Client encourages the use of semantic HTML and native browser behavior.

### Accessibility

Standard HTML elements already provide important accessibility capabilities.

```html
<label for="customer-email"> Email Address </label>

<input
	id="customer-email"
	type="email"
	array="customers"
	object="123"
	key="email"
	required />
```

Developers can continue using:

- Semantic elements
- Labels
- Keyboard navigation
- Native form controls
- ARIA attributes
- Focus management
- Accessible error messages

Declarative application behavior should complement accessibility rather than replace it.

### SEO

CoCreate Client can enhance HTML documents without requiring the entire interface to originate from client-side JavaScript rendering.

Applications can use:

- Semantic HTML
- Server-rendered content
- Static HTML
- Progressive enhancement
- Metadata
- Search-friendly document structures

Search visibility still depends on the application's rendering and content-delivery strategy.

---

## Application Use Cases

CoCreate Client is not limited to a specific category of application.

Its modular capabilities can be combined to build many kinds of interfaces.

### Websites

Build responsive websites with reusable components, interactive content, forms, and dynamic rendering.

### Website Builders

Create visual editing environments with reusable components, declarative behavior, and persistent application data.

### Application Builders

Allow users to compose interfaces, data relationships, and actions through structured configuration and HTML.

### Customer Relationship Management

Build CRMs with:

- Customer records
- Contact forms
- Realtime updates
- Dashboards
- Data tables
- Offline-capable interfaces
- Collaborative workflows

### Enterprise Resource Planning

Build ERP interfaces for managing operational data, business processes, reporting, and administrative tools.

### Content Management Systems

Create CMS interfaces with:

- Content editing
- Data-driven rendering
- Reusable components
- Media handling
- Collaborative content management

### E-Commerce

Build product catalogs, administrative interfaces, customer portals, carts, and checkout integrations.

### Dashboards

Create dashboards with live data, filters, interactive controls, and realtime updates.

### Project Management

Build shared project boards, task lists, collaboration interfaces, and team workspaces.

### Collaborative Editors

Create interfaces that support shared editing, synchronization, and reusable collaboration capabilities.

### AI-Assisted Applications

Use structured HTML, reusable actions, and declarative configuration to build AI-assisted interfaces.

AI can generate or modify application structures using standard web technologies rather than requiring a proprietary frontend language.

### Progressive Web Apps

Combine browser storage, Service Workers, caching, and responsive interfaces to create installable, offline-capable web applications.

### Internal Tools

Build administrative applications with forms, data management, tables, dashboards, and reusable actions.

### Mobile Web Applications

Create responsive, touch-friendly applications that use native browser capabilities and progressive enhancement.

---

## Architecture

CoCreate Client is organized around reusable browser capabilities rather than a single monolithic rendering system.

### Conceptual Architecture

```text
Application
    |
    +-- HTML Attribute API
    |
    +-- Headless JavaScript API
    |
    v
CoCreate Client Modules
    |
    +-- Components
    +-- Rendering
    +-- Data Binding
    +-- Forms
    +-- Events
    +-- Actions
    +-- State
    +-- CRUD Integration
    +-- Realtime Communication
    +-- Offline Storage
    +-- Collaboration
    |
    v
Native Browser APIs
    |
    +-- DOM
    +-- Events
    +-- Fetch
    +-- WebSockets
    +-- IndexedDB
    +-- Service Workers
    +-- Browser Storage
```

This is a conceptual architecture rather than a literal source-directory map.

### HTML as an Interface

HTML attributes describe behavior.

### JavaScript as an Interface

JavaScript modules expose functionality directly.

### Modules as Capabilities

Modules implement reusable browser functionality.

### Data as Shared State

Structured application data connects interfaces, actions, and synchronization.

### Native Browser APIs as the Foundation

The browser provides the underlying platform.

---

## Development Philosophy

### Build on Standards

Prefer standard HTML, CSS, JavaScript, and browser APIs.

### Favor Composability

Build reusable capabilities that can work together without requiring one enormous framework abstraction.

### Keep the API Familiar

Use terminology aligned with JavaScript:

- Array
- Object
- Key
- Index
- Value
- Event
- Action

### Separate Behavior from Presentation

Application behavior should be reusable across different interfaces.

### Make Declarative Development Practical

Developers should be able to express common functionality without writing repetitive JavaScript.

### Keep Advanced Functionality Accessible

Declarative simplicity should not prevent developers from implementing advanced custom behavior.

### Avoid Unnecessary Dependencies

Use native browser capabilities where they provide an appropriate foundation.

### Support Incremental Adoption

Developers should be able to use one module, several modules, or the broader ecosystem.

### Make Applications Inspectable

HTML attributes and structured actions should make application behavior easier to understand, debug, and maintain.

### Design for Collaboration

Shared data and synchronization should be reusable capabilities.

### Design for Offline Operation

Applications should be able to incorporate local persistence and synchronization where needed.

### Design for AI-Assisted Development

Structured application definitions are easier for both humans and AI systems to inspect, generate, modify, and validate.

---

## Getting Started

### 1. Create an HTML File

Create an `index.html` file.

### 2. Add the CoCreate Client Script

```html
<script src="https://cdn.cocreate.app/latest/CoCreate.min.js"></script>
```

### 3. Add Declarative Behavior

```html
<input
	array="users"
	object="123"
	key="name"
	placeholder="Enter your name"
	save />
```

### 4. Add Your Application Design

Use ordinary HTML and CSS.

```html
<style>
	body {
		font-family: system-ui, sans-serif;
		max-width: 720px;
		margin: 4rem auto;
		padding: 1rem;
	}

	input {
		display: block;
		width: 100%;
		padding: 0.75rem;
		margin-top: 0.5rem;
	}
</style>
```

### 5. Extend as Needed

Add modules for:

- Forms
- Rendering
- Data
- Realtime synchronization
- Offline storage
- Collaboration
- Components
- Custom interactions

Data persistence and remote synchronization require an appropriately configured data service.

### Explore the Source

https://github.com/CoCreateJS/client

---

## Contributing

CoCreate Client is an open-source project.

Contributions are welcome across:

- Core JavaScript modules
- Declarative HTML capabilities
- Performance improvements
- Browser compatibility
- Accessibility
- Documentation
- Examples
- Testing
- Developer tooling
- Offline functionality
- Realtime synchronization
- Collaboration features

### Contribution Principles

When contributing, favor:

1. Native browser capabilities where practical.
2. Small, reusable modules.
3. Consistent JavaScript naming conventions.
4. Declarative and programmatic interoperability.
5. Minimal unnecessary dependencies.
6. Backward-compatible improvements where possible.
7. Clear documentation and examples.
8. Efficient DOM and memory usage.

For repository-specific contribution instructions, consult the project's contributing documentation.

---

## Community

CoCreate Client is part of the broader CoCreateJS open-source project.

The client focuses on browser-side application development and can be used independently.

### Repositories

**CoCreate Client**

https://github.com/CoCreateJS/client

**CoCreateJS Organization**

https://github.com/CoCreateJS

### Contact

For project information, collaboration, and general inquiries:

**Email:** info@cocreatejs.com

---

## License

Refer to the `LICENSE` file in the repository for the applicable license terms.

---

## Build Experiences, Not Boilerplate

Frontend development should not require endless layers of abstraction to create useful applications.

CoCreate Client brings application behavior closer to the interface through declarative HTML while preserving the full flexibility of JavaScript.

Build with HTML.

Extend with JavaScript.

Connect data.

Synchronize in realtime.

Work offline.

Collaborate.

Create reusable components.

Integrate with existing frameworks.

**Focus on the experience. Let the framework handle the repetition.**

**CoCreate Client — Declarative HTML. Native JavaScript. Limitless creativity.**

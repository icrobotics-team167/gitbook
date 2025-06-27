# Section 2: Commands

WPILib has a system to allow for high level actions to be safely and easily coordinated via Commands, Subsystems and Triggers, called Command-based. It is the way that robot mechanism actions are handled in modern FRC programming, and any deviations from the code design patterns it expects are considered unsafe, both in terms of code behavior, and physical safety.

In Command-based architecture, each physical mechanism is represented through a `Subsystem` class, and each action that the mechanism takes is represented through a `Command`. Each `Command` can be scheduled to run by `Trigger` s, which can be anything from "The primary driver's controller's `a` button is down" to "The sensor detected a game piece for longer than .5 seconds."

One crucial difference with normal programming is that normal coding is in a imperative style, meaning you are in control of what happens when, using bigger blocks of code, but Command-based architecture is a declarative event-driven style, where you declare that a short bit of code (A `Command`) should run when an event (A `Trigger`) happens, and the library handles the rest.

## Subsystems

The mechanism in which Command-based architecture enforces behavioral and physical safety is through Subsystem mutexing. A mutex, or mutual exclusion, means that a resource cannot be accessed by two operations at the same time, or in this case, two `Command`s cannot require the same `Subsystem`(s) simultaneously. If command A is running and requires the arm subsystem, but command B is scheduled and it also requires the arm subsystem, then command A is canceled so that command B can run.

A `Subsystem` can only be used by one `Command` at a time, but a `Command` can take control of multiple `Subsystem`s, such as a "place game piece" command taking control of the `Arm` subsystem and `Wrist` subsystem simultaneously.

TODO: Make lesson

## Lambdas

Declaring what code runs is done through lambas. It is similar to functions/methods in that it is defined and run later, but the reference to that define code can be passed around as data, and called upon by code. Commands primarily use `Runnables` (which just runs code) and `Suppliers` (which outputs a value) as the creation of a `Command` object and when that command is actually run are different times.

The syntax of a lambda is as follows:

```java
var lambda = () -> {
  // Some code that runs later
  // If this is a Supplier, then a return statement would be at the end.
};
```

If all a lambda does is call upon an existing method, IE:

```java
var lambda = () -> { foo.bar() };
```

Then it can be shortened as such:

```java
var lamdba = foo::bar;
```

## Executing Commands with Triggers

To run a command, it must be scheduled to execute via `Trigger` s. A `Trigger` takes in a boolean state (button down, sensor tripped, etc.) and schedules or cancels `Command`s that are bound to it when the state changes.

For a lesson on binding `Command`s to `Trigger` s, see below:

{% content-ref url="lesson-2.-binding-commands-to-triggers.md" %}
[lesson-2.-binding-commands-to-triggers.md](lesson-2.-binding-commands-to-triggers.md)
{% endcontent-ref %}

NEVER schedule commands manually or execute them manually through `command.schedule()` and `command.execute()` .

## Commands

There are many types of `Command`s that do different things. Each command type have their own pages and accompanying lessons:

{% content-ref url="lesson-2.-run-command.md" %}
[lesson-2.-run-command.md](lesson-2.-run-command.md)
{% endcontent-ref %}

## Command factories

A factory method is a method that hides the object instantiation (`new` ) within itself, making it cleaner to read the code. WPILib has many factory methods for commands, which allows for use of commands without calling class constructors explicitly.

There are two sources for command factories:

* The `Subsystem` class
  * Commands from these factories automatically declare the subsystem as a requirement, allowing for implicit command requirements.
  * Does not contain all the factories.
* `import static edu.wpi.first.wpilibj2.command.Commands.*;`&#x20;
  * Has factories for every command type.
  * Does not have implicit command requirements.

You can also make your own command factories in a subsystem class. This allows for command actions to be a single method from the outside, while keeping resources, variables, and logic on the inside.

## Command groups

In addition, commands can be grouped together to run sequentially, in parallel, racing each other, etc. See the below lesson for more:

{% content-ref url="lesson-2.-command-groups.md" %}
[lesson-2.-command-groups.md](lesson-2.-command-groups.md)
{% endcontent-ref %}

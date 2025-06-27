# Lesson 2.?: run Command

Accompanying coding lesson: [https://github.com/icrobotics-team167/CotcCurriculum/tree/main/CommandBasics/run](https://github.com/icrobotics-team167/CotcCurriculum/tree/main/CommandBasics/run)

A `run` command takes in a `Runnable` and runs that every loop in `execute()`. This is used for Command actions that must run periodically, such as motor control loops.

Syntax example:

```java
// Example.java
public Command runCommand() {
  return run(() -> {
    // Do something every robot loop
  }
}

// Robot.java
var example = new Example(mode != mode.REPLAY ? new ExampleIOPhoenix() : new ExampleIO() {});

primary.a().whileTrue(example.runCommand());
```

The `run` method from the `Subsystem` class automatically declares the subsystem as a requirement, while the `run` method from the `Commands` class does not have requirements unless explicitly declared in the parameters.

Code examples:

* Kernel Overflow (Team 167, Reefscape)
  * [Swerve teleop drive](https://github.com/icrobotics-team167/2025_Reefscape/blob/230afa18a2fbffd82682add448cd1f2adc900073/src/main/java/frc/cotc/drive/Swerve.java#L352)
  * [Elevator position control](https://github.com/icrobotics-team167/2025_Reefscape/blob/230afa18a2fbffd82682add448cd1f2adc900073/src/main/java/frc/cotc/superstructure/Elevator.java#L118)
  * [Algae roller intaking](https://github.com/icrobotics-team167/2025_Reefscape/blob/230afa18a2fbffd82682add448cd1f2adc900073/src/main/java/frc/cotc/superstructure/AlgaeRollers.java#L28)


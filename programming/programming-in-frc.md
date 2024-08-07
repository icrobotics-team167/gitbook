---
description: >-
  Things in FRC software iterate far too rapidly to make any guide to specific
  things that can stay relevant for more than a season or two, so this doc will
  focus on how you can find answers to problems
---

# Programming in FRC

## Step 0: Don't pull an XY problem.

The XY problem, as it's commonly called, is a common problem where a user tries to make their own solution to a problem, gets stuck and looks for help on their attempted solution instead of the original solution, getting counterproductive answers.

An example from [https://xyproblem.info](https://xyproblem.info):

> ```
> <bob> How can I echo the last three characters in a filename?
> <feline> If they're in a variable: echo ${foo: -3}
> <feline> Why 3 characters? What do you REALLY want?
> <feline> Do you want the extension?
> <bob> Yes.
> <feline> There's no guarantee that every filename will have a three-letter extension,
> <feline> so blindly grabbing three characters does not solve the problem.
> <feline> echo ${foo##*.}
> ```

## Step 1: Read documentation

Many software things in FRC have extensive documentation that will most likely have what you want. Poking around and clicking on things that seem relevant and/or typing in keywords into the docs page's search bar can often get you the thing you want.

Some links to the docs for popular things in FRC: (Non-exhaustive)

* WPILib: [https://docs.wpilib.org/en/stable/index.html](https://docs.wpilib.org/en/stable/index.html)
* Phoenix 6: [https://v6.docs.ctr-electronics.com/en/latest/](https://v6.docs.ctr-electronics.com/en/latest/)
* REVLib: [https://docs.revrobotics.com/brushless](https://docs.revrobotics.com/brushless)
* PathPlanner: [https://pathplanner.dev/home.html](https://pathplanner.dev/home.html)
* PhotonVision: [https://docs.photonvision.org/en/latest/](https://docs.photonvision.org/en/latest/)
* LimelightVision: [https://docs.limelightvision.io/docs/docs-limelight/getting-started/summary](https://docs.limelightvision.io/docs/docs-limelight/getting-started/summary)

## Step 2: The power of the internet, in your hands

You can figure out a lot of things by typing in the issue into your browser's search bar. Google is surprisingly powerful when it comes to finding solutions to problems.

However, you need to be specific. Google is not omnipotent, it needs to know what you want. In addition, although this is less relevant in FRC, you may get articles that are completely useless/irrelevant and just want you to click on ads.

An example:

> User X is having an issue where VS Code is telling them that the `TalonFX` class is deprecated.
>
> Things User X should not type into Google:
>
> * `TalonFX`
>   * This is too broad, they will only get information related to TalonFX motors.
> * `FRC Phoenix`
>   * This is not much better, it doesn't specify the thing they're having an issue with.
>
> What they should type instead:
>
> * `FRC TalonFX deprecated`
> * This returns results on ChiefDelphi related to how the `TalonFX` class in Phoenix v5 is considered deprecated, and that the user should use Phoenix v6's `TalonFX` class.

## Step 3: Ask Online


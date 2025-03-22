---
description: >-
  Eventually, no matter what, you'll find a problem you can't easily figure out
  yourself. Here are some tips to help you find solutions better and faster.
---

# How to Solve Programming Problems

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
* AdvantageKit: [https://docs.advantagekit.org/](https://docs.advantagekit.org/)
* AdvantageScope: (Also available in the app) [https://docs.advantagescope.org/](https://docs.advantagescope.org/)
* Phoenix 6: [https://v6.docs.ctr-electronics.com/en/latest/](https://v6.docs.ctr-electronics.com/en/latest/)
* REVLib: [https://docs.revrobotics.com/brushless](https://docs.revrobotics.com/brushless)
* PathPlanner: [https://pathplanner.dev/home.html](https://pathplanner.dev/home.html)
* Choreo: [https://choreo.autos/](https://choreo.autos/)
* PhotonVision: [https://docs.photonvision.org/en/latest/](https://docs.photonvision.org/en/latest/)
* LimelightVision: [https://docs.limelightvision.io/docs/docs-limelight/getting-started/summary](https://docs.limelightvision.io/docs/docs-limelight/getting-started/summary)

## Step 2: The power of the internet, in your hands

You can figure out a lot of things by typing in the issue into your browser's search bar. Google is surprisingly powerful when it comes to finding solutions to problems.

However, you need to be specific. Google is not omnipotent, it needs to know what you want. In addition, although this is less relevant in FRC, you may get articles that are completely useless/irrelevant and just want you to click on ads, so you need to make sure you're being specific to avoid the useless articles.

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

There are two main forums for FRC:

* ChiefDelphi: [https://chiefdelphi.com](https://chiefdelphi.com)
  * An old-school internet forum, this the big discussion forum for FRC and occasionally FTC, where discussion posts and help posts are made.
* Unofficial FRC Discord: [https://discord.gg/frc](https://discord.gg/frc)
  * A Discord server for FRC, this is the other big discussion places for FRC. You can find all sorts of discussions and help happening in here, in their relevant channels (IE `#programming-discussion`)

However, just like Google as described in Step 2, the people helping you in those online forums are not omnipotent; You need to ask good, descriptive questions that lay out your problem in detail.

Resources on help forum etiquette:

* Don't Ask To Ask: [https://dontasktoask.com/](https://dontasktoask.com/)
* No Hello: [https://nohello.net/en/](https://nohello.net/en/)

Resources on asking good questions:

* StackOverflow questions guidelines: [https://stackoverflow.com/help/how-to-ask](https://stackoverflow.com/help/how-to-ask)
* ProPublica: "How to Ask Programming Questions": [https://www.propublica.org/nerds/how-to-ask-programming-questions](https://www.propublica.org/nerds/how-to-ask-programming-questions)

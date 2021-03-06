# RulesEngine
RulesEngine is a simple example of reducing the complexity of conditional logic.

 - C# 7.0
 - .NET Standard 2.0

There are multiple project types implemented here:

  - RulesEngine_Basic - DotNet Core Class Library / Tests
  - RulesEngine_Func_HTTP - Azure Function v2 / HTTP Trigger
  - RulesEngine_Func_Queue - Azure Function v2 / Queue Trigger

The goal is to separate the rules from the logic. We create a collection of rules. We process them by looping over the collection, verify the thresholds are violated, and calling the processing logic that should happen for that particular violation.

In this example we have are collecting refrigerator telemetry. We create multiple temperature-based rules. Using these rules, we will either generate a task or a workorder depending on the threshold and violation severity.

![Image of CodeMap](https://github.com/tripdubroot/RulesEngine/blob/master/img/codemap.PNG)

Created using [The Rules Design Pattern](http://www.michael-whelan.net/rules-design-pattern/) by Michael Whelan

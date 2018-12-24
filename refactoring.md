#### Class - 
  - data 
  - behavior (maybe on its data)


#### Refactoring:
- gives you a terminology. Many of them are pretty simple ideas. 
- honestly, it's about as detailed as you can get developers to talk about code. 
- es6 / mocha

#### cons
 - implicit assumption about what is "good code" - if there was a consensus on that, the refactorings could probably be less
 - such as function-size
 - a lot of repetition 
 - doesn't acknowledge the reality that good code should be simple - seems to make good code more complicated 
 - no deep discussion of architectural issues
   - refactoring involves a DevOps mindset
   - no algorithmic discussions
   - no web patterns 
     - no mention of REST
     - no mention of frameworks
   - no database concepts
     - no join tables, has_many though:
   - no big data patterns
 - no discussion of other conecpts such as Single Responsibility Principe, Leaky Abstractions, Law of Demeter
 - doesn't deal with issues of language flexibility
    - when to use eval in Javascript
    - when to use define_method in Ruby
 - refactoring for gains in performance
 - no discussion of lambdas
 - no discussion of exceptions
 - should be easier to say this is what good code is
    - really permeatest the book and the overall poor writing. A good example is `Inline Function`; p115 without notions of 'what is good?', cataloguing them is a bit pointless. 
 - bad code --> better code
 - it was pretty revolutionary in its time but the update is pretty meager for 20 years later
    - no map-reduce
 - some trivial examples such as Rename Variable
 - a bit too stand-alone - many large open source products have undergone refactorings but no discussion of those choices
 - doesn't deal with duck typing
 - doesn't deal with dynamic language refactorings

 
#### Refactoring: A First Example 
  - The Starting Point p001
  - Comments on the Starting Program  p003
  - Decomposing the `statement` function p006
  - Status: Lots of Nested Functions p022
  - Splitting the Phases of Calculation and Formatting p024
  - Status: Separated into Two Files (and Phases) p031
  - Reorganizing the Calculations by Type p034
     - Creating a Performance Calculator p036
     - Moving Functions into the Calculator p037
     - Making the Performance Calculator Polymorphic p038
  - Status: Creating the Data with the Polymorphic Calculator p041
  - Final Thoughts p043

#### Principles in Refactoring 
  - Defining Refactoring p045
  - The Two Hats p046
  - Why Should We Refactor? p047
    - Refactoring Improves the Design of Software p047
    - Refactoring Makes Software Easier to Understand p047
    - Refactoring Helps Me Find Bugs p048
    - Refactoring Helps Me Program Faster p048
  - When Should we Refactor? p050
    - Prepatory Refactoring - Making It Easier to Add a Feature p050
    - Comprehension Refactoring: Making Code Easier to Understand p051
    - Litter-Pickup Refactoring p052
    - Planned and Opportunistic Refactoring p052
    - Long Term Refactoring p053
    - Refactoring in a Code Review p054
    - What Do I Tell My Manager? p054
    - When Should I Not Refactor? p055
  - Problems with Refactoring p055
    - Slowing Down New Features p056
    - Code Ownership p057
    - Branches p058
    - Testing p059
    - Legacy Code p060
    - Databases p061
  - Refactoring, Architecture, and YAGNI p062
  - Refactoring and the Wider Software Development Process p063
  - Refactoring and Performance p064
  - Where did Refactoring Come From? p067
  - Automated Refactorings p068
  - Going Further p070

#### Bad Smells in Code 
  - Mysterious Name p072
  - Duplicated Code p072
  - Long Function p073
  - Long Parameter List p074
  - Global Data p074
  - Mutable Data p075
  - Divergent Change p076
  - Shotgun Surgery p076
  - Feature Envy p077
  - Data Clumps p078
  - Primitive Obsession p078
  - Repeated Switches p079
  - Loops p079
  - Lazy Element p080
  - Speculative Generality p080
  - Temporary Field p080
  - Message Chains p081
  - Middle Man p081
  - Insider Trading p082
  - Large Class p082
  - Alternative Classed with Different Interfaces p083
  - Data Class p083
  - Refused Bequest p083
  - Comments p084


#### Building Tests
  - The Value of Self-Testing Code p085
  - Sample Code to Test p087
  - A First Test p090
  - Add Another Test p093
  - Modifying the Fixture p095
  - Probing the Boundaries p097
  - Much More Than This p099  

#### Introducing the Catalog 
  - Format of the Refactorings p101
  - The Choice of Refactorings p102
 
#### First Set of Refactorings
  - Extract Function p106
  - Inline Function p115
  - Extract Variable p119
  - Inline Variable p123
  - Change Function Declaration p124
  - Encapsulate Variable p132
  - Rename Variable p137
  - Introduce Parameter Object p140
  - Combine Functions into Class p144
  - Combine Functions into Transform p149
  - Split Phase p154
 
#### Encapsulation 
  - Encapsulate Record p162
  - Encapsulate Collection p170
  - Replace Primitive with Object p174
  - Replace Temp with Query p178
  - Extract Class p182
  - Inline Class p186
  - Hide Delegate p189
  - Remove Middle Man p192
  - Substitute Algorithm p195 
 
#### Organizing Data
  - Split Variable p240
  - Rename Field p240
  - Replace Derived Variable with Query p248
  - Change Reference to Value p252
  - Change Value to Reference p256

#### Moving Features 
  - Move Function p198
  - Movie Field p207
  - Move Statements into Function p213
  - Move Statements to Callers p217
  - Replace Inline Code with Function Call p222
  - Slide Statements p223
  - Split Loop p227
  - Replace Loop with Pipeline p231
  - Remove Dead Code p237
 
#### Simplify Conditional Logic
  - Decompose Conditional p260
  - Consolidate Condition Expression p263
  - Replace Nested Conditional with Guard Clauses p266
  - Replace Conditional with Polymorphism p272
  - Introduce Special Case p289
  - Introduce Assertion p302

#### Refactoring APIs
  - Separate Query from Modifier p306
  - Parameterize Function p310
  - Remove Flag Argument p314
  - Preserve Whole Object p319
  - Replace Parameter with Query p324
  - Replace Query with Parameter p327
  - Remove Setting Method p331
  - Replace Constructor with Factory Function p334
  - Replace Function with Command p337
  - Replace Command with Function p344


#### Dealing with Inheritance 
  - Pull Up Method p350
  - Pull Up Field p353
  - Pull Up Constructor Body p355
  - Push Down Method p359
  - Push Down Field p361
  - Replace Type Code with Subclasses p362
  - Remove Subclass p369
  - Extract Superclass p375
  - Collapse Hierarchy p380
  - Replace Subclass with Delegate p381
  - Replace Superclass with Delegate p399

#### Catalogue of Refactorings
1. Replace Conditional with Polymorphism p272
1. Introduce Assertion p302
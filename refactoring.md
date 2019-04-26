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
    - Motivation p106
    - Mechanics p107
    - Example: No Variables Out of Scope p109
    - Example: Using Local Variables p110
    - Example: Reassigning a Local Variable p112
  - Inline Function p115
    - Motivation p115
    - Mechanics p116
    - Example p116
  - Extract Variable p119
    - Motivation p119
    - Mechanics p120
    - Example p120
    - Example: With a Class p121
  - Inline Variable p123
    - Motivation p123
    - Mechanics p123
  - Change Function Declaration p124
    - Motivation p124
    - Mechanics p125
      - Simple Mechanics p126
      - Migration Mechanics p126
    - Example: Renaming a Function (Simple Mechanics) p127
    - Example: Renaming a Function (Migration Mechanics) p127
    - Example: Adding a Parameter p128
    - Example: Changing a Parameter to One of Its Properties p129
  - Encapsulate Variable p132
  - Rename Variable p137
  - Introduce Parameter Object p140
  - Combine Functions into Class p144
  - Combine Functions into Transform p149
  - Split Phase p154
 
#### 7 Encapsulation 
  - Encapsulate Record p162
    - Motivation p162
      - Mechanics p163
      - Example p163
      - Example: Encapsulating a Nested Record p165
  - Encapsulate Collection p170
    - Motivation p170
    - Mechanics p171
    - Example p172
  - Replace Primitive with Object p174
    - Motivation p174
    - Mechanics p175
    - Example p175
  - Replace Temp with Query p178
    - Motivation p178
    - Mechanics p179
    - Example p180
  - Extract Class p182
    - Motivation p182
    - Mechanics p183
    - Example p183
  - Inline Class p186
    - Motivation p186
    - Mechanics p187
    - Example p187
  - Hide Delegate p189
    - Motivation p189
    - Mechanics p190
    - Example p190
  - Remove Middle Man p192
    - Motivation p192
    - Mechanics p193
    - Example p193
  - Substitute Algorithm p195 
    - Motivation p195
    - Mechanics p196
 

#### Moving Features 
  - Move Function p198
    - Motivation p198
    - Mechanics p199
    - Example: Moving a Nested Function to Top Level p200
    - Example: Moving Between Classes p204
  - Movie Field p207
    - Motivation p207
    - Mechanics p208
    - Example p209
    - Example: Moving to a Shared Object p211
  - Move Statements into Function p213
    - Motivation p213
    - Mechanics p214
    - Example p214
  - Move Statements to Callers p217
    - Motivation p217
    - Mechanics p218
    - Example p218
  - Replace Inline Code with Function Call p222
    - Motivation p222
    - Mechanics p222
  - Slide Statements p223
    - Motivation p223
    - Mechanics p223
    - Example p224
    - Example: Sliding with Conditionals p226
    - Further Reading p226
  - Split Loop p227
    - Motivation p227
    - Mechanics p228
    - Example p229
  - Replace Loop with Pipeline p231
    - Motivation p231
    - Mechanics p231
    - Further Reading p236
  - Remove Dead Code p237
    - Motivation p237
    - Mechanics p237

#### 9 Organizing Data
  - Split Variable p240
    - Motivation p240
    - Mechanics p240
    - Example p241
    - Example: Assigning to an Input Parameter p242
  - Rename Field p240
    - Motivation p244
    - Mechanics p244
    - Example: Renaming a Field p245
  - Replace Derived Variable with Query p248
    - Motivation p248
    - Mechanics p249
    - Example p249
    - Example: More Than One Source p250
  - Change Reference to Value p252
    - Motivation p252
    - Mechanics p253
    - Example p254
  - Change Value to Reference p256
    - Motivation p256
    - Mechanics p257
    - Example p257

#### Simplify Conditional Logic
  - Decompose Conditional p260
    - Motivation p260
    - Mechanics p261
    - Example p261
  - Consolidate Condition Expression p263
    - Motivation p263
    - Mechanics p264
    - Example p264
    - Example: Using ands p265
  - Replace Nested Conditional with Guard Clauses p266
    - Motivation p267
    - Mechanics p267
    - Example p267
    - Example: Reversing the Conditions p269
  - Replace Conditional with Polymorphism p272
    - Motivation p272
    - Mechanics p273
    - Example P274
    - Example: Using Polymorphism for Variation p278
  - Introduce Special Case p289
    - Motivation p289
    - Mechanics p289
    - Example p290
    - Example: Using an Object Literal p295
    - Example: Using a Transform p297
  - Introduce Assertion p302
    - Motivation p302
    - Mechanics p303
    - Example p303

#### Refactoring APIs
  - Separate Query from Modifier p306
    - Motivation p306
    - Mechanics p307
    - Example p307
  - Parameterize Function p310
    - Motivation p310
    - Mechanics p310
    - Example p311
  - Remove Flag Argument p314
    - Motivation p314
    - Mechanics p315
    - Example p316
  - Preserve Whole Object p319
    - Motivation p319
    - Mechanics p320
    - Example p320
    - Example: A Variation to Create the New Function p322
  - Replace Parameter with Query p324
    - Motivation p324
    - Mechanisms p325
    - Example p325
  - Replace Query with Parameter p327
    - Motivation p327
    - Mechanisms p328
    - Example p328
  - Remove Setting Method p331
    - Motivation p331
    - Mechanisms p332
    - Example p332
  - Replace Constructor with Factory Function p334
    - Motivation p334
    - Mechanisms p334
    - Example p335
  - Replace Function with Command p337
    - Motivation p337
    - Mechanisms p338
    - Example p338
  - Replace Command with Function p344
    - Motivation p344
    - Mechanisms p344
    - Example p345


#### Dealing with Inheritance 
  - Pull Up Method p350
    - Motivation p350
    - Mechanisms p351
    - Example p351
  - Pull Up Field p353
    - Motivation p353
    - Mechanisms p354
  - Pull Up Constructor Body p355
    - Motivation p356
    - Mechanisms p356
    - Example p356
  - Push Down Method p359
    - Motivation 359
    - Mechanics 359
  - Push Down Field p361
    - Motivation p361
    - Mechanics p361
  - Replace Type Code with Subclasses p362
    - Motivation p362
    - Mechanics p363
    - Example p364
    - Example: Using Indirect Inheritance p366
  - Remove Subclass p369
    - Motivation p369
    - Mechanics p370
    - Example p370
  - Extract Superclass p375
    - Motivation p376
    - Mechanics p376
    - Example p376
  - Collapse Hierarchy p380
    - Motivation p380
    - Mechanics p380
  - Replace Subclass with Delegate p381
  - Replace Superclass with Delegate p399

#### Catalogue of Refactorings
1. Replace Conditional with Polymorphism p272
1. Introduce Assertion p302
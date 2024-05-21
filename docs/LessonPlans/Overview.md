
# Lesson Plans

Lesson plans are developed in Obsidian and broken into 15-30min blocks. The idea being that depending on the length of the lesson various blocks can be combined. Eg: If the lesson duration is 60min then 2-3 blocks of related material would be combined. 

Each block defines:

- Learning Outcomes
- Lesson Goals
- Assessment
    - Diagnostic
    - Formative
    - Summative

A full lesson plan would be:

```mermaid
block-beta
 columns 1
 LO("Lesson Overview")
 block:Block1:1
    columns 1
    A1("Activity A1")
    A2("Activity A2")
 end
 block:Block2:1
    columns 1
    B1("Activity B1")
    B2("Activity B2")
 end
 block:Reflection:1
    columns 1
    Evaluation
    Summation
 end

```

```mermaid
classDiagram
    LessonPlan "1" --> "*" Block
    Block "1" --> "*" Activity
    LessonPlan "1" --> "1" Reflection
    Reflection --> Evaluation
    Reflection --> "*" SummationQuestions
class LessonPlan {
    Class
    Subject
    Period
    LessonTime
    StartTime
    EndTime
    Size
}
class Block {
    Goals
    Outcomes
    Assessements
    Equipment
}
class Activity {
    Timing
    TeacherActivity
    StudentActivity
    Homework
}
```
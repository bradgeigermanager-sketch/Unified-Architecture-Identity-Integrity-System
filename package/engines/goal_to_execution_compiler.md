Compiler: GoalToExecutionCompiler

Pipeline:
1. interpretGoal()
2. generateSubGoals()
3. generateTasks()
4. buildProcedures()
5. generateToolSpecs()
6. assembleExecutionPlan()

Modules:
- GoalInterpreter
- SubGoalGenerator
- TaskGenerator
- ProcedureBuilder
- ToolSpecGenerator

Outputs:
- executionPlan
- tasks[]
- procedures[]
- toolSpecs[]

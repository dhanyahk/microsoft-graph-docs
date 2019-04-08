
```CS

GraphServiceClient graphClient = new GraphServiceClient( authProvider );

var orderHintsByAssignee = new PlannerOrderHintsByAssignee
{
	Aaa27244-1db4-476a-a5cb-004607466324 = "8566473P 957764Jk!",
};

var assignedToTaskBoardFormat = new PlannerAssignedToTaskBoardTaskFormat
{
	OrderHintsByAssignee = orderHintsByAssignee,
};

await graphClient.Planner.Tasks["{task-id}"].AssignedToTaskBoardFormat
	.Request()
	.UpdateAsync(assignedToTaskBoardFormat);

```
# 🛠 Development Workflow with MCPs

## ⏳ Before Each Coding Session

```bash
archon:manage_task(action="list", filter_by="project", filter_value="[project_id]")
archon:manage_task(action="list", filter_by="status", filter_value="todo", project_id="[project_id]")
```

## 🔁 Task Execution Loop

1. **Check current task** → `archon:manage_task(action="get", task_id="[current_task_id]")`
2. **Mark In-Progress** → `archon:manage_task(action="update", task_id="[current_task_id]", update_fields={"status":"doing"})`
3. **Do RAG + example research** (see [TASK_RESEARCH_GUIDE.md](./TASK_RESEARCH_GUIDE.md))
4. **Implement using Serena** (see [SERENA_RULES.md](./SERENA_RULES.md))
5. **Mark complete** → `archon:manage_task(action="update", task_id="[current_task_id]", update_fields={"status":"review"})`
6. **Get next task** → `archon:manage_task(action="list", filter_by="status", filter_value="todo", project_id="[project_id]")`

## 📅 End of Session Rituals

- Update statuses (done/review)
- Log architectural notes if relevant
- Create new tasks if scope discovered

# 🚀 Bootstrapping Archon Projects

Use this guide when starting or migrating projects:

## Scenario 1: New Project

```bash
archon:manage_project(action="create", title="New Project", github_repo="github.com/user/repo-name")
```

## Scenario 2: Integrating into a Legacy Project

1. Analyze existing codebase thoroughly (read major files, architecture, state)
2. Identify remaining work and create tasks accordingly
3. Create project container:

```bash
archon:manage_project(action="create", title="Existing Project")
```

## Scenario 3: Continuing an Existing Project

```bash
archon:manage_task(action="list", filter_by="project", filter_value="[project_id]")
```

## Research Before Planning Tasks

```bash
archon:perform_rag_query(query="JWT middleware architecture", match_count=5)
```

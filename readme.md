# Override way
```
[tool.uv]
override-dependencies = [
    "my-testing-lib @ git+ssh://git@github.com/Wintreist/uv_issue_16484.git@test_update_git_to_path#subdirectory=my-testing-lib"
]
```
```powershell
PS D:\ROBO\Repositories\uv_issue_16484\my-lib> uv sync -U     
  × Failed to resolve dependencies for `my-testing-lib` (v0.1.0)
  ╰─▶ Requirements contain conflicting URLs for package `other-lib` in all marker environments:
      - git+ssh://git@github.com/Wintreist/uv_issue_16484.git@test_update_git_to_path#subdirectory=other-lib
      - git+ssh://git@github.com/Wintreist/uv_issue_16484.git#subdirectory=other-lib
  help: `my-testing-lib` (v0.1.0) was included because `my-lib:dev` (v0.1.0) depends on `my-testing-lib`
```
# Constraint way
```
[tool.uv]
constraint-dependencies = [
    "my-testing-lib @ git+ssh://git@github.com/Wintreist/uv_issue_16484.git@test_update_git_to_path#subdirectory=my-testing-lib"
]
```
```powershell
PS D:\ROBO\Repositories\uv_issue_16484\my-lib> uv sync -U
    Updated ssh://git@github.com/Wintreist/uv_issue_16484.git (4f566b9fa385dca6f92c6968e8060965d66094e0)
  × Failed to resolve dependencies for `other-lib` (v0.1.0)
  ╰─▶ Requirements contain conflicting URLs for package `my-testing-lib` in all marker environments:
      - git+ssh://git@github.com/Wintreist/uv_issue_16484.git@test_update_git_to_path#subdirectory=my-testing-lib
      - git+ssh://git@github.com/Wintreist/uv_issue_16484.git#subdirectory=my-testing-lib
  help: `other-lib` (v0.1.0) was included because `my-lib` (v0.1.0) depends on `other-lib`
```
# Override way
```
[tool.uv]
override-dependencies = [
    "my-testing-lib @ git+ssh://git@github.com/Wintreist/uv_issue_16484.git@test_branch_with_git_to_path#subdirectory=my-testing-lib"
]
```
```powershell
PS D:\ROBO\Repositories\uv_issue_16484\my-lib> uv sync -U     
  × Failed to resolve dependencies for `my-testing-lib` (v0.1.0)
  ╰─▶ Requirements contain conflicting URLs for package `other-lib` in all marker environments:
      - git+ssh://git@github.com/Wintreist/uv_issue_16484.git@test_update_git_to_path#subdirectory=other-lib
      - git+ssh://git@github.com/Wintreist/uv_issue_16484.git@test_branch_with_git_to_path#subdirectory=other-lib
  help: `my-testing-lib` (v0.1.0) was included because `my-lib:dev` (v0.1.0) depends on `my-testing-lib`
```
# Constraint way
```
[tool.uv]
constraint-dependencies = [
    "my-testing-lib @ git+ssh://git@github.com/Wintreist/uv_issue_16484.git@test_branch_with_git_to_path#subdirectory=my-testing-lib"
]
```
```powershell
PS D:\ROBO\Repositories\uv_issue_16484\my-lib> uv sync -U
    Updated ssh://git@github.com/Wintreist/uv_issue_16484.git (d9801bf70c81235511ad2d32b593f6670aac34b7)
    Updated ssh://git@github.com/Wintreist/uv_issue_16484.git (8613fef1ef3435c75dc55f7b06e9fc9b84fe4112)
  × Failed to resolve dependencies for `my-testing-lib` (v0.1.0)
  ╰─▶ Requirements contain conflicting URLs for package `other-lib` in all marker environments:
      - git+ssh://git@github.com/Wintreist/uv_issue_16484.git@test_update_git_to_path#subdirectory=other-lib
      - git+ssh://git@github.com/Wintreist/uv_issue_16484.git@test_branch_with_git_to_path#subdirectory=other-lib
  help: `my-testing-lib` (v0.1.0) was included because `my-lib:dev` (v0.1.0) depends on `my-testing-lib`
```
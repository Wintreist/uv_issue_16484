PS D:\...\Repositories\uv_issue_16484\my-lib> uv sync -U
  × Failed to resolve dependencies for `other-lib` (v0.1.0)
  ╰─▶ Requirements contain conflicting URLs for package `my-testing-lib` in all marker environments:
      - git+ssh://git@github.com/Wintreist/uv_issue_16484.git@TESTING-BRANCH#subdirectory=my-testing-lib
      - git+ssh://git@github.com/Wintreist/uv_issue_16484.git#subdirectory=my-testing-lib
  help: `other-lib` (v0.1.0) was included because `my-lib` (v0.1.0) depends on `other-lib`
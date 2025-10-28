PS D:\ROBO\Repositories\uv_issue_16484\my-lib> uv sync -U
  × Failed to resolve dependencies for `my-testing-lib` (v0.1.0)
  ╰─▶ Package `pyqt-extra-dep-lib` was included as a URL dependency. URL dependencies must be expressed as direct requirements or constraints. Consider adding `pyqt-extra-dep-lib @
      git+ssh://git@github.com/Wintreist/uv_issue_16484.git#subdirectory=pyqt-extra-dep-lib` to your dependencies or constraints file.
  help: `my-testing-lib` (v0.1.0) was included because `my-lib:dev` (v0.1.0) depends on `my-testing-lib`
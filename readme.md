PS D:\...\Repositories\uv_issue_16484\my-lib> uv sync -U
Resolved 3 packages in 681ms
      Built my-lib @ file:///D:/.../Repositories/uv_issue_16484/my-lib
      Built my-testing-lib @ git+ssh://git@github.com/Wintreist/uv_issue_16484.git@cc49101f03715fbe6495f9e0bd142921aca81c5f#subdirectory=my-testing-lib
      Built other-lib @ git+ssh://git@github.com/Wintreist/uv_issue_16484.git@cc49101f03715fbe6495f9e0bd142921aca81c5f#subdirectory=other-lib
Prepared 3 packages in 1.02s
Uninstalled 8 packages in 940ms
░░░░░░░░░░░░░░░░░░░░ [0/3] Installing wheels...
warning: Failed to hardlink files; falling back to full copy. This may lead to degraded performance.
         If the cache and target directories are on different filesystems, hardlinking may not be supported.
         If this is intentional, set `export UV_LINK_MODE=copy` or use `--link-mode=copy` to suppress this warning.
Installed 3 packages in 14ms
 ~ my-lib==0.1.0 (from file:///D:/.../Repositories/uv_issue_16484/my-lib)
 - my-testing-lib==0.1.0 (from git+ssh://git@github.com/Wintreist/uv_issue_16484.git@2dc7aa7257c40029c68346d5d5bc3d7993613fd7#subdirectory=my-testing-lib)
 + my-testing-lib==0.1.0 (from git+ssh://git@github.com/Wintreist/uv_issue_16484.git@cc49101f03715fbe6495f9e0bd142921aca81c5f#subdirectory=my-testing-lib)
 - other-lib==0.1.0 (from git+ssh://git@github.com/Wintreist/uv_issue_16484.git@2dc7aa7257c40029c68346d5d5bc3d7993613fd7#subdirectory=other-lib)
 + other-lib==0.1.0 (from git+ssh://git@github.com/Wintreist/uv_issue_16484.git@cc49101f03715fbe6495f9e0bd142921aca81c5f#subdirectory=other-lib)
 - pyqt-extra-dep-lib==0.1.0 (from git+ssh://git@github.com/Wintreist/uv_issue_16484.git@2dc7aa7257c40029c68346d5d5bc3d7993613fd7#subdirectory=pyqt-extra-dep-lib)
 - pyside6==6.10.0
 - pyside6-addons==6.10.0
 - pyside6-essentials==6.10.0
 - shiboken6==6.10.0
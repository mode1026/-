自动打字 (Auto Typer)
一键将文本内容逐字输入到任何输入框，支持学习通等防粘贴平台。

功能特点
🔤 逐字注入模式：通过 WM_CHAR 消息逐字输入，不被防粘贴检测拦截
🚀 粘贴模式：模拟 Ctrl+V 快速粘贴
📌 窗口置顶：始终保持在最前，方便操作
⏳ 5秒倒计时：点击开始后有充足时间切换到目标窗口
📊 实时进度：显示输入进度和当前字符
使用方法
方式一：直接运行（无需 Python）
下载 dist/自动打字.exe，双击运行即可。

方式二：从源码运行（需要 Python 3.8+）
pip install pyperclip
python auto_type.pyw
或双击 启动自动打字.bat。

操作步骤
将需要输入的文字粘贴到文本框
选择模式：粘贴(Ctrl+V) 或 逐字注入(防检测)
点击 ▶ 开始
在 5 秒倒计时结束前，点击目标输入框
自动输入过程中请勿动键盘鼠标
自行打包
pip install pyperclip pyinstaller
pyinstaller --onefile --windowed --name "自动打字" auto_type.pyw
生成的 exe 文件在 dist/ 目录下。

依赖
Python 3.8+（仅源码运行需要）
pyperclip（仅粘贴模式需要）
tkinter（Python 自带）
注意事项
仅支持 Windows 系统
逐字注入模式使用 PostMessage WM_CHAR，绕过大多数输入钩子检测
使用过程中请勿切换窗口或移动鼠标

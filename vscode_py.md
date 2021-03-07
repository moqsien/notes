- Anaconda3安装

  - 下载
  ```text
  # 最新版即可
  https://mirrors.bfsu.edu.cn/anaconda/archive/
  ```
  - 安装
  ```bash
  # 按照提示安装即可
  sudo sh Anaconda3.sh
  ```
  - 配置国内源
  ```text
  # 配置中科大镜像源或者清华镜像源
  http://mirrors.ustc.edu.cn/help/anaconda.html
  https://mirror.tuna.tsinghua.edu.cn/help/anaconda/
  ```
  - 配置pip源
  ```text
  # 如果不想用conda install，anacoda创建的虚拟环境同样可以用pip install
  # 先在~/.pip/下创建pip.conf
  # 然后在pip.conf中添加如下配置（阿里源）
  [global]
  trusted-host = mirrors.aliyun.com
  index-url = https://mirrors.aliyun.com/pypi/simple
  ```
  - 创建虚拟环境
  ```bash
  conda create -n xxx python=x.x
  # 例如，conda create -n web python=3.9
  # 在.bashrc（若用zsh，则在.zshrc）中设置命令alias
  alias workon="conda activate"
  alias deactivate="conda deactivate"
  ```

- vscode配置

  - python插件
  ```json
  {
    "python.languageServer": "Pylance",
    "python.autoUpdateLanguageServer": true,
    "python.autoComplete.addBrackets": true,
    "python.autoComplete.showAdvancedMembers": true,
    "python.diagnostics.sourceMapsEnabled": true,
    "python.formatting.provider": "autopep8",
    "python.linting.enabled": true,
    "python.showStartPage": false,
    "python.formatting.autopep8Args": [
        "--max-line-length=120",
        "--experimental",
        "--ignore",
        "E402"
    ],
    "python.venvPath": "~/.conda/envs",
    "python.defaultInterpreterPath": "~/.conda/envs/web/bin/python3.9 ",
    "python.analysis.completeFunctionParens": true
  }
  ```
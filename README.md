# 文件结构

TailWindCss文件
./docs/index.html
./docs/hero.png
为什么放在./docs文件夹中？
因为mkdocs需要github action生成静态html，而tailwindcss是静态的，直接利用当前针对mkdocs的这个action将docs目录里的其他文件都复制到gh-pages里去



Mkdocs文件
./mkdocs.yml
./docs/home.md
./docs/about.md
./nested/xxx



操作：
    - 流程：
        git branch [main]中进行编辑，提交后git actions（[Deploy MkDocs](https://github.com/marketplace/actions/deploy-mkdocs)）自动生成新文件到git branch [gh-pages]，访问https://codush.github.io/tampalte_app_pages可查看更新的网站
    - 具体操作
        - 编辑首页：直接编辑./docs/index.html（需要学习tailwindcss）制作app landing page
        - 编辑帮助文档：添加xxx.md文件，并在mkdocs.yml中编辑文档结构（对应到侧边栏）
        - 提交到git branch main

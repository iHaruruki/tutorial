---
title: "Hello LaTeX"
lang: "ja"
parent: "LaTex"
nav_order: 2
permalink: "/latex/hello_latex/"
---

1. Docker DesktopまたはPowerShellを開く
2. USBメモリからコピーした`latex_ws`に移動する
```powershell
cd "$HOME\Documents\latex_ws"
```
3. `latex_ws`のフォルダ内を確認する
```powershell
Get-ChildItem
```
出力結果：
```text
Directory: C:\Users\your-name\Documents\latex_ws

Mode   LastWriteTime   Length Name
----   -------------   ------ ----
-a---  ...             ...    main.tex
-a---  ...             ...    build.sh
```
4. `main.tex`を開く（お好きなエディタで開いてください）
```powershell
notepad .\main.tex
```

5. `main.tex`に以下の内容を記述する
```tex
\documentclass{jsarticle}
\begin{document}

Hello LaTex

アインシュタインは $E=mc^2$といった．

\end{document}
```

6. Build（pdfを生成する）
```powershell
docker run --rm -v "${PWD}:/work" -w /work iharuruki/ubuntu2404-latex bash -c "bash ./build.sh"
```
> [!NOTE]
> 上記コマンドは`main.tex`と`build.sh`があるディレクトリであれば，どこでも実行できます

7. PDFを確認する
- `C:\Users\your-name\Documents\latex_ws`に`build`フォルダが作られる
- エクスプローラーで`C:\Users\your-name\Documents\latex_ws\build`を開き`main.pdf`を確認
生成されたPDF
<img src="../../assets/images/latex/01_main.png" alt="01_main" width="80%">
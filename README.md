# Monterey, Appleシリコン(M1)/arm64 対応版 cooViewer
依存する XADMaster と UniversalDetector を submodule 化して簡単にビルドできるようにしただけ。
自分でビルドできる方向け(要: Xcode, git)、バイナリは配布しません。
ビルド方法は後述。

2022/08 現在の XADMaster を持ってきているので RAR5 アーカイブも扱える。

<br>

## 開発, 確認環境
- MacBook Pro (2021, M1) + Monterey -> Sonoma
- MacBook Pro (2018, Intel) + Monterey

## ビルド
### CLI
```
$ git clone --recursive https://github.com/plife18/cooViewer.git
$ cd cooViewer
$ xcodebuild -configuration Deployment [-arch x86_64/arm64]
```
ビルドに成功すると `cooViewer/build/Deployment` 以下に `cooViewer.app` ができる。
`-arch` 以下を省略すると x86_64/arm64 のユニバーサルバイナリ２ができる。
`-arch` を指定する場合は自分の環境に合わせて指定する。
<br>
\# Apple系の開発者ではなく Xcode 的な流儀は知らないので、configuration の "Deployment" が適切なのか否かは不明。

### GUI: Xcode.app
1. cooViewer/cooViewer.xcodeproj を開く。
1. メニュー → Build (or Cmd+B)
1. 左ペインの Project Nagivator: cooViewer/Products/cooViewer.app の右クリックから "Show in Finder" でビルドした app が見つかる。

\# configuration: "Development" が適用され、操作中環境用ビルドができる、多分。Apple系の開発者ではないので(略)。


<br>
<br>
以下、fork 元の README.md

---
---
---
<br>
<br>


# cooViewer1.2b
https://coo-ona.github.io/cooViewer/

## 開発環境
MacBook Pro (2.3GHz/16GB)<br>
MacOS X 10.14.5

## 操作方法
https://coo-ona.github.io/cooViewer/manual.html

## アンインストール
・アプリ本体<br>
・/Users/(ユーザー名)/ライブラリ/Preferences/jp.coo.cooViewer.plist<br>
を消してください

## 著作権、免責等
cooViewerはMITライセンスです。
ライセンスについては添付のLicence.txtを参照してください。

このソフトウェアはXAD library system ( http://sourceforge.net/projects/libxad/ ) を使用しています。<br>
ライセンスについては添付のLicence_xad.txtを参照してください。

このソフトウェアはRemote Control Wrapper ( http://www.martinkahr.com/source-code/ ) を使用しています。<br>
ライセンスについては添付のLicence_RemoteControlWrapper.txtを参照してください。

デフォルトの書類アイコンは新・mac板 オナニー用画像ビューアー Part4の971さんに作成していただきました。

64bit化対応にあたり、スレの皆様をはじめ、多くの方にご協力いただきました。ありがとうございます。
また、nibをxibに変換いただいたkanjitalk755さんには特に感謝申し上げます。
---
sidebar_position: 1
---

# 導入方法
---

## 導入に必要なもの {#requirements}
- Unity 2022.3.22f1
- Gesture Manager (推奨)
- Av3 Emulator (アバターギミックを使用する場合は必須、合わせてGesture Managerも)
- Very Animation や Avapo! などのポージングツール（推奨）。なければアニメーションデータセット

## Avagraphyの導入方法 {#installation}
1. Unityプロジェクトを開く
1. Avagraphy_vx.x.x.unitypackageをインポート  
自動でPost Processing Stack v2もインポートされます。

## 撮影の準備 {#preparation}
### 1. 撮影用のアバターとマテリアルを作成する
まず、アバターをCtrl+Dで複製します。（Modular Avatarを使用している場合は、アバターを選択し `右クリック > Modular Avatar > Manual Bake Avatar` します。AvaPo!の場合も同様の案内があるはずです）  
次に複製されたアバターを選択し、`Unity上部メニュー > ツール > Avagraphy > Material Duplicator` を開きます。  
アバターに含まれるマテリアルが全て選択したフォルダに複製され、置き換えられます。

### 2. Avagraphyをシーン上に配置する
    1. Hierarchy上で `右クリック>Avagraphy>セットアップ` または `Unity上部メニュー>ツール>Avagraphy>Setup (Select) Avagraphy` を選択
    1. `[Avagraphy]` という名前のGameObjectが生成されるので、選択してアバター欄に撮影したいアバターを指定する

### 3. Gesture ManagerやAv3 Emulatorを導入する (任意)
アバターの動きを再現したい場合は、Gesture ManagerやAv3 Emulatorを導入してください。  
PhysBoneを使用したいだけの場合はこれらは不要です。

### [撮影の流れ](../photographing) に続きます。
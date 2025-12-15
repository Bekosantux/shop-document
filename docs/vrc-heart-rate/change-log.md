---
sidebar_position: 999
toc_max_heading_level: 2
---

# 更新履歴

## 2025/12/15 v1.0.5
---
### 修正
- Additiveレイヤーを使用しているギミック（特に呼吸アニメーションなど）が存在する場合、Sit判定でVRC Heart Rateを使用したギミックが壊れることがある問題を修正
- パラメータ名を `VCRHR/Local_Trigger` から `VRCHR/Local_Trigger` に変更（タイポ）

## 2025/9/21 v1.0.4
---
### 修正
- Avatar Optimizer使用時にNDMFコンソールに警告が出る問題と、不要なゲームオブジェクトが残る問題を修正


## 2025/9/14 v1.0.3
---
### 修正
- 英語など一部環境でコンパイルエラーが発生する問題を修正

## 2025/9/3 v1.0.2
---
### 変更
- マニュアルプレハブ
  - 初期心拍数を65に変更
  - 心拍数の保存を有効化
- OSCプレハブ
  - マニュアル心拍数とマニュアル強制化オプションの保存を有効化

## 2025/9/3 v1.0.1
---
### 変更
- プレハブ `VRCHeartRate_Core_Manual`
  - オブジェクト名 `VRCMenu` → `VRCMenu_VRCHeartRate`
  - メニュー名 `Heart Rate Manual Control` → `Heart Rate`
- プレハブ `VRCHeartRate_Core`
  - オブジェクト名 `VRCMenu` → `VRCMenu_VRCHeartRate`

## 2025/9/3 v1.0.0
---
- 初期リリース
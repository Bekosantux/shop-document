---
sidebar_position: 7
---

# パラメーターについて
<hr/>

- HR (OSCのみ)  
心拍数のInt値。0～255まで。  
**改変におすすめです。** 寝落ち判定など、一定の心拍数を条件にするなどのギミックを組む際におすすめです。

- HBG/HRCounter_Bool  
心拍計を表示するかどうかのBool値。

- HBG/Sound_Bool  
心音を再生するかどうかのBool値。

- HBG/SoundRadius_Float  
心音の聞こえる範囲を調整するためのFloat値。

- HBG/ManualHR_Float  
心拍数をラジアルパペットで操作するためのFloat値。心拍数50～177の範囲で0～1に変換します。  
(改変はなるべく下のHBG/Local_FullHR_Floatを使用してください)

- HBG/HRCounterFlash_Bool  
心拍計を明滅させるかどうかのBool値。

- HBG/AutoControlHR_Bool (OSCのみ)  
OSC信号で心拍数をコントロールするかのBool値。

Local_ の接頭辞がついているものはローカル動作です。

- HBG/Local_AdjustingRadius_Bool  
心音範囲を変更中かどうかのBool値。音源範囲を示す球の表示に使われます。

- HBG/Local_FullHR_Float  
HRが0～1の範囲に変換されたFloat値。高精度で同期されます。  
**改変におすすめです。** 顔の赤みを変えるなど、心拍数に比例したギミックなどを組む際に使用できます。

- HBG/Local_Mute_Bool  
自分の心音をミュートにするかどうかのBool値。

- HBG/Local_ListenOwnHB_Bool  
自分の心音を聞くかどうかのBool値。

- HBG/Local_nSoundRadius  
アバタースケーリングに心音範囲を追従させるために使われます。

- HBG/Local_nBeatTime  
心音の再生時間を正規化した数値が入ります。  
**改変におすすめです。** アニメーションのMotion Timeに使用することで、任意のアニメーションを心音に合わせて再生することができます。

- ScaleFactor  
VRChat標準パラメータ。アバタースケーリングでの整合性を保つために使用されます。

- HBG/Blend  
Direct Blend Tree (DBT) を有効化するために使われます。変更しないでください。
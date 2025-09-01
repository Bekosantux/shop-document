---
sidebar_position: 7
---

# パラメーターについて
<hr/>

心拍数などを用いたギミックを自作したい場合は、[VRC Heart Rateのパラメーター](/ShopDoc/VRCHeartRate/development/#パラメーターについて)をご覧ください。

- HBG/HRCounter_Bool  
心拍計を表示するかどうかのBool値。

- HBG/Sound_Bool  
心音を再生するかどうかのBool値。

- HBG/SoundRadius_Float  
心音の聞こえる範囲を調整するためのFloat値。

- HBG/HRCounterFlash_Bool  
心拍計を明滅させるかどうかのBool値。

Local_ の接頭辞がついているものはローカル動作です。

- HBG/Local_Mute_Bool  
自分の心音をミュートにするかどうかのBool値。

- HBG/Local_ListenOwnHB_Bool  
自分の心音を聞くかどうかのBool値。

- HBG/Local_AdjustingRadius_Bool  
心音範囲を変更中かどうかのBool値。音源範囲を示す球の表示に使われます。

- HBG/Local_nSoundRadius  
アバタースケーリングに心音範囲を追従させるために使われます。

- ScaleFactor  
VRChat標準パラメータ。アバタースケーリングでの整合性を保つために使用されます。

- HBG/Blend  
Direct Blend Tree (DBT) を有効化するために使われます。変更しないでください。
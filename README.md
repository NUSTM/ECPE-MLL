
# End-to-End Emotion-Cause Pair Extraction based on SlidingWindow Multi-Label Learning

This repository contains the code for our EMNLP 2020 paper:


Zixiang Ding, Rui Xia, Jianfei Yu. End-to-End Emotion-Cause Pair Extraction based on SlidingWindow Multi-Label Learning. EMNLP 2020.

Please cite our paper if you use this code.

## Dependencies

- **Python 2** (tested on python 2.7.15)
- [Tensorflow](https://github.com/tensorflow/tensorflow) 1.13.1
- BERT (The pretrained BERT model "[BERT-Base, Chinese](https://storage.googleapis.com/bert_models/2018_11_03/chinese_L-12_H-768_A-12.zip)" is required. Our model is built based on
this implementation: https://github.com/google-research/bert)




## Usage

python main.py

## Results

Experimental results under two different data split setttings:

- 10-fold cross-validation, following [NUSTM/ECPE](https://github.com/NUSTM/ECPE) (already reported in our paper)

<table align='center' border=0 cellpadding=0 cellspacing=0 width=722 style='border-collapse:
 collapse;table-layout:fixed;width:542pt'>
 <col width=146 style='mso-width-source:userset;mso-width-alt:5205;width:110pt'>
 <col width=64 span=9 style='width:48pt'>
 <tr height=19 style='height:14.4pt'>
  <td align='center'rowspan=2 height=38 class=xl636700 width=146 style='height:28.8pt;
  width:110pt'>Approach</td>
  <td align='center'colspan=3 class=xl636700 width=192 style='border-left:none;width:144pt'>Emotion-Cause
  Pair Ext.</td>
  <td align='center'colspan=3 class=xl636700 width=192 style='border-left:none;width:144pt'>Emotion Ext.</td>
  <td align='center'colspan=3 class=xl636700 width=192 style='border-left:none;width:144pt'>C<font
  class="font56700">ause Ext.</font></td>
 </tr>
 <tr height=19 style='height:14.4pt'>
  <td align='center'height=19 class=xl666700 style='height:14.4pt;border-top:none;border-left:
  none'>P</td>
  <td align='center'class=xl666700 style='border-top:none;border-left:none'>R</td>
  <td align='center'class=xl666700 style='border-top:none;border-left:none'>F1</td>
  <td align='center'class=xl666700 style='border-top:none;border-left:none'>P</td>
  <td align='center'class=xl666700 style='border-top:none;border-left:none'>R</td>
  <td align='center'class=xl666700 style='border-top:none;border-left:none'>F1</td>
  <td align='center'class=xl666700 style='border-top:none;border-left:none'>P</td>
  <td align='center'class=xl666700 style='border-top:none;border-left:none'>R</td>
  <td align='center'class=xl666700 style='border-top:none;border-left:none'>F1</td>
 </tr>
 <tr height=19 style='height:14.4pt'>
  <td align='center'height=19 class=xl636700 style='height:14.4pt;border-top:none'>ECPE-MLL(ISML)</td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.7090</td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.6441</td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.674<font
  class="font56700">0</font></td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.8582</td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.8429</td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.85<font
  class="font56700">00</font></td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.7248</td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.6702</td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.695<font
  class="font56700">0</font></td>
 </tr>
<tr height=19 style='height:14.4pt'>
  <td align='center'height=19 class=xl636700 style='height:14.4pt;border-top:none'>ECPE-MLL(BERT)</td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.7700</b>  </td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.7235</b> </td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.7452</b> </td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.8608</b> </td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.9191</b> </td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.8886</b> </td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.7382</b> </td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.7912</b> </td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.7630</b> </td>
 </tr>
</table>


- Randomly sampling train/validation/test sets with 8:1:1 proportion 20 times, following [HLT-HITSZ/TransECPE](https://github.com/HLT-HITSZ/TransECPE)
<table align='center' border=0 cellpadding=0 cellspacing=0 width=722 style='border-collapse:
 collapse;table-layout:fixed;width:542pt'>
 <col width=146 style='mso-width-source:userset;mso-width-alt:5205;width:110pt'>
 <col width=64 span=9 style='width:48pt'>
 <tr height=19 style='height:14.4pt'>
  <td align='center'rowspan=2 height=38 class=xl636700 width=146 style='height:28.8pt;
  width:110pt'>Approach</td>
  <td align='center'colspan=3 class=xl636700 width=192 style='border-left:none;width:144pt'>Emotion-Cause
  Pair Ext.</td>
  <td align='center'colspan=3 class=xl636700 width=192 style='border-left:none;width:144pt'>Emotion Ext.</td>
  <td align='center'colspan=3 class=xl636700 width=192 style='border-left:none;width:144pt'>C<font
  class="font56700">ause Ext.</font></td>
 </tr>
 <tr height=19 style='height:14.4pt'>
  <td align='center'height=19 class=xl666700 style='height:14.4pt;border-top:none;border-left:
  none'>P</td>
  <td align='center'class=xl666700 style='border-top:none;border-left:none'>R</td>
  <td align='center'class=xl666700 style='border-top:none;border-left:none'>F1</td>
  <td align='center'class=xl666700 style='border-top:none;border-left:none'>P</td>
  <td align='center'class=xl666700 style='border-top:none;border-left:none'>R</td>
  <td align='center'class=xl666700 style='border-top:none;border-left:none'>F1</td>
  <td align='center'class=xl666700 style='border-top:none;border-left:none'>P</td>
  <td align='center'class=xl666700 style='border-top:none;border-left:none'>R</td>
  <td align='center'class=xl666700 style='border-top:none;border-left:none'>F1</td>
 </tr>
 <tr height=19 style='height:14.4pt'>
  <td align='center'height=19 class=xl636700 style='height:14.4pt;border-top:none'>ECPE-MLL(ISML)</td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.6725</td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.6248</td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.6471</td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.8415</td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.8212</td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.8310</td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.6864</td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.6443</td>
  <td align='center'class=xl646700 style='border-top:none;border-left:none'>0.6639</td>
 </tr>
<tr height=19 style='height:14.4pt'>
  <td align='center'height=19 class=xl636700 style='height:14.4pt;border-top:none'>ECPE-MLL(BERT)</td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.7488</b>  </td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.6976</b> </td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.7220</b> </td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.8465</b> </td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.8990</b> </td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.8717</b> </td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.7051</b> </td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.7704</b> </td>
  <td align='center'class=xl656700 style='border-top:none;border-left:none'> <b>0.7358</b> </td>
 </tr>
</table>

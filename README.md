# 精度比較
試した時系列順に表記しています  
★が今回提出したものです (submit_LightGBM_NaN_encoding_2_0_tuning.ipynb, submit_LightGBM_NaN_encoding_2_0_tuning.csv)

## submit_rf.ipynb
ランダムフォレスト  
**RMSE: 0.6326244864434752**

## submit_GBDT.ipynb
GBDT xgboost(NaNを-99に変換)  
**RMSE: 0.610822959180329**

## submit_GBDT_NaN.ipynb
GDBT xgboost(NaNのまま)  
**RMSE: 0.6042383633971182**

## submit_GBDT_NaN_encoding.ipynb
GDBT xgboost(NaNのまま，encoding多め)  
**RMSE: 0.6044626823948162**

## submit_GBDT_NaN_encoding_2.ipynb
GDBT xgboost(NaNのまま，encoding少し減らした(2))  
**RMSE: 0.6019717685235362**

## submit_GBDT_NaN_encoding_3.ipynb
GDBT xgboost(NaNのまま，encoding少し調整(3))  
**RMSE: 0.6028445518316041**

## submit_rf_encoding_3.ipynb
ランダムフォレスト(encoding(3))  
**RMSE: 0.6285389042045287**

## ~~submit_GBDT_NaN_encoding_2_select.ipynb~~
GBDT(特徴量選択)  
途中でエラーを吐いたため断念  
**RMSE:**

## submit_GBDT_NaN_encoding_2_0.ipynb
GDBT xgboost(NaNのまま，encoding少し減らした(2))  
負の値と予測されたものは0に修正  
**RMSE: 0.5999766265357284**

## submit_GBDT_NaN_encoding_2_0_NaNinfo.ipynb
GDBT xgboost(NaNのまま，encoding少し減らした(2))  
負の値と予測されたものは0に修正  
NaNの数を特徴量に追加  
**RMSE: 0.6034448592873829**

## submit_GBDT_NaN_encoding_2_0_cut.ipynb
GDBT xgboost(NaNのまま，encoding少し減らした(2))  
負の値と予測されたものは0に修正  
ほとんど同じ値のカラムを削除  
**RMSE: 0.6096558872255264**

## submit_GBDT_NaN_encoding_2_0_Kolmogorov–Smirnov.ipynb
GDBT xgboost(NaNのまま，encoding少し減らした(2))  
負の値と予測されたものは0に修正  
コルモゴロフ-スミルノフ検定を利用して特徴量を選択  
**RMSE: 0.7573977795833612**

## submit_LightGBM_NaN_encoding_2_0.ipynb
GDBT LightGBM(NaNのまま，encoding少し減らした(2))  
負の値と予測されたものは0に修正  
**RMSE: 0.5908967018000341**

## ★submit_LightGBM_NaN_encoding_2_0_tuning.ipynb
GDBT LightGBM(NaNのまま，encoding少し減らした(2))  
負の値と予測されたものは0に修正  
ハイパーパラメータを少し変更 ("colsample_bytree": 0.7)  
**RMSE: 0.5892398722162967**

## submit_LightGBM_NaN_encoding_2_0_optuna.ipynb
GDBT LightGBM(NaNのまま，encoding少し減らした(2))  
負の値と予測されたものは0に修正  
optunaを実装  
**RMSE: 0.5899869311047072**

# 所感
実践的に自ら回帰モデルを実装したのが初めてだったため，かなり苦戦しました．精度を上げるために試行錯誤をする大変さを身にしみて感じました．  

# 雑なメモ
参考にしたリンクなどを雑にまとめています  
https://www.notion.so/74b670feee034e0cb461ffb9630d7ebd

# 参考文献
[1]Kaggleで勝つデータ分析の技術  
[2]機械学習のための特徴量エンジニアリング

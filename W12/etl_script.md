import pandas as pd
import numpy as np

RANDOM_SEED = 42  # 固定 seed，任何隨機步驟都要用它，確保可重現
np.random.seed(RANDOM_SEED)

df = pd.read_csv("credit-dirty.csv")

# TODO 逐欄檢查：每一欄都看過缺值、型別、格式、範圍、唯一性、類別是否一致。
#      檢查結果寫進 decision_log.md 第一張表——檢查過但不需要處理的欄位也要列。
# TODO 依 decision_log.md 訂的規則逐欄處理。
#      有排除或隔離資料列的話，要印出筆數與原因，不要「安靜地」丟掉。

# 輸出檔案必須包含 ID, PAY_0, default（系統會檢查），
# 其他欄位也要留著（不要整欄刪掉）；各欄的型別與範圍要符合「欄位規格」檔。
df.to_csv("credit-clean.csv", index=False)

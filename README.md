Dataset
7 cột chính: rating, company_name, job_title (hay job_roles), salary, salaries_reported, location, employment_status. Không có cột kinh nghiệm hay giới tính — các phân tích đã được điều chỉnh phù hợp với điều này.

Thư viện & công nghệ đã dùng
Xử lý dữ liệu: pandas, numpy — đọc CSV, chuẩn hóa cột, loại outlier (1%–99%), fill missing values.
Trực quan hóa: matplotlib, seaborn — Histogram, KDE, Boxplot, Barplot, Scatter, Regplot, Heatmap.
Machine Learning: scikit-learn (LinearRegression, Ridge, Lasso, DecisionTree, RandomForest, GradientBoosting), xgboost, shap — 7 mô hình, cross-validation 5-fold, SHAP TreeExplainer.
Kiểm định thống kê: scipy.stats — ANOVA (f_oneway), T-test (ttest_ind).

Biểu đồ theo từng tầng
Tầng 1: Histogram · KDE · Boxplot phân phối · Barplot lương theo job title · Boxplot nhóm vị trí.
Tầng 2: Bar + Boxplot theo employment status · Scatter + Regplot (rating vs salary) · Barplot lương theo location · Barplot theo job roles · Correlation Heatmap.
Tầng 3: Bar so sánh R²/CV-R²/MAE/MAPE của 7 mô hình · Actual vs Predicted scatter · Residual plot · Feature Importance bar · SHAP summary bar + Beeswarm.
Tầng 4: Grouped bar Actual vs Predicted (5 mẫu) · Error % bar · Line chart Salary Roadmap theo job role · Growth % bar chart.

Kết luận chính
Về lương trung bình (Q1+Q2): phân phối lệch phải, Median phản ánh thực tế tốt hơn Mean, có sự chênh lệch rõ rệt theo vị trí (senior/lead cao hơn đáng kể entry-level).
Về nguyên nhân (Q3): Job Role là yếu tố quan trọng nhất, tiếp theo là Location (chênh lệch địa lý lớn), Employment Status và Company Rating cũng ảnh hưởng có ý nghĩa thống kê.
Về dự đoán (Q4): XGBoost là mô hình tốt nhất, SHAP Values xác định top features ảnh hưởng mạnh nhất đến lương.

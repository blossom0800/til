# Barplot 작성 예시
```
plt.figure(figsize=(15, 3))
sns.barplot(data = df_merge, x="card_company", y="total_score", hue="category")
plt.legend(bbox_to_anchor=(1.05, 1), loc=2, borderaxespad=0.)
```

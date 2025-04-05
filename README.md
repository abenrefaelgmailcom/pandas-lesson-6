# pandas-lesson-6
pandas lesson 6


📘 סיכום עיקרי של השיעור:
✅ 1. פעולות בסיסיות על DataFrame
קריאת קובץ CSV עם pd.read_csv
בדיקת הנתונים עם df.info() ו-df.describe()
המרת טיפוס נתונים עם pd.to_numeric
פעולות על מחרוזות עם .str (למשל: strip, replace, capitalize)
✅ 2. פעולות GroupBy
קיבוץ לפי עמודה/ות עם df.groupby()
שימוש ב- mean(), max(), min(), count() על קבוצות
קיבוץ לפי מספר עמודות: df.groupby(['col1','col2'])
אגגרגציה מתקדמת עם agg() והרצת כמה פונקציות על עמודות שונות
ניהול אינדקסים מרובי רמות אחרי GroupBy
שימוש ב- reset_index() כדי "לשטח" את האינדקס לאחר groupby
✅ 3. טכניקות מתקדמות ב-GroupBy
גישה לקבוצה מסוימת עם get_group()
מציאת ערכים גדולים ביותר בתוך קבוצות עם nlargest()
חיתוך חתכים בתוך אינדקס היררכי עם xs()
סינון קבוצות לפי תנאים
החלפת רמות באינדקס עם swaplevel() וסידור מחדש עם sort_index()
✅ 4. מיזוג DataFrame-ים (Join / Merge)
שימוש ב- pd.merge() עם סוגי הצטרפות שונים: inner, outer, left, right
טיפול בשמות עמודות כפולים עם הפרמטר suffixes
מיזוג לפי שמות עמודות שונים עם left_on ו-right_on
מיזוג מוצלב (קרוס) עם how='cross'
✅ 5. שימוש ב-pd.concat()
חיבור DataFrame-ים לאורך צירים שונים (שורות או עמודות)
✅ 6. מילוי וניקוי נתונים חסרים
מילוי קדימה (ffill())
מילוי אחורה (bfill())
שרשור שיטות מילוי (bfill().ffill() לדוגמה)
🔹 דוגמה מתוך המחברת:

python
Copy
Edit
data = {'A': [1, None, 3, None], 'B': [None, 2, None, 4]}
df = pd.DataFrame(data)

# מילוי קדימה
df_ffill = df.ffill()

# מילוי אחורה
df_bfill = df.bfill()

# שרשור מילוי
df_clean = df.bfill().ffill()
✅ 7. פונקציות לניתוח נתונים
ניתוח שכיחות עם value_counts()
סינון בין ערכים עם between()
יצירת סטטיסטיקות מותאמות אישית עם agg()
סינון עם אינדוקס בוליאני (תנאים כמו df['col'] > 10)


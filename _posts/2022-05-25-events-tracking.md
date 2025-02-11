---
layout: post
title: Events tracking
author: shiran
date: 2022-05-24 19:53:02
intro_paragraph: והפעם נדבר על מיפוי והגדרה של eventים
image: uploads/event.jpg
categories: "#eventstracking"
---


### מה זה Events tracking?<br>
מעקב אחרי אירועים שמשתמש מבצע בזמן שהותו באתר.

### בשביל מה? <br>
על ידי מעקב זה, ניתן לזהות את התנהגות המבקרים, למדוד ולנתח את תנועת הלקוחות. באמצעות החקירה הזאת ניתן לעזור לעסק לקבל החלטות מושכלות יותר לשיפור הנתיבים, כלומר להכוונת תנועת המבקר באתר בכדי שיממש את המטרה אליה העסק חותר.

*דוגמה פשוטה,* <br>
אתר שמציע פריטים למכירה<br>
המטרה: להוביל את המבקר לביצוע רכישה. <br>
על ידי מיפוי האיוונטים כמו צפייה, לחיצה, גלילה וכד׳ של מבקר באתר ניתן להתחקות אחר תנועת המבקרים ולהבין טוב יותר את הנתיב בו המבקרים ״הולכים״ באתר, בעצם מה שלבי הfunnel (כניסה לעמוד הבית-->לחיצה על פריט מסוים--> לחיצה על קנה עכשיו --> מילוי פרטים רלוונטים, כמו כתובת למשלוח, אמצעי תשלום-->ולחיצה על רכישה סופית). <br>
בעזרת המידע הזה, ניתן לנסות להכווין את המבקרים לרכישה הן בצורה של הסרת חסמים-<br>
ראינו שאם כפתור ״קנה עכשיו״ מופיע רק אחרי שלוחצים ״קרא עוד״ פחות אנשים לוחצים עליו לעומת מקרה שהוא מופיע ישירות בכניסה לפריט.<br>
והן בצורה של ניתוב מיטבי-<br>
הצגת ״הצעות נוספות לרכישה״ לאחר הוספת פריט אחד לסל.


### איך מגדירים eventים? <br>

1. מה המטרה? <br>
תחילה, חשוב להבין מה ייחשב בעיניינו כהצלחה? מה הKPIs הרלוונטים שיאפשרו לנו למדוד את אותה הצלחה? ומה עוד נרצה למדוד כדי לדעת אם אנחנו בדרך הנכונה?

2. איך האתר בנוי?<br>
לאחר מכן, נמפה אזורים שונים באתר, אילו סוגי דפים יש לי? (הדגש הוא על סוג הדף ולא מספר הדפים) ואילו סוגי אזורים יש לי בכל דף?

את האזורים האלה נגדיר כקטגוריות שונות - כמו לחצני קישור חיצוניים, לחצני קישור בתוך העמוד, סרטונים, Search bar וכד׳.

3. מה הפעולות שנרצה לנטר?<br>
בשלב הבא, נזהה פעולות בעלי ערך שנרצה לנטר - צפיה בעמוד, גלילה, לחיצה, הקלדה וכד׳
זכרו- לא כל הפעולות חייבות להיות רלוונטיות עבורכם 

השלבים האלו יתנו לנו את שם האיוונט והסוג
השם צריך להיות מספיק ספציפי שלא נתבלבל בינו לבין איוונט אחר ומספיק כללי כדי שאם מחר הטקסט או משהו בעיצוב משנה, זה לא ישנה את האיוונט. 
לדוגמה
name: home_page_view
kind: view

name: item_click<br>
kind: click <br><br>
**ולא** <br>
name: alma_dress_item_click<br>
kind: click<br>
<br>
4. נתונים נוספים<br>
כשלב אחרון, נוסיף את כל המידע הנוסף שניתן לקבל יחד עם הניטור של אותו איוונט - <br>
מי המבקר שלחץ - ID 
מתי הפעולה קרתה - created_at
מה הנתונים שאפשר לדעת על המבקר? - Browser, os, device
מה ביצועי האתר בזמן הפעולה - זמן טעינת העמוד
כתובת העמוד הנוכחי בו בוצעה הפעולה - URL
כתובת העמוד אליה הפעולה שולחת (במקרה של לחיצה לדוגמה) - Target URL
Session ID
וכל מידע רלוונטי נוסף שניתן לדלות.

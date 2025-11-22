# Course Management API

## תאור הפרויקט
המערכת מאפשרת למדריכות לנהל קורסים שונים, ולתלמידות להירשם אליהם.  
כל מדריכה יכולה לפתוח כמה קורסים, כאשר לכל קורס יש שם, רמה, ויום בשבוע.  
תלמידות יכולות להירשם לקורסים דרך מערכת ההרשמה, והמערכת שומרת את פרטי ההרשמה, כולל שם התלמידה ותאריך ההצטרפות.  
המערכת מסייעת בניהול פשוט של קורסים והצגת המדריכה, הקורסים שלה, ומי נרשם לכל קורס.

## ישויות
- מדריכה
- קורס
- הרשמה לקורס
---
## מיפוי
## מדריכה (Instructor)

- **שליפת רשימת המדריכות**  
  `GET https://courses.co.il/instructors`
  
- **שליפת מדריכה לפי מזהה**  
  `GET https://courses.co.il/instructors/1`
  
- **הוספת מדריכה**  
  `POST https://courses.co.il/instructors`
  
- **עדכון מדריכה**  
  `PUT https://courses.co.il/instructors/1`
  
- **מחיקת מדריכה**  
  `DELETE https://courses.co.il/instructors/1`
  
- **עדכון התמחות (פעולה נוספת)**  
  `PUT https://courses.co.il/instructors/1/specialty`

---

## קורס (Course)

- **שליפת רשימת הקורסים**  
  `GET https://courses.co.il/courses`
  
- **שליפת קורס לפי מזהה**  
  `GET https://courses.co.il/courses/1`
  
- **הוספת קורס**  
  `POST https://courses.co.il/courses`
  
- **עדכון קורס**  
  `PUT https://courses.co.il/courses/1`
  
- **מחיקת קורס**  
  `DELETE https://courses.co.il/courses/1`
  
- **שינוי מדריכת הקורס (פעולה נוספת)**  
  `PUT https://courses.co.il/courses/1/instructor`

---

## הרשמות (Enrollments)

- **שליפת רשימת ההרשמות**  
  `GET https://courses.co.il/enrollments`
  
- **שליפת הרשמה לפי מזהה**  
  `GET https://courses.co.il/enrollments/1`
  
- **הוספת הרשמה**  
  `POST https://courses.co.il/enrollments`
  
- **עדכון הרשמה**  
  `PUT https://courses.co.il/enrollments/1`
  
- **מחיקת הרשמה**  
  `DELETE https://courses.co.il/enrollments/1`
  
- **עדכון סטטוס הרשמה (פעולה נוספת)**  
  `PUT https://courses.co.il/enrollments/1/status`

---

## אפשרויות סינון ומיון לשליפות

- **שליפת הרשמות לקורס מסוים**  
  `GET https://courses.co.il/enrollments?courseId=3`
  
- **שליפת הרשמות לפי סטטוס**  
  `GET https://courses.co.il/enrollments?status=Active`
  
- **שליפת קורסים לפי מדריכה מסוימת**  
  `GET https://courses.co.il/courses?instructorId=2`
  Update README with Mapping section


---
name: israeli-fines-fighter
description: "Appeal parking tickets and traffic fines in Israel: generates Hebrew appeal letters, explains deadlines, covers municipal fine codes, speed camera violations, and the points system. Use when a user receives a knasa (fine) and wants to understand their options, draft an appeal, or calculate penalty points. Helps users hit the 30-day cancellation window (bakasha le-bitul) AND the 90-day court-hearing window (bakasha le-hishafet), and avoid the +50% surcharge that kicks in after the 90-day mark."
license: MIT
---

# Israeli Fines Fighter

## Problem

Getting fined in Israel is stressful and confusing. Parking tickets arrive with cryptic violation codes, traffic fines carry penalty points that accumulate toward license suspension, and there are TWO different appeal windows running in parallel for both fine types: a **30-day cancellation request (bakasha le-bitul)** to the prosecutor or municipality, and a **90-day court-hearing request (bakasha le-hishafet)** OR 30 days from the rejection of a cancellation request. After 90 days without action, a +50% surcharge kicks in, then +5% every additional 6 months. This skill helps users hit both windows, decide whether to appeal, and generate a proper Hebrew appeal letter with the right legal grounds.

## Instructions

### Step 1: Identify the Fine Type

Ask the user for the fine details. Israeli fines fall into two main categories:

| Type | Issued By | Hebrew Term | Appeal To |
|------|-----------|-------------|-----------|
| **Parking fine** (knasa chanaya) | Municipal inspector (paqach) | קנס חנייה / דוח חנייה | Municipality (iriya) |
| **Traffic fine** (knasa tnu'a) | Police officer or camera | קנס תנועה / דוח תנועה | Police prosecution (tvia'a) or traffic court |

Key details to collect:
- Fine number (mispar hadoch)
- Date received
- Violation code or description
- Amount in NIS
- Issuing authority (municipality name or "Israel Police")
- Location where the violation occurred
- Whether the user was driving or the vehicle owner

### Step 2: Assess the Deadline

There are TWO appeal mechanisms with separate deadlines, applicable to BOTH parking fines and traffic fines:

| Window | Mechanism | Hebrew | Submitted To |
|---|---|---|---|
| **30 days from receipt** | Cancellation request (essentially clerk review) | בקשה לביטול / בקשת בירור | Municipality (parking) or Police prosecutor (traffic) |
| **90 days from receipt** OR **30 days from rejection of a cancellation request** | Court hearing request | בקשה להישפט | Traffic court / municipal court |

After **day 90** without payment or appeal, the fine carries a **+50% surcharge**, with **+5% every additional 6 months**. The pre-2026 framing of "fine doubles after 30 days" is wrong — surcharge does not start at 30 days, and it is +50% (not 100%).

| Timeline | Status | Action |
|----------|--------|--------|
| **Day 0-30** | Both windows open | Best time to file בקשה לביטול. Many municipalities also offer a 25-50% early-payment discount in this window (varies by city). |
| **Day 31-90** | Cancellation window closed; court-hearing window still open | File בקשה להישפט before day 90, OR if a בקשה לביטול was rejected, file court request within 30 days of the rejection. |
| **Day 90+** | Both standard windows closed; +50% surcharge accrues | Late-appeal exceptions (איחור מוצדק) apply only for hospitalization, military reserve service, or being abroad — see Criminal Procedure Law § 230. Otherwise enforcement via Hotza'a Lapo'al, vehicle-registration block (ikuv rishum), additional fees. |

**For parking fines:** the 30-day clock starts from the date the ticket was placed on the vehicle OR the date a notice was mailed to the registered owner.

**For traffic fines (breirot mishpat):** by default the fine becomes a court conviction at day 90 if no בקשה להישפט was filed.

### Step 3: Evaluate Appeal Grounds

Not every fine is worth appealing. Help the user assess their case:

**Strong grounds for parking fine appeals:**

| Ground | Hebrew Term | Evidence Needed |
|--------|-------------|-----------------|
| Missing or obscured signage | שלט חסר / שלט מוסתר | Photos of the location showing no sign or blocked sign |
| Broken parking meter | מדחן תקול | Photo of meter showing error, receipt attempts |
| Medical emergency | מצב חירום רפואי | Medical documentation with date/time |
| Loading/unloading (commercial) | פריקה וטעינה | Business delivery documentation |
| Incorrect vehicle details on ticket | פרטים שגויים בדוח | The ticket itself showing wrong plate number, color, or make |
| Ticket issued outside enforcement hours | מחוץ לשעות אכיפה | Photo of sign showing hours vs. ticket timestamp |
| Disabled parking permit (valid) | תג נכה בתוקף | Copy of valid disabled parking permit |

**Strong grounds for traffic fine appeals:**

| Ground | Hebrew Term | Evidence Needed |
|--------|-------------|-----------------|
| Vehicle was sold before violation date | הרכב נמכר | Sale contract (heskhem mechira) with date |
| Vehicle was stolen | הרכב נגנב | Police report (tlunat mishtara) |
| Camera malfunction | תקלה במצלמה | Request calibration records from police |
| Emergency circumstances | נסיבות חירום | Documentation (medical records, police report) |
| Driver was someone else (owner liability) | נהג אחר | Statutory declaration (tatzir) identifying the actual driver |

**Weak grounds (usually rejected):**
- "I didn't see the sign" (ignorance of signage is not a defense)
- "I was only parked for a minute" (duration is irrelevant)
- "Everyone parks there" (common practice is not a legal defense)
- "The meter app crashed" (use physical payment as backup)

### Step 4: Generate the Appeal Letter

**For parking fines (bakasha leitul knasa chanaya):**

The appeal letter must be in Hebrew and include:

```
לכבוד
עיריית [שם העירייה]
מחלקת חניה / אגף אכיפה

הנדון: בקשה לביטול דוח חניה מספר [FINE_NUMBER]

1. פרטי הדוח:
   - מספר דוח: [FINE_NUMBER]
   - תאריך: [DATE]
   - מיקום: [LOCATION]
   - מספר רכב: [PLATE_NUMBER]

2. נימוקי הבקשה:
   [SPECIFIC LEGAL GROUNDS - see Step 3]

3. ראיות מצורפות:
   [LIST ATTACHED EVIDENCE]

4. בקשה:
   לאור האמור לעיל, אבקש לבטל את הדוח / להפחית את הקנס.

בכבוד רב,
[NAME]
[ID_NUMBER]
[PHONE]
[DATE]
```

**For traffic fines (bakasha lehisha'fet):**

Traffic fine appeals go to the prosecution or court. The letter structure differs:

```
לכבוד
תביעות משטרת ישראל / בית המשפט לתעבורה

הנדון: בקשה להישפט בגין דוח תנועה מספר [FINE_NUMBER]

אני הח"מ [NAME], ת.ז. [ID], מבקש/ת להישפט על דוח תנועה מספר [FINE_NUMBER]
שניתן בתאריך [DATE].

נימוקים:
[SPECIFIC LEGAL GROUNDS]

[NAME]
[DATE]
```

### Step 5: Submission Guidance

**Parking fine appeals -- submission channels by municipality:**

| Municipality | Online Portal | In-Person |
|-------------|--------------|-----------|
| Tel Aviv-Yafo | tel-aviv.gov.il (Resident Portal) | 110 Jerusalem Blvd, Jaffa |
| Jerusalem | jerusalem.muni.il | Safra Square, City Hall |
| Haifa | haifa.muni.il | 14 Hassan Shukri St |
| Other municipalities | Check municipal website for online appeal form | Visit city hall parking department |

**Traffic fine options:**
- **Pay the fine:** Online at gov.il (police fine payment service) or at any post office
- **Request a court hearing (bakasha lehisha'fet):** Submit within 90 days. You will receive a court date. You may represent yourself or hire a traffic lawyer (orech din letnu'a)
- **Plea bargain (hasdarei to'en):** Some offenses allow negotiating a reduced fine or fewer points through the prosecution

### Step 6: Point System Impact (Shitat HaNikud)

When the fine is a traffic violation, calculate the point impact:

| Points Accumulated | Consequence |
|-------------------|-------------|
| 12-22 points | Warning letter from licensing authority |
| 22-34 points | Mandatory safe driving course (kurs nehiga bituchit) |
| 22-34 points | Advanced safe-driving course + theory test |
| 34+ points | 24-month license suspension (NOT 3 months) |
| 36 points (or two separate 22-point reaches in 6 years) | 9-month suspension + practical re-test |
| 36+ points | Extended license suspension, re-examination required |

Points expire based on total accumulated count, not severity: **≤20 points clear after 2 years** of clean driving and completion of any required courses; **≥22 points clear after 4 years** under the same conditions. Without completing required courses, points do not expire.

**Common violation point values:**

| Violation | Fine (NIS) | Points |
|-----------|-----------|--------|
| Running a red light | 1,000 | 10 |
| Speeding 21-30 km/h over limit (urban) | 750 | 8 |
| Speeding 31-40 km/h over limit (urban) | 1,500 | 10 |
| Using mobile phone while driving | 1,000 | 8 |
| Not wearing seatbelt | 250 | 2 |
| Illegal overtaking | 500-1,000 | 6-8 |

Note: Fine amounts are updated periodically by ministerial order. Always verify current amounts on gov.il. The amounts above are approximate as of early 2026.

## Gotchas

1. **Municipal vs. police fines are different legal processes.** Parking tickets from a municipal inspector (paqach) follow the municipal appeal process (bakasha leitul). Traffic fines from police or cameras follow criminal traffic law (breirot mishpat). Mixing up the appeal process wastes the deadline.

2. **The 30-day and 90-day deadlines are from receipt date, not violation date.** For mailed notices, receipt date is presumed to be a few days after mailing. If the user says "I got a fine from 2 months ago," clarify when they actually received the notice.

3. **Owner liability (achrayut ba'alim) is the default for camera fines.** The registered vehicle owner receives camera fines regardless of who was driving. The owner can transfer liability by submitting a statutory declaration (tatzir) naming the actual driver within 90 days.

4. **Do NOT fabricate fine amounts.** Israeli fine amounts change by ministerial order and vary by municipality for parking violations. Always advise users to check the amount on their actual fine notice rather than relying on fixed numbers. The amounts in this skill are approximate guidelines.

5. **Appeals are municipality-specific.** Each Israeli municipality has its own appeal form, portal, and process. Do not assume Tel Aviv's process works for Jerusalem or Haifa. Always direct the user to their specific municipality's website.

## Bundled Resources

### references/

- `appeal-grounds.md` -- Comprehensive list of valid appeal grounds with legal basis
- `fine-types.md` -- Israeli fine categories, violation codes, and amount ranges

### scripts/

- `deadline-calculator.py` -- Calculate remaining days in appeal window based on fine date

## Troubleshooting

### "My fine grew because I missed a deadline"

The pre-2026 "fine doubles after 30 days" framing is incorrect. The actual rule:
- Past day 90 without payment or appeal: **+50% surcharge** (not +100%, not at day 30).
- Past 6 months thereafter: **+5% every additional 6 months**.
- Possible additional collection fees, vehicle-registration block (ikuv rishum), and enforcement via Hotza'a Lapo'al.

If still within the 30-day cancellation window or 90-day court window, file the appropriate request immediately. After day 90, late-appeal exceptions (איחור מוצדק) apply only for hospitalization, active reserve service, or being abroad — see Criminal Procedure Law § 230 and document the cause.

### "My fine doubled because I missed the 30-day deadline"
If the deadline passed, the user can still pay the increased amount to avoid further escalation. In exceptional cases (hospitalization, military reserve duty), some municipalities accept late appeals with documentation.

### "I got a camera fine but I wasn't driving"
The vehicle owner must submit a statutory declaration (tatzir) identifying the actual driver. This transfers liability. The declaration must be submitted within 90 days and include the other driver's full name and ID number.

### "I want to go to court over a parking fine"
Parking fines in Israel are administrative, not criminal. The appeal goes to the municipality, not a court. If the municipal appeal is rejected, the next step is filing an administrative appeal (erur minhal'i) with the local court, but this is rarely cost-effective for small fines.

### "How much does a traffic lawyer cost?"
Traffic lawyers in Israel typically charge 1,500-5,000 NIS depending on the violation severity. For minor fines under 500 NIS, self-representation is usually more economical. For fines with 10+ points or license suspension risk, a lawyer may be worthwhile.

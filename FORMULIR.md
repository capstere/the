QDIP Power BI – enkel text- och presentationsguide

Syfte: göra QDIP enkel, konsekvent och snabb att läsa under mötet.
Princip: less is more. Visa vad användaren behöver förstå – inte hur lösningen är byggd.

Den här guiden utgår från de senaste skärmbilderna och den manuellt redigerade PBIP-versionen i 04_PowerBI(2).zip.

────────

0. Regler för hela rapporten

Använd samma språk på alla sidor.

Behåll

• BOARD
• MONTHLY REVIEW
• EHS DETAIL
• QUALITY DETAIL
• DELIVERY DETAIL
• REPORTING
• INFORMATION
• Fiscal month
• KPI-namnen: EHS Checklist, Incident, Amplicon, NRFT, Closed LFI, Delivery Leading, Delivery Lagging.

Använd konsekvent

• DETAILS →
• SOURCE DETAILS →
• LFI DETAILS →
• ACTIVE … ACTIONS
• Date
• Status
• Reason
• Notes
• Target

Ta bort från normalvyn när det inte behövs

• official
• canonical
• selected period
• source population
• source evidence
• saved snapshot
• all reporting dates
• investigate selected record view
• completeness protected
• numerator
• denominator

Tekniska ord får finnas i modellen och i felsökning – inte i användarens standardvy.

Statusord

Använd samma betydelse överallt:

• Green = target met
• Red = needs attention
• N/A = not applicable
• Not reported = missing input/data
• Not expected = not due yet
• Error = data/setup issue

────────

1. INFORMATION

Sidrubrik

Behåll:

INFORMATION · QUICK GUIDE

Rubrik över tabellen

Ändra:

KPI GUIDE · daily result and monthly result

till:

KPI GUIDE

Kolumnrubriker

|Nu            |Ändra till    |
|--------------|--------------|
|Metric        |KPI           |
|Reporting     |Reporting     |
|Daily result  |Daily status  |
|Monthly result|Monthly status|
|Owner         |Owner         |

Tabelltext

EHS Checklist

Reporting

• MANUAL · QDIP Reporting
• Weekdays

Daily status

• Score 33–36 = Green
• 0–32 = Red

Monthly status

• Average ≥33 = Green

Incident

Reporting

• EVENT ONLY
• Report when an incident occurs

Daily status

• 0 = Green
• >0 = Red

Monthly status

• Events in month
• Target 0

Amplicon

Reporting

• EVENT ONLY
• Report when an event occurs

Daily status

• 0 = Green
• >0 = Red

Monthly status

• Events in month
• Target 0

NRFT

Reporting

• MANUAL · QDIP Reporting
• Enter NRFT lots

Daily status

• 0 = Green
• >0 = Red

Monthly status

• NRFT-free ≥98% = Green

Closed LFI

Reporting

• AUTOMATIC · LFI log
• Closure date

Daily status

• 0 = Green
• >0 = Red

Monthly status

• ≤3 closed = Green
• >3 = Red

Delivery Leading

Reporting

• AUTOMATIC
• Snapshot 09:00 · fallback if needed

Daily status

• WIP ≥10h
• 0–3 = Green · >3 = Red

Monthly status

• Average WIP ≤3 = Green

Delivery Lagging

Reporting

• AUTOMATIC
• Snapshot 07:00 · fallback if needed

Daily status

• <20h = Green
• ≥20h = Red

Monthly status

• ≥80% within 20h = Green

Nederdelen

REPORTING DATES

Använd:

> Each calendar cell is a reporting date.  
> Tue–Fri: Lagging refers to the previous day.  
> Monday: Lagging covers Friday–Sunday.

REPORTING

Byt REPORTING & UPDATES till:

REPORTING

Använd:

> Complete Checklist and NRFT before the QDIP meeting.  
> Report Incident and Amplicon only when an event occurs.  
> Delivery updates automatically; fallback is used only when needed.

Statusraden

Ändra till:

• GREEN · target met
• RED · needs attention
• N/A · not applicable
• NOT REPORTED · missing input
• NOT EXPECTED · not due yet
• ERROR · data/setup issue

────────

2. BOARD

BOARD ska vara mötestavlan. Lägg inte mer information här.

Övre underrubrik

Ändra:

CARDS: TODAY / DUE · CALENDARS: FISCAL MONTH

till:

TODAY'S STATUS · FISCAL MONTH OVERVIEW

Detail-knappar

Ändra alla:

DETAIL →

till:

DETAILS →

Kalenderrubriker

|Nu                           |Ändra till         |
|-----------------------------|-------------------|
|CHECKLIST — LEADING          |CHECKLIST          |
|INCIDENT + AMPLICON — LAGGING|INCIDENT + AMPLICON|
|NRFT — LAGGING               |NRFT               |
|LFI — LAGGING                |CLOSED LFI         |
|DELIVERY — LEADING           |DELIVERY LEADING   |
|DELIVERY — LAGGING           |DELIVERY LAGGING   |

Nedersta visualer

|Nu                                              |Ändra till             |
|------------------------------------------------|-----------------------|
|Checklist - Daily score vs target: Current month|CHECKLIST · DAILY SCORE|
|NRFT - Top Causes: Current month                |NRFT · REASONS         |
|Closed LFI: Current month                       |CLOSED LFI · THIS MONTH|
|HOT LOTS WIP ≥10h                               |ORDERS WAITING ≥10h    |
|Delivery Lagging ≥20h                           |LATE ORDERS ≥20h       |
|ACTIONS — EHS · QUALITY · DELIVERY · TOP 5      |ACTIONS · TOP 5        |

────────

3. MONTHLY REVIEW

Huvudrubrik över matrisen

Ändra:

OFFICIAL FISCAL RESULTS · results, coverage and period state are separate

till:

FISCAL MONTH RESULTS

Hjälptext

Använd:

Compare KPI results by fiscal month. Missing or incomplete reporting is shown.

Filter

|Nu                          |Ändra till|
|----------------------------|----------|
|Review year                 |Year      |
|Review months · multi-select|Months    |

Matrisens första kolumner

|Nu        |Ändra till|
|----------|----------|
|Area      |Section   |
|MetricName|KPI       |

Nederdelen

Ändra:

Selected cell

till:

SELECTED RESULT

Text:

Select a KPI result above to see its period, target and details.

Ändra:

Investigate month → open a detail page

till:

DETAIL MONTH

Text:

Choose the month to use on the detail pages.

Matrisens celltext

Här behövs en DAX-ändring. Se avsnitt 10. DAX.

Målet är:

35.6 avg score · Green
25/25 reported

eller:

67.3% within 20h · Red
28/28 reported

Event-only och LFI ska inte repetera teknisk information i varje cell.

────────

4. DELIVERY DETAIL

Knapp

Ändra:

OPEN SOURCE DETAIL →

till:

SOURCE DETAILS →

KPI-kort

|Nu             |Ändra till     |
|---------------|---------------|
|Leading average|Avg WIP ≥10h   |
|Leading status |Leading status |
|Within20 %     |Within 20h     |
|Lagging status |Lagging status |
|Total lots     |Total lots     |
|Within20 lots  |Within 20h lots|
|Late ≥20h lots |Late ≥20h lots |

Förklaring under korten

Byt den långa texten mot:

Selected month · Leading target ≤3 avg WIP · Lagging target ≥80% within 20h

Visualrubriker

|Nu                                                          |Ändra till                       |
|------------------------------------------------------------|---------------------------------|
|LEADING · daily saved snapshots                             |LEADING · DAILY WIP ≥10h         |
|LAGGING · cumulative month vs target                        |LAGGING · MONTH-TO-DATE VS TARGET|
|LATE ORDERS · current source evidence for selected due dates|LATE ORDERS · CURRENT SOURCE DATA|

Late Orders – kolumner

|Nu         |Ändra till   |
|-----------|-------------|
|Review date|Review date  |
|Order      |Order        |
|LSP        |LSP          |
|Total h    |Lead time (h)|
|Main stage |Main stage   |
|Issue      |Issue        |

Text under Late Orders

Använd endast:

Current source data may differ from saved results if the source changes later.

Ta bort teknisk text om blank/error från huvudsidan.

Coverage

Ändra:

SNAPSHOT COVERAGE

till:

LEADING COVERAGE

Actions

Ändra:

ACTIVE DELIVERY ACTIONS · all reporting dates

till:

ACTIVE DELIVERY ACTIONS

────────

5. QUALITY DETAIL

KPI-kort

|Nu                                  |Ändra till              |
|------------------------------------|------------------------|
|NRFT LOTS                           |NRFT LOTS               |
|Manual reported numerator           |Reported NRFT lots      |
|TOTAL LOTS                          |TOTAL LOTS              |
|Official saved denominator          |Used for NRFT-free %    |
|NRFT FREE · PERIOD                  |NRFT-FREE               |
|Target ≥98% · completeness protected|Target ≥98%             |
|LFI CLOSED · PERIOD                 |CLOSED LFI              |
|Target ≤3 · by closure date         |Target ≤3 · closure date|

Reporting coverage

Ändra exempelvis:

Complete to date: 35/35 due dates reported

till:

NRFT REPORTING · Complete · 35/35 dates

Väljare

Ändra:

Records to investigate

till:

VIEW

Behåll:

• Deviations
• All reported

Ändra:

• Missing / invalid → Missing / issues

Visualrubriker

|Nu                                     |Ändra till                  |
|---------------------------------------|----------------------------|
|NRFT · DAILY REPORTED COUNT            |NRFT · LOTS REPORTED BY DATE|
|NRFT · INVESTIGATE SELECTED RECORD VIEW|NRFT DETAILS                |

Tabellkolumner

|Nu              |Ändra till|
|----------------|----------|
|Reporting date  |Date      |
|Data state      |Status    |
|NRFT            |NRFT lots |
|Recorded reasons|Reason    |
|Notes           |Notes     |

LFI-text

Använd:

Closed LFI is based on the LFI log and closure date.

Knapp

Ändra:

OPEN LFI RECORDS →

till:

LFI DETAILS →

Actions

Ändra:

ACTIVE QUALITY ACTIONS · ALL DATES

till:

ACTIVE QUALITY ACTIONS

────────

6. EHS DETAIL

KPI-kort

|Nu                                  |Ändra till       |
|------------------------------------|-----------------|
|CHECKLIST · PERIOD AVERAGE          |CHECKLIST AVERAGE|
|Target 33–36 · reported daily scores|Target 33–36     |
|INCIDENT · PERIOD EVENTS            |INCIDENTS        |
|Target 0 · no event is valid zero   |Target 0         |
|AMPLICON · PERIOD EVENTS            |AMPLICON EVENTS  |
|Target 0 · no event is valid zero   |Target 0         |

Reporting coverage

Ändra exempelvis:

Complete to date: 1/1 due dates reported

till:

CHECKLIST REPORTING · Complete · 1/1 dates

Väljare

Ändra:

Records to investigate

till:

VIEW

Behåll:

• Deviations
• All reported

Ändra:

• Missing / invalid → Missing / issues

Checklist

Ändra:

CHECKLIST · DAILY SCORE vs TARGET

till:

CHECKLIST · DAILY SCORE

Ändra:

CHECKLIST · INVESTIGATE SELECTED RECORD VIEW

till:

CHECKLIST DETAILS

Checklist-tabell

|Nu              |Ändra till|
|----------------|----------|
|Reporting date  |Date      |
|Data state      |Status    |
|Score           |Score     |
|Recorded reasons|Reason    |
|Notes           |Notes     |

Events

Ändra:

INCIDENT + AMPLICON · ACTUAL EVENTS (including events without a recorded reason)

till:

INCIDENT & AMPLICON EVENTS

Kolumner:

|Nu              |Ändra till|
|----------------|----------|
|Reporting date  |Date      |
|Metric          |Event     |
|Count           |Count     |
|Recorded reasons|Reason    |
|Notes           |Notes     |

Actions

Ändra:

ACTIVE EHS ACTIONS · ALL DATES

till:

ACTIVE EHS ACTIONS

────────

7. CLOSED LFI · DETAILS

Sidrubrik

Ändra:

LFI RECORDS · CLOSED INVESTIGATIONS

till:

CLOSED LFI · DETAILS

KPI-kort

Ändra:

LFI CLOSED · PERIOD

till:

CLOSED LFI

Ändra:

Target ≤3 · closure date, not occurrence date

till:

Target ≤3 · based on closure date

Hjälptext

Använd:

Select an LFI to view its summary, root cause and assignable cause.

Rubriker

|Nu                                    |Ändra till            |
|--------------------------------------|----------------------|
|CLOSED INVESTIGATIONS · SOURCE RECORDS|CLOSED LFI RECORDS    |
|SELECTED LFI · FULL SUMMARY           |SELECTED LFI · SUMMARY|
|Source summary                        |Summary               |

Placeholder

Använd:

Select an LFI to view its summary.

Text under tabellen

Använd:

LFI is grouped by closure date. Closure date is not the incident date.

Actions

Ändra:

ACTIVE QUALITY ACTIONS · ALL DATES

till:

ACTIVE QUALITY ACTIONS

────────

8. DELIVERY · SOURCE DETAILS

Sidrubrik

Ändra:

DELIVERY · SOURCE DETAIL

till:

DELIVERY · SOURCE DETAILS

Tillbaka-knapp

Ändra:

← OFFICIAL PERIOD RESULTS

till:

← DELIVERY DETAIL

Current WIP

Ändra:

CURRENT WIP ≥10h · live now, independent of selected month

till:

CURRENT WIP ≥10h

Liten text:

Live view · not affected by selected month

Ändra:

Current source: no eligible WIP ≥10h

till:

No current WIP ≥10h

Kolumner

|Nu           |Ändra till   |
|-------------|-------------|
|Order        |Order        |
|LSP / batch  |LSP / batch  |
|Material     |Material     |
|IPT LT h     |Lead time (h)|
|Current stage|Current stage|

Test / packing

Ändra hjälptexten till:

Select an order to view test and packing details.

Text under WIP

Ersätt den långa tekniska texten med:

Current WIP may differ from earlier saved results.

Late Orders

Ändra:

LATE ORDERS · selected due reporting dates · source population

till:

LATE ORDERS · CURRENT SOURCE DATA

Kolumn:

• Total h → Lead time (h)

Process time

Ändra:

PROCESS TIME · average h / late lot

till:

PROCESS TIME · AVERAGE HOURS

Text:

Shows average stage duration. Missing durations are left blank.

Selected late order

Ändra:

SELECTED LATE ORDER · process durations and source error text

till:

SELECTED LATE ORDER · DETAILS

Kolumner:

|Nu        |Ändra till   |
|----------|-------------|
|Test h    |Testing (h)  |
|Compile h |Compiling (h)|
|Review h  |Review (h)   |
|Main stage|Main stage   |

Source error

Behåll rubriken:

SOURCE ERROR TEXT

Placeholder:

Select a late order above to view its source error text.

Om den tekniska Source query feedback-rutan är tom i normal användning:

• dölj den i normalvyn, eller
• ge den ett tydligt användarsyfte.

Lämna inte en tom teknisk ruta bara för att den finns.

────────

9. REPORTING

Det här är inmatnings-/rapportvyn. Den ska vara ännu enklare än Power BI-sidorna.

Titel

Behåll:

QDIP Reporting

Ingress

Ändra till:

Before the QDIP meeting: complete Checklist and NRFT. Report Incident and Amplicon only when an event occurs.

Ta bort förklaringen om read-only från ingressen. Raderna visar redan vad som är automatiskt.

Kolumnrubriker

|Nu                            |Ändra till|
|------------------------------|----------|
|KPI                           |KPI       |
|CATEGORY / TYPE               |Reporting |
|WHAT TO DO / TODAY’S REPORTING|Today     |

EHS Checklist

Reporting:

• INPUT REQUIRED
• EHS

Today:

• behåll Missing · x/x reported
• behåll aktuellt datum

NRFT

Reporting:

• INPUT REQUIRED
• Quality

Today:

• behåll Missing · x/x reported
• behåll aktuellt datum

Closed LFI

Reporting:

• AUTOMATIC
• Quality

Today:

No manual input

Byt alltså ut:

Automatic in Power BI · no manual value

Delivery Leading

Reporting:

• AUTOMATIC
• Delivery

Today:

• behåll Available · x/x
• behåll datum

Delivery Lagging

Samma struktur som Delivery Leading.

Incident

Reporting:

• EVENT ONLY
• EHS

Today:

Report only when an event occurs

Amplicon

Samma som Incident.

Knappar

Behåll:

• QDIP Input
• Actions
• History

Ingen ytterligare text behövs.

────────

10. DAX

10.1 ÄNDRA: Monthly Review Cell

Det här är den enda nya presentationsändringen som krävs för textstädningen.

Ersätt hela måttet med:

Monthly Review Cell =
VAR __MetricID =
    SELECTEDVALUE ( DimMetric[MetricID] )

VAR __ResultValue =
    [Monthly Review Result]

VAR __StatusText =
    [Monthly Review Status]

VAR __ReportedDates =
    [Monthly Review Reported Dates]

VAR __ExpectedDates =
    [Monthly Review Expected Dates]

VAR __PeriodState =
    [Monthly Review Period Context]

VAR __IsEventOnly =
    __MetricID IN {
        "EHS_INCIDENT",
        "EHS_AMPLICON"
    }

VAR __IsLFI =
    __MetricID = "Q_LFI_CLOSED"

VAR __ResultText =
    SWITCH (
        TRUE (),
        ISBLANK ( __ResultValue ),
            "—",
        __MetricID = "EHS_CHECKLIST",
            FORMAT ( __ResultValue, "0.0" ) & " avg score",
        __MetricID = "D_WIP_10H",
            FORMAT ( __ResultValue, "0.0" ) & " avg WIP",
        __MetricID = "Q_NRFT",
            FORMAT ( __ResultValue, "0.0%" ) & " NRFT-free",
        __MetricID = "D_OVER_20H",
            FORMAT ( __ResultValue, "0.0%" ) & " within 20h",
        __MetricID = "Q_LFI_CLOSED",
            FORMAT ( __ResultValue, "0" ) & " closed",
        FORMAT ( __ResultValue, "0" ) & " events"
    )

VAR __ResultLine =
    __ResultText & " · " & __StatusText

VAR __CoverageLine =
    IF (
        NOT __IsEventOnly
            && NOT __IsLFI
            && NOT ISBLANK ( __ExpectedDates )
            && __ExpectedDates > 0,
        FORMAT ( __ReportedDates, "0" )
            & "/"
            & FORMAT ( __ExpectedDates, "0" )
            & " reported"
    )

VAR __PeriodSuffix =
    IF (
        NOT ISBLANK ( __PeriodState )
            && __PeriodState <> "Ended",
        __PeriodState
    )

VAR __SecondLine =
    SWITCH (
        TRUE (),
        NOT ISBLANK ( __CoverageLine )
            && NOT ISBLANK ( __PeriodSuffix ),
            __CoverageLine & " · " & __PeriodSuffix,
        NOT ISBLANK ( __CoverageLine ),
            __CoverageLine,
        NOT ISBLANK ( __PeriodSuffix ),
            __PeriodSuffix
    )

RETURN
    IF (
        HASONEVALUE ( DimMetric[MetricID] )
            && HASONEVALUE ( 'Monthly Review Period'[FiscalYearMonth] )
            && [Monthly Review Period Visible] = 1,
        __ResultLine
            & IF (
                NOT ISBLANK ( __SecondLine ),
                UNICHAR ( 10 ) & __SecondLine
            )
    )

Förväntade exempel

35.6 avg score · Green
25/25 reported

57.9% within 20h · Red
35/35 reported

1 event · Red

1 closed · Green
In progress

— · Not reported
5/20 reported

Viktigt: detta ändrar presentationen, inte [Monthly Review Result], [Monthly Review Status] eller coverage-logiken.

────────

10.2 BEHÅLL: Detail Period Context

Den uppladdade manuella versionen har redan den syntaxsäkra varianten.

Om du behöver återställa den, använd:

Detail Period Context =
VAR __PeriodLabel =
    SELECTEDVALUE ( DimDate[FiscalYearMonth], "Selected dates" )

VAR __PeriodStartDate =
    MIN ( DimDate[RefDate] )

VAR __PeriodEndDate =
    MAX ( DimDate[RefDate] )

RETURN
    IF (
        ISBLANK ( __PeriodStartDate ),
        "No reporting dates selected",
        __PeriodLabel
            & " | "
            & FORMAT ( __PeriodStartDate, "dd MMM yyyy" )
            & " – "
            & FORMAT ( __PeriodEndDate, "dd MMM yyyy" )
    )

Ingen ytterligare ändring behövs här om den redan fungerar.

────────

10.3 ÄNDRA INTE KPI-LOGIKEN I DETTA PASS

Behåll nuvarande:

• Monthly Review Status
• Monthly Review Result
• Monthly Review Coverage State
• Monthly Review Coverage
• Delivery Leading/Lagging-resultat
• NRFT-resultat
• EHS-resultat
• LFI-resultat

Den manuella ZIP-versionen innehåller redan Leading-korrigeringen i Monthly Review Status.

Rensa inte measures i detta pass.

────────

11. Arbetsordning

Gör ändringarna i denna ordning:

1. INFORMATION
2. BOARD
3. MONTHLY REVIEW
4. DELIVERY DETAIL
5. QUALITY DETAIL
6. EHS DETAIL
7. CLOSED LFI · DETAILS
8. DELIVERY · SOURCE DETAILS
9. REPORTING
10. Monthly Review Cell DAX
11. Slutkontroll

Spara gärna efter varje sida.

────────

12. Slutkontroll

Kontrollera endast detta när du är klar:

☐ Alla rubriker syns helt.
☐ Samma ord används för samma sak på alla sidor.
☐ Inga tekniska ord står kvar i normalvyn utan anledning.
☐ BOARD går att förstå på några sekunder.
☐ Detail-sidor följer: resultat → reporting → details → actions.
☐ MONTHLY REVIEW visar resultatet först och datatäckning endast där det behövs.
☐ INFORMATION är en snabbguide, inte teknisk dokumentation.
☐ REPORTING säger tydligt vad användaren ska göra idag.
☐ Alla navigation-knappar fungerar.
☐ Tooltips fungerar.
☐ Inga KPI-mått eller datakällor har ändrats av misstag.
☐ Ingen measure cleanup har gjorts.

────────

Slutlig språkprincip

När du tvekar mellan två formuleringar:

Välj den som en kollega förstår direkt utan att känna till Power BI.

Exempel:

• source evidence → current source data
• selected period → selected month
• investigate selected record view → details
• saved snapshot → ta bort om användaren inte behöver veta det
• denominator → förklara vad värdet används till
• all reporting dates → ta bort om det inte hjälper användaren

Rapporten ska förklara verksamheten – inte datamodellen.

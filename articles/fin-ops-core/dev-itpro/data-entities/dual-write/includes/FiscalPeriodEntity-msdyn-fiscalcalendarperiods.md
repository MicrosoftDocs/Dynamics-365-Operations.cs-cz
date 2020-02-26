## <a name="fiscal-calendar-period-to-msdyn_fiscalcalendarperiods"></a>Období fiskálního kalendáře do msdyn_fiscalcalendarperiods

Tato šablona synchronizuje data mezi aplikacemi Finance and Operations a Common Data Service.

Pole aplikace Finance and Operations | Typ mapování | Jiné pole Dynamics 365 | Výchozí hodnota
---|---|---|---
COMMENTS | = | msdyn_comments | 
ENDDATE | = | msdyn_enddate | 
MONTH | >< | msdyn_month | 
CALENDAR | = | msdyn_fiscalcalendar.msdyn_calendar | 
QUARTER | >< | msdyn_quarter | 
SHORTNAME | = | msdyn_shortname | 
STARTDATE | = | msdyn_startdate | 
TYP | >< | msdyn_fiscalperiodtype | 
PERIODNAME | = | msdyn_periodname | 
FISCALYEAR | = | msdyn_fiscalcalendaryear.msdyn_name | 
CALENDAR | = | msdyn_fiscalcalendaryear.msdyn_fiscalcalendarname | 

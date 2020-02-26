## <a name="fiscal-calendar-year-integration-entity-to-msdyn_fiscalcalendaryears"></a>Entita integrace roku fiskálního kalendáře do msdyn_fiscalcalendaryears

Tato šablona synchronizuje data mezi aplikacemi Finance and Operations a Common Data Service.

Pole aplikace Finance and Operations | Typ mapování | Jiné pole Dynamics 365 | Výchozí hodnota
---|---|---|---
FISCALCALENDAR_CALENDARID | = | msdyn_fiscalcalendarname | 
NAME | = | msdyn_name | 
STARTDATE | = | msdyn_startdate | 
ENDDATE | = | msdyn_enddate | 
FISCALCALENDAR_CALENDARID | = | msdyn_calendar.msdyn_calendar | 

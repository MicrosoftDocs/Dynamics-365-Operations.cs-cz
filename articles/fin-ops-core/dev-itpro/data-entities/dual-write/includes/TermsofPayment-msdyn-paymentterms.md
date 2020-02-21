## <a name="terms-of-payment-to-msdyn_paymentterms"></a>Platební podmínky do msdyn_paymentterms

Tato šablona synchronizuje data mezi aplikacemi Finance and Operations a Common Data Service.

Pole aplikace Finance and Operations | Typ mapování | Jiné pole Dynamics 365 | Výchozí hodnota
---|---|---|---
DESCRIPTION | = | msdyn_description | 
NAME | = | msdyn_name | 
NUMBEROFMONTHS | = | msdyn_numberofmonth | 
CUTOFFDAYOFMONTH | = | msdyn_cutoffdayofmonth | 
ISCASHPAYMENT | >< | msdyn_iscashpayment | 
NUMBEROFDAYS | = | msdyn_days | 
ISCERTIFIEDCOMPANYCHECK | >< | msdyn_iscertifiedcompanycheck | 
ISDEFAULTPAYMENTTERM | >< | msdyn_isdefaultpaymentterm | 
CREDITCARDPAYMENTTYPE | >< | msdyn_creditcardpaymenttype | 
CREDITCARDCREDITCHECKTYPE | >< | msdyn_creditcardcreditchecktype | 
PAYMENTDAYNAME | = | msdyn_paymentdayname.msdyn_name | 
PAYMENTMETHODTYPE | >< | msdyn_paymentmethodtype | 
PAYMENTSCHEDULENAME | = | msdyn_paymentschedulename.msdyn_name | 

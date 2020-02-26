## <a name="customer-groups-to-msdyn_customergroups"></a>Skupiny zákazníků do msdyn_customergroups

Tato šablona synchronizuje data mezi aplikacemi Finance and Operations a Common Data Service.

Pole aplikace Finance and Operations | Typ mapování | Jiné pole Dynamics 365 | Výchozí hodnota
---|---|---|---
CUSTOMERGROUPID | = | msdyn_groupid | 
DESCRIPTION | = | msdyn_description | 
ISSALESTAXINCLUDEDINPRICE | >< | msdyn_issalestaxincludedinprice | 
PAYMENTTERMID | = | msdyn_paymenttermid.msdyn_name | 
CLEARINGPERIODPAYMENTTERMNAME | = | msdyn_clearingperiodpaymenttermname.msdyn_name | 

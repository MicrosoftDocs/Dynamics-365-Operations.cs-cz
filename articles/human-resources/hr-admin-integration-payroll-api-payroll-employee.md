---
title: Zaměstnanec na výplatní listině
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu zaměstnance na výplatní listině v Dynamics 365 Human Resources.
author: jcart
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e853a8a5730d397f253c8ce3a330794594dfd907
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8068477"
---
# <a name="payroll-employee"></a>Zaměstnanec na výplatní listině


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma popisuje entitu Zaměstnanec se mzdou pro Dynamics 365 Human Resources.

Fyzický název: mshr_payrollemployeeentity.

### <a name="description"></a>popis

Tato entita poskytuje informace o zaměstnanci. Musíte nastavit [parametry integrace mezd](hr-admin-integration-payroll-api-parameters.md) před použitím této entity.

>[!IMPORTANT] 
>Pole **FirstName**, **MiddleName**, **LastName**, **NameValidFrom** a **NameValidTo** v této entitě již nejsou dostupná. Tím je zajištěno, že existuje pouze jeden datový zdroj data platnosti, který podporuje tuto entitu.
>Tato pole budou k dispozici na **DirPersonNameHistoricalEntity**, která byla vydána v aktualizaci platformy 43. Existuje vztah OData z **PayrollEmployeeEntity** do **DirPersonNameHistoricalEntity**. 

## <a name="properties"></a>Vlastnosti

| Vlastnost</br>**Fyzický název**</br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID právnické osoby**</br>mshr_legalentityid</br>*Řetězec* | Jen pro čtení | Určuje právnickou osobu (společnost). |
| **Číslo pracovníka**</br>mshr_personnelnumber</br>*Řetězec* | Jen pro čtení | Jedinečné osobní číslo zaměstnance. |
| **Počáteční datum zaměstnání**</br>mshr_employmentstartdate</br>*Posun data a času* | Jen pro čtení | Počáteční datum zaměstnaneckého poměru zaměstnance. |
| **Koncové datum zaměstnání**</br>mshr_employmentenddate</br>*Posun data a času* | Jen pro čtení |Koncové datum zaměstnaneckého poměru zaměstnance.  |
| **Datum narození**</br>mshr_birthdate</br>*Posun data a času* | Jen pro čtení | Datum narození zaměstnance |
| **Rod**</br>mshr_gender</br>[Sada možností mshr_hcmpersongender](hr-admin-integration-payroll-api-gender.md) | Jen pro čtení | Pohlaví zaměstnance. |
| **Typ zaměstnání**</br>mshr_employmenttype</br>[sada možností mshr_hcmemploymenttype](hr-admin-integration-payroll-api-hcmemploymenttype.md) | Jen pro čtení | Typ zaměstnání. |
| **ID typu identifikace**</br>mshr_identificationtypeid</br>*Řetězec* |Jen pro čtení | Typ identifikace definovaný pro zaměstnance. |
| **Identifikační číslo do**</br>mshr_identificationnumber</br>*Řetězec* | Jen pro čtení |Identifikační číslo definované pro zaměstnance. |
| **Připraveno k platbě**</br>mshr_readytopay</br>[Sada možností mshr_noyes](hr-admin-integration-payroll-api-no-yes.md) | Jen pro čtení | Udává, zda je zaměstnanec označen jako připravený k výplatě. |
| **ID entity zaměstnance na výplatní listině**</br>mshr_payrollemployeeentityid</br>*GUID* | Generováno systémem | Systémem generovaná hodnota globálně jedinečného identifikátoru (GUID) pro jedinečnou identifikaci zaměstnance. |

## <a name="relations"></a>Vztahy

|Hodnota vlastnosti | Související entita | Navigační vlastnost | Typ kolekce |
| --- | --- | --- | --- |
| _mshr_fk_employment_id_value | mshr_hcmemploymentdetailentity | mshr_FK_Employment_id | mshr_FK_HcmEmploymentDetailEntity_PayrollEmployee |
| _mshr_fk_fixedcompplan_id_value | [mshr_payrollfixedcompensationplanentity](hr-admin-integration-payroll-api-payroll-fixed-compensation-plan.md) | mshr_FK_FixedCompPlan_id | mshr_FK_PayrollFixedCompensationPlanEntity_Employee |
| _mshr_fk_name_id_value | mshr_dirpersonnamehistoricalentity | mshr_FK_Name_id | - |
| _mshr_fk_worker_id_value | mshr_hcmworkerbaseentity | mshr_FK_Worker_id | mshr_FK_HcmWorkerBaseEntity_PayrollEmployee |
| _mshr_fk_workerbankaccount_id_value | mshr_hcmworkerbankaccountentity | mshr_FK_WorkerBankAccount_id | mshr_FK_HcmWorkerBankAccountEntity_PayrollEmployee |
| _mshr_fk_variablecompaward_id_value | [mshr_payrollvariablecompensationawardentity](hr-admin-integration-payroll-api-payroll-variable-compensation-plan.md) | mshr_FK_VariableCompAward_id | mshr_FK_PayrollVariableCompensationAwardEntity_Employee |
| _mshr_fk_address_id_value | [mshr_payrollworkeraddressentity](hr-admin-integration-payroll-api-payroll-worker-address.md) | mshr_FK_Address_id | mshr_FK_PayrollWorkerAddressEntity_Worker |

## <a name="example-query-for-payroll-employee"></a>Příklad dotazu pro zaměstnance na výplatní pásce

**Žádost**

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq '000041'
```

**Odezva**

```json
{
    "mshr_legalentityid": "USMF",
    "mshr_personnelnumber": "000041",
    "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
    "mshr_employmentenddate": "2154-12-31T23:59:59Z",
    "mshr_birthdate": "1987-09-12T00:00:00Z",
    "mshr_gender": 200000002,
    "mshr_employmenttype": 200000000,
    "mshr_identificationtypeid": "SSN",
    "mshr_identificationnumber": "888-99-9342",
    "mshr_readytopay": 200000000,
    "mshr_dataareaid": "USMF",
    "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
    "_mshr_fk_employment_id_value": "00000d4e-0000-0000-0600-014105000000",
    "_mshr_fk_fixedcompplan_id_value": "00000598-0000-0000-4cd0-fda002000000",
    "_mshr_fk_name_id_value": "00000832-0000-0000-d700-014105000000",
    "_mshr_fk_worker_id_value": "000000af-0000-0000-d5ff-004105000000",
    "_mshr_fk_workerbankaccount_id_value": "000006f2-0000-0000-b7ff-004105000000",
    "mshr_payrollemployeeentityid": "00000666-0000-0000-d5ff-004105000000",
    "_mshr_fk_address_id_value": null,
    "_mshr_fk_variablecompaward_id_value": null,
    "_mshr_dataareaid_id_value": null
}
```

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

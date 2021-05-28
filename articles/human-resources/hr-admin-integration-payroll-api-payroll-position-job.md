---
title: Práce pozice mzdy
description: Toto téma poskytuje informace a ukázkový dotaz pro entitu pracovní pozice na výplatní listině v Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9444a36f5ddf92bd41008c83ec77ab7ff5191fa3
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019339"
---
# <a name="payroll-position-job"></a>Práce pozice mzdy

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Toto téma poskytuje informace a ukázkový dotaz pro entitu vztahu pracovní pozice na výplatní listině v Dynamics 365 Human Resources.

## <a name="properties"></a>Vlastnosti

| Vlastnost<br>**Fyzický název**<br>**_Typ_** | Použít | popis |
| --- | --- | --- |
| **ID úlohy**<br>mshr_jobid<br>*Řetězec* | Jen pro čtení<br>Povinná |ID úlohy. |
| **Platné od**<br>mshr_validto<br>*Posun data a času* | Jen pro čtení <br>Povinná | Datum, od kterého je pozice a pracovní vztah platné. |
| **Platné do**<br>mshr_validto<br>*Posun data a času* | Jen pro čtení <br>Povinná | Datum, do kterého je pozice a pracovní vztah platné.  |
| **ID pozice**<br>mshr_positionid<br>*Řetězec* | Jen pro čtení<br>Povinná | Identifikace pozice. |
| **Primární pole**<br>mshr_primaryfield<br>*Řetězec* | Povinná<br>Generováno systémem |  |
| **Hodnota ID pracovní pozice**<br>_mshr_fk_positionjob_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_PayrollPositionJobEntity mshr_payrollpositionjobentity |ID práce přidružené k pozici.|
| **Hodnota ID pevného plánu kompenzace**<br>_mshr_fk_fixedcompplan_id_value<br>*GUID* | Jen pro čtení<br>Povinná<br>Cizí klíč: mshr_FixedCompPlan_id z mshr_payrollfixedcompensationplanentity  | ID plánu pevné kompenzace přidruženého k pozici. |
| **ID entity pracovní pozice na výplatní listině**<br>mshr_payrollpositionjobentityid<br>*Guid* | Povinná<br>Generováno systémem. | Systémem generovaná hodnota GUID pro jedinečnou identifikaci pracovní pozice.  |


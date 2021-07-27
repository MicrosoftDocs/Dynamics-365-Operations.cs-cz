---
title: Přehled MyLeaveRequests
description: Entita MyLeaveRequests v Microsoft Dynamics 365 Human Resources poskytuje seznam požadavků na pracovní volno v systému (omezen) na požadavky, které jsou přístupné aktuálnímu uživateli při zadávání dotazu na entitu.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 724c4c91e38bb8ac9fe1fd0794dc5a79b2435472
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/03/2021
ms.locfileid: "6339732"
---
# <a name="myleaverequests-overview"></a>Přehled MyLeaveRequests

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Entita MyLeaveRequests v Microsoft Dynamics 365 Human Resources poskytuje seznam požadavků na pracovní volno v systému (omezen) na požadavky, které jsou přístupné aktuálnímu uživateli při zadávání dotazu na entitu.

## <a name="key"></a>Klíč

  | Název vlastnosti | Datový typ |
  |---------------|-----------|
  | dataAreaId    | Řetězec    |
  | RequestId     | Řetězec    |
  | LeaveType     | Řetězec    |
  | LeaveDate     | Datum      |
  
## <a name="properties"></a>Vlastnosti

  | Název vlastnosti     | Datový typ | Povinné |
  |-------------------|-----------|----------|
  | dataAreaId        | Řetězec    | X        |
  | RequestId         | Řetězec    | X        |
  | LeaveType         | Řetězec    | X        |
  | LeaveDate         | Datum      | X        |
  | ReasonCodeId      | Řetězec    |          |
  | PersonnelNumber   | Řetězec    | X        |
  | RequestDate       | Datum      | X        |
  | Komentář           | Řetězec    |          |
  | Stav            | Výčet      | X        |
  | Množství            | Reálný      |          |
  | HalfDayDefinition | Výčet      |          |

## <a name="actions"></a>Akce

 | Název akce                               | Popis                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [odeslat](hr-developer-api-myleaverequests-submit.md)   | Odešlete požadavek ke zpracování pomocí workflowu. |

## <a name="see-also"></a>Viz také

- [Odeslání žádosti o volno do workflow](hr-developer-api-myleaverequests-submit.md)
- [Ověřování](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
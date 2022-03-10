---
title: Přehled MyLeaveRequests
description: Entita MyLeaveRequests v Microsoft Dynamics 365 Human Resources poskytuje seznam požadavků na pracovní volno v systému (omezen) na požadavky, které jsou přístupné aktuálnímu uživateli při zadávání dotazu na entitu.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 41ef8c6fc0e896e7f2cefd94801abab610083b81
ms.sourcegitcommit: 3a7f1fe72ac08e62dda1045e0fb97f7174b69a25
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2022
ms.locfileid: "8070847"
---
# <a name="myleaverequests-overview"></a>Přehled MyLeaveRequests


[!INCLUDE [PEAP](../includes/peap-1.md)]

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

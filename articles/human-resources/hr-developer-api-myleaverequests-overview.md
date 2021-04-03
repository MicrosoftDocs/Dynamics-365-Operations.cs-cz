---
title: Přehled MyLeaveRequests
description: Entita MyLeaveRequests v Microsoft Dynamics 365 Human Resources poskytuje seznam požadavků na pracovní volno v systému (omezen) na požadavky, které jsou přístupné aktuálnímu uživateli při zadávání dotazu na entitu.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465503"
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
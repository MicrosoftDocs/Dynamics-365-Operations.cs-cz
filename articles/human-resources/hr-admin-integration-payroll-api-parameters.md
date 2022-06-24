---
title: Parametry integrace mezd
description: Tento článek popisuje parametry Dynamics 365 Human Resources pro integraci mezd.
author: marcelbf
ms.date: 06/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-06-17
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7d784909fc8c5fa05557566b62b19802cd2acece
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896090"
---
# <a name="payroll-integration-parameters"></a>Parametry integrace mezd


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Před použitím integrace mezd Dynamics 365 Human Resources, musíte nastavit parametry popsané v tomto článku.

## <a name="enable-payroll-address"></a>Aktivace adresy mezd

Abyste mohli použít mzdovou adresu, musíte ji povolit ve [formuláři sdílených parametrů](hr-setup-shared-parameters.md) na kartě Integrace mezd.

## <a name="define-the-identification-type"></a>Určete typ identifikace

Chcete-li vystavit ID typu identifikace typ v [entitě zaměstnanců mzdy](hr-admin-integration-payroll-api-payroll-employee.md), musíte [konfigurovat parametry Human Resources](hr-setup-shared-parameters.md) pro každou společnost.

1. V pracovním prostoru **Správa kompenzace** vyberte v části odkazy **Parametry Human Resources**. 
2. Na kartě **Integrace mezd** zadejte hodnotu následujících polí.

| Pole | popis |
| --- | --- |
| Použít typy identifikace při zpracování mezd | Když je vybrána tato možnost, vybrané ID typu bude vystaveno v entitě zaměstnance mezd. |
| Typ identifikace | Typ identifikace, který má být vystaven v poli **mshr_payrollemployeeentityid** [entity zaměstnance mezd](hr-admin-integration-payroll-api-payroll-employee.md). |

## <a name="see-also"></a>Viz také

[Úvod do rozhraní API integrace mezd](hr-admin-integration-payroll-api-introduction.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

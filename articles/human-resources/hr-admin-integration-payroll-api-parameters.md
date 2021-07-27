---
title: Parametry integrace mezd
description: Toto téma popisuje parametry Dynamics 365 Human Resources pro integraci mezd.
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
ms.openlocfilehash: 5f76ce395d7f5a82ab622dd323aee52a39b09847
ms.sourcegitcommit: 89bb2a7f402deed32998eddc1e56e75250e3d15e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/29/2021
ms.locfileid: "6314343"
---
# <a name="payroll-integration-parameters"></a>Parametry integrace mezd

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Před použitím integrace mezd Dynamics 365 Human Resources, musíte nastavit parametry popsané v tomto tématu.

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

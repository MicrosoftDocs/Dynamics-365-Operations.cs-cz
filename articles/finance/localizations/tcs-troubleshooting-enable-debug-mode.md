---
title: Povolení režimu ladění ve službě výpočtu daně
description: Tento článek vysvětluje, jak povolit režim ladění ve službě Výpočet daně za účelem prošetření problémů.
author: hangwan
ms.date: 03/25/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: ''
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 03/23/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 2bb381939ebe32cb51caf730cdd441557d83a4c0
ms.sourcegitcommit: 088a7b5eb9a3b68710dfe012abf4c24776978750
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/01/2022
ms.locfileid: "9620891"
---
# <a name="enable-debug-mode-in-the-tax-calculation-service"></a>Povolení režimu ladění ve službě výpočtu daně

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje, jak povolit režim ladění ve službě Výpočet daně za účelem prošetření problémů.

1. Přidejte **&debug=vs%2CconfirmExit&** k adrese URL Application Object Server (AOS) a poté stránku obnovte.
2. Když vyberete **Daň z prodeje** pro výpočet daně z prodeje, otevře se textový soubor s názvem **TaxServiceTroubleshootingLog.txt**. Soubor **TaxServiceTroubleshootingLog.txt** obsahuje **TaxableDocument** a parametr výpočtu. Tyto výsledky jsou vráceny z daňové služby a informací o výjimce pro odstraňování problémů.

## <a name="sample"></a>Ukázka

```json
===============================Tax service calculation input JSON:=====================================
{
    "TaxableDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Transaction Line ID": "5816,68719677391",
            ...
            }
        ],
        "Transaction Header ID": "2022,68719506302",
        ...
        }
    ]
    },
    "Parameter": {
    "ContinueOnErrors": true,
    ...
    },
    "Adjustment": {
    "Lines": {}
    }
}
===========================Tax service calculation result JSON:=================================
{
    "taxDocument": {
    "Header": [
        {
        "Lines": [
            {
            "Tax Codes": {
                ...
            }
        ],
        "Measures": {
            "List Code": "EUTrade"
        },
        "Tax Registration ID": null,
        "Transaction Header ID": "2022,68719506302",
        "Errors": null
        }
    ]
    },
    "solutionId": "b51e0025-cbbe-4d37-bf0b-90d7be4f214d|1",
    "isPartialSuccess": false
}
=============================CorrelationId:==============================
"21f3a8a1-ee9a-477b-b44e-b8ec79e74d16"
```

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

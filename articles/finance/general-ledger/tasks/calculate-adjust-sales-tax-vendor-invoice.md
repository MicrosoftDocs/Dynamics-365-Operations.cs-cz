---
title: Výpočet a úprava DPH na faktuře dodavatele
description: V tomto článku je vysvětleno, jak upravit DPH u faktury dodavatele v aplikaci Dynamics 365 Finance.
author: twheeloc
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a1093631688351d065d6b55bc65055b6f92d256
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868351"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Výpočet a úprava DPH na faktuře dodavatele

[!include [banner](../../includes/banner.md)]

V tomto článku je vysvětleno, jak upravit DPH u faktury dodavatele. Pokud původní zdrojový dokument zobrazí různé částky daně tak, jak se vypočítají, můžete je upravit před zaúčtováním. Tento úkol používá ukázkovou společnost DEMF.

1. Přejděte na **Závazky > Faktury > Deník faktur**.
2. Zvolte **Nové**.
3. V poli **Název** nového řádku vyberte některou z možností v rozevírací nabídce.
4. V podokně akcí zvolte **Řádky**.
5. Zadejte požadované hodnoty do pole **Účet**.
6. Zadejte hodnotu do pole **Faktura**.
7. V poli **Dobropis** zadejte číslo.
8. Zadejte požadované hodnoty do pole **Protiúčet**.
9. Vyberte **DPH**.
10. V poli **Celková částka skutečné DPH** zadejte číslo.
11. Na kartě **Úprava** lze upravit částky DPH podle kódu DPH.
12. Vyberte **Resetovat skutečné částky z vypočítaných částek**.
13. Vyberte **OK**.
14. Zvolte **Uložit**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

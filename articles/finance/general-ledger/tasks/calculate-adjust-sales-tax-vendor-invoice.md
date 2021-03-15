---
title: Výpočet a úprava DPH na faktuře dodavatele
description: V tomto tématu je vysvětleno, jak upravit DPH u faktury dodavatele v aplikaci Dynamics 365 Finance.
author: twheeloc
manager: AnnBe
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2536e87953267eae13cf3b42c2bd5476fc647c22
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994708"
---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a>Výpočet a úprava DPH na faktuře dodavatele

[!include [banner](../../includes/banner.md)]

V tomto tématu je vysvětleno, jak upravit DPH u faktury dodavatele. Pokud původní zdrojový dokument zobrazí různé částky daně tak, jak se vypočítají, můžete je upravit před zaúčtováním. Tento úkol používá ukázkovou společnost DEMF.

1. V navigačním podokně přejděte na **Moduly > Závazky > Faktury > Deník faktury**.
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
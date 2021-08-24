---
title: Výpočet a úprava DPH na faktuře dodavatele
description: V tomto tématu je vysvětleno, jak upravit DPH u faktury dodavatele v aplikaci Dynamics 365 Finance.
author: twheeloc
ms.date: 07/31/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 648d94e895a4941f5f3148134130b3ffa693a9d57e0bb4e236f5d5fb33aca48f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6779805"
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
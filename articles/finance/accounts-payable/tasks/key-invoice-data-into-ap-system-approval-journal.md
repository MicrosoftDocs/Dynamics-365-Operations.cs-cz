---
title: Zadání dat faktury do závazků s použitím deníku schválení
description: Tento článek popisuje použití registru faktur k vytvoření faktur a použití deníku schválení pro aktualizaci účtů výdajů.
author: abruer
ms.date: 02/11/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransInvoiceRegister, HcmWorkerLookUp, LedgerJournalTransApprove, LedgerJournalTransApproveFetchVouchers, LedgerTransVoucher
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: afe1471949bbf892f4e28ed3bea830ee491a517f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909207"
---
# <a name="key-invoice-data-into-accounts-payable-using-an-approval-journal"></a>Zadání dat faktury do závazků s použitím deníku schválení

[!include [banner](../../includes/banner.md)]

Tento článek popisuje použití registru faktur k vytvoření faktur a použití deníku schválení pro aktualizaci účtů výdajů.

## <a name="create-and-post-and-invoice"></a>Vytvoření a zaúčtování faktury
1. V navigačním podokně přejděte na **Moduly > Závazky > Faktury > Registr faktur**.
2. Zvolte **Nové**.
3. Vyberte název registru faktury, který chcete použít.
4. Kliknutím na **Řádky** otevřete registr a zadejte řádky výdajů.
5. Vyberte dodavatele. Například zadejte nebo vyberte možnost `US-104`.
6. Zadejte hodnotu do pole **Faktura**.
7. Zadejte hodnotu do pole **Popis**.
8. V poli **Dobropis** zadejte číslo.
9. V poli **Schválil/a** vyberte z rozevírací nabídky schvalovatele.
10. Zvolte **Zaúčtovat**.

## <a name="approve-an-invoice"></a>Schválení faktury
1. V navigačním podokně přejděte na **Moduly > Závazky > Faktury > Schvalovatel faktury**.
2. Zvolte **Nové**.
3. Vyberte název deníku schválení faktur, který chcete použít.
4. Výběrem položky **Řádky** zobrazte stránku, kde bude možné vybrat faktury, které chcete schválit.
5. Výběrem možnosti **Hledat doklady** zobrazte všechny faktury, které jsou již připraveny ke schválení.
6. Označte fakturu, kterou jste vytvořili, a poté kliknětena tlačítko **Vybrat**. Doklady vybrané výše, se po výběru přesunou do tohoto seznamu.  
7. Vyberte **OK**.
8. Vyberte pole s **číslem účtu** přidejte výdajový účet k faktuře.
9. Zadejte číslo účtu a opusťte toto pole. Zadejte například `600120`.
10. Zvolte **Zaúčtovat**.
11. Výběrem možnosti **Doklad** zobrazte položky, které byly zaúčtovány. Účet Faktury čekající na schválení bude stornován a nahrazen údaji skutečného účtu výdajů.  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

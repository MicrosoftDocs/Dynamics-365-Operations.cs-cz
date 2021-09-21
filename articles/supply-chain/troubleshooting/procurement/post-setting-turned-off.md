---
title: Nastavení možnosti Zaúčtovat na účet poplatků v hlavní knize není zapnuto
description: K tomuto problému dochází, když je nákupní objednávka fakturována, pokud je možnost "Zaúčtovat na účet poplatků v hlavní knize" povolena na kartě Faktura stránky Parametry závazků.
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 592444958dad4624fdc9098dc58df0a2e49e63de
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475816"
---
# <a name="the-post-to-charge-account-in-ledger-setting-isnt-turned-on"></a>Nastavení možnosti Zaúčtovat na účet poplatků v hlavní knize není zapnuto

## <a name="symptoms"></a>Příznaky

K tomuto problému dochází, když je nákupní objednávka fakturována, pokud je možnost **Zaúčtovat na účet poplatků v hlavní knize** nastavena na *Ano* na kartě **Faktura** stránky **Parametry závazků**.

## <a name="reproduce-the-issue"></a>Reprodukování problému

Následující postup ukazuje jeden způsob, jak reprodukovat problém.

1. Přejděte do nabídky **Závazky \> Nastavení \> Parametry závazků**.
1. Na kartě **Faktura** nastavte možnost **Zaúčtovat na účet poplatků v hlavní knize** na *Ano*.
1. Přejděte na **Řízení zásob \> Nastavit \> Zaúčtování \> Zaúčtování**.
1. Na kartě **Nákupní objednávka** se ujistěte, že jste odstranili všechny řádky v nákupních výdajích za produkt.
1. Přejděte na **Závazky \> Nákupní objednávky \> Všechny nákupní objednávky**.
1. Vytvoření nákupní objednávky. V poli **Účet dodavatele** vyberte *1001 kancelářské potřeby Acme*.
1. Přidejte řádek nákupní objednávky, který má následující nastavení:

    - **Číslo položky:** *Laserový projektor D0011*
    - **Lokalita:** *1*
    - **Sklad:** *11*
    - **Množství:** *4*

1. V podokně akcí na kartě **Nákup** ve skupině **Akce** zvolte **Potvrdit**.
1. V podokně Akce na kartě **Přijmout** ve skupině **Generovat** zvolte **Příjemka produktu**.
1. V dialogovém okně **Zaúčtování příjemky produktu** v poli **Příjemka produktu** zadejte libovolné číslo a poté vyberte **OK**.
1. V podokně akcí na kartě **Faktura** ve skupině **Generovat** zvolte **Faktura**.
1. V poli **Číslo** zadejte libovolné číslo jako číslo faktury.
1. Aktualizujte stav párování a zaúčtování.
1. Všimněte si, že nyní při generování faktury z nákupní objednávky se zobrazí následující chyba: „Číslo účtu pro typ transakce nákupního výdaje za produkt neexistuje.“

## <a name="resolution"></a>Řešení

To závisí na nastavení parametrů pro faktury a skupiny faktur. Další informace najdete v následujícím příspěvku na blogu: [Účtování nákladů nákupu a odchylky zásob](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/12/15/accounting-for-purchase-charge-and-stock-variation/).

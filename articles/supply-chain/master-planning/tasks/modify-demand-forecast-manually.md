---
title: 'Průvodce: Ruční úprava prognózy poptávky'
description: Tento článek popisuje postup úpravy prognózy pro položku
author: t-benebo
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6275749f85c9b9d5a8b89da6340beeafbe22c2d4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8859249"
---
# <a name="guide-modify-a-demand-forecast-manually"></a>Průvodce: Ruční úprava prognózy poptávky

[!include [banner](../../includes/banner.md)]

Tento postup popisuje postup úpravy prognózy pro položku. Tento postup je určen pro plánujícího produkce.

## <a name="modify-the-forecast-for-a-selected-item"></a>Upravení prognózy pro vybranou položku

Upravení prognózy pro vybranou položku:

1. Přejděte na **Moduly \> Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vyhledejte na seznamu požadovaný záznam a vyberte ho. Vyberte položku, u které chcete změnit typ prognózu.
1. V podokně akcí otevřete kartu **Plán** a vyberte **Prognóza poptávky**.
1. V seznamu vyberte řádek. Pokud neexistují žádné řádky prognózy, vytvořte nový řádek výběrem možnosti **Nový** v podokně Akce.  
1. Do pole **Prodejní množství** zadejte kladné číslo. Toto číslo představuje předpovídané množství položky. Pokud zadáte záporné číslo, zobrazí se chyba.
1. Podle potřeby vyplňte ostatní pole.
1. V podokně akcí vyberte **Uložit**.

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a>Úprava prognózy pro jednu nebo více položek v aplikaci Microsoft Excel

Postup úpravy prognózy pro jednu nebo více položek v aplikaci Microsoft Excel:

1. Proveďte některou z následujících akcí:
    - Otevřete stránku **Prognóza poptávky** pro libovolnou položku (nezáleží na tom kterou), jak je popsáno v předchozí části.
    - Přejděte na **Hlavní plánování \> Prognózování \> Ruční zadání prognózy \> Řádky prognózy poptávky**.
1. V podokně akcí vyberte **Otevřít v Microsoft Office \> Záznamy prognózy poptávky**.
1. Vyberte umístění pro stažení, uložte a poté otevřete stažený soubor v aplikaci Excel.
1. Pokud se zobrazí varování, zvolte možnost **Povolit úpravy**.
1. V aplikaci Excel se přihlaste do Supply Chain Management pomocí podokna úloh Microsoft Dynamics. Musíte se přihlásit s aktivní možností **Zachovat přihlášení** a aplikaci pro datové připojení musíte důvěřovat.
1. Tabulka Excel nyní zobrazuje všechny aktuální řádky prognózy poptávky pro vaši společnost.  Podle potřeby řádky prognózy poptávky můžete přidávat, odstraňovat a upravovat.
1. Vyberte **Publikovat** v podokně úloh Microsoft Dynamics a nahrajte své změny zpět do Supply Chain Management.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

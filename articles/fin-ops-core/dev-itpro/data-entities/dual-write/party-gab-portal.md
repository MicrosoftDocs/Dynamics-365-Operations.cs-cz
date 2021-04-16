---
title: Používání Power Portal s datovým modelem strany
description: Toto téma popisuje změny webových rolí portálu Power Portal kvůli datovému modelu strany v duálním zápisu.
author: RamaKrishnamoorthy
ms.date: 03/22/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2021-03-22
ms.openlocfilehash: a2ea914344341ee26138e853727c551bdd5d733e
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833083"
---
# <a name="using-power-portal-with-the-party-data-model"></a>Používání Power Portal s datovým modelem strany

[!INCLUDE[banner](../../includes/banner.md)]

[!INCLUDE[rename-banner](~/includes/cc-data-platform-banner.md)]

Verze řešení orchestrace aplikace s duálním zápisem 2.0.999.0 a novější zahrnuje změny datového modelu strany a globálního adresáře u tabulek Účet a Kontakt. Změny umožňují vztahy N:N, které podporují pokročilé obchodní scénáře. Tyto změny nejsou podporovány webovými rolemi portálu, včetně zákaznického portálu, které jsou dodávány jako integrované nebo které ve vašem prostředí existovaly před instalací duálního zápisu. Aby webové role fungovaly podle očekávání, musíte pomocí nového datového modelu vytvořit nové webové role. 

Stručně řečeno, změnil se způsob interakce tabulek, ale oprávnění k tabulkám na zákaznickém portálu se nezměnila. Toto téma vysvětluje, jak vytvořit nové webové role, které fungují s novým rozšířeným datovým modelem.

Tento diagram ukazuje relaci tabulky **bez** datového modelu strany a globálního adresáře:

   ![bez modelu strany](media/without-party-model.PNG)

Tento diagram ukazuje relaci tabulky **s** datovým modelem strany a globálního adresáře:

   ![s modelem strany](media/with-party-model.png)

## <a name="create-a-new-table-permission"></a>Vytvořte nové oprávnění k tabulce

Chcete-li vytvořit tato nová oprávnění k tabulce, postupujte takto:

1. Přihlaste se do [Power Apps](https://make.powerapps.com) a přejděte do svých aplikací.
2. Vyberte aplikaci pro správu portálu.
3. Na postranním panelu vyberte možnost **Zabezpečení > Oprávnění tabulky**.

    Musíte vytvořit tři nová oprávnění:

    + Spojení kontakt – strana
    + Spojení strana – účet
    + Spojení účet – objednávka

4. Vytvořte a uložte nové oprávnění pro spojení kontakt – strana a nastavte tyto parametry:

    + **Název**: Spojení strana – účet (nebo podle vašeho výběru)
    + **Název tabulky**: msdyn_contactforparty
    + **Web**: Zákaznický portál
    + **Rozsah**: Kontakt
    + **Oprávnění**: Vybrat vše
    + **Webové role**: Ověření uživatelé, Zástupce zákazníka (nebo podle vašeho výběru)

5. Vytvořte a uložte nové oprávnění pro spojení strana – účet a nastavte tyto parametry:

    + **Název**: Spojení strana – účet (nebo podle vašeho výběru)
    + **Název tabulky**: account
    + **Web**: Zákaznický portál
    + **Rozsah**: Nadřazený objekt
    + **Oprávnění**: Vybrat vše
    + **Oprávnění nadřazené tabulky**: Spojení kontakt – strana

6. Vytvořte a uložte nové oprávnění pro spojení účet – objednávka a nastavte tyto parametry:

    + **Název**: Spojení účet – objednávka (nebo podle vašeho výběru)
    + **Název tabulky**: salesorder
    + **Web**: Zákaznický portál
    + **Rozsah**: Nadřazený objekt
    + **Oprávnění**: Vybrat vše
    + **Oprávnění nadřazené tabulky**: Spojení strana – účet

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

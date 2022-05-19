---
title: Opětovné přidělení uznání výnosů – scénář 1
description: Toto téma se zabývá scénářem opětovného přidělení uznání výnosů, když jsou zadány dvě prodejní objednávky, ale ty jsou pouze potvrzeny. K podobným výsledkům dojdete, když jsou potvrzeny více než dvě prodejní objednávky.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: cd094840e16a0ab19e234148e4ef40c454315d96
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8725785"
---
# <a name="revenue-recognition-reallocation--scenario-1"></a>Opětovné přidělení uznání výnosů – scénář 1

[!include [banner](../includes/banner.md)]

Toto téma se zabývá scénářem opětovného přidělení uznání výnosů, když jsou zadány dvě prodejní objednávky, ale ty jsou pouze potvrzeny. K podobným výsledkům dojdete, když jsou potvrzeny více než dvě prodejní objednávky.

V tomto scénáři je možnost **Zaúčtovat opravy faktur do pohledávek při opětovném přidělení** na kartě **Uznání výnosů** na stránce **Parametry hlavní knihy** (**Uznání výnosů \> Nastavení \> Parametry hlavní knihy**) nastavena na **Ne**.

[![Možnost Zaúčtovat opravy faktur do pohledávek je nastavena na Ne](./media/06_rev-rec-scenarios.png)](./media/06_rev-rec-scenarios.png)

Pro odběratele US\_SI\_0003 je vytvořena prodejní objednávka. Odběratel si kupuje přenosný počítač (číslo položky S0012) a plán podpory (číslo položky S0008, „Trvalé inženýrské služby“). Výnosy za přenosný počítač jsou okamžitě uznány (neexistuje žádný plán uznání výnosů). Výnosy za plán podpory budou odloženy a uznány za 12 měsíců, jak je definováno časovým obdobím ve smlouvě.

[![Řádky prodejní objednávky pro přenosný počítač a plán podpory](./media/07_rev-rec-scenarios.png)](./media/07_rev-rec-scenarios.png)

Prodejní objednávka je potvrzena. Protože jsou obě položky nastaveny pro přidělení výnosové ceny, při potvrzení prodejní objednávky se vypočítá výnosová cena. Výnosy, které budou uznány, můžete zobrazit na stránce **Přidělení výnosové ceny** (na stránce **Prodejní objednávka** v podokně akcí na kartě **Spravovat** ve skupině **Uznání výnosů** vyberte **Přidělení výnosové ceny**). Výnosy za přenosný počítač budou zaúčtovány na účet výnosů ve výši $1008,01. Výnosy za plán podpory budou zaúčtovány na účet odložených výnosů ve výši $190,99. Součet výnosových cen se musí rovnat součtu řádků, které byly vytvořeny pro zachytávání přidělení výnosových cen ($1199,00).

[![Stránka Přidělení výnosové ceny](./media/08_rev-rec-scenarios.png)](./media/08_rev-rec-scenarios.png)

Odběratel se v době prodeje rozhodl nekupovat instalační služby (číslo položky S0001), ale později si to rozmyslel. Proto je pro stejného odběratele zadána druhá prodejní objednávka.

[![Řádek prodejní objednávky instalačních služeb](./media/09_rev-rec-scenarios.png)](./media/09_rev-rec-scenarios.png)

Druhá prodejní objednávka je potvrzena. Protože tato prodejní objednávka obsahuje pouze jeden řádek, při jejím potvrzení není přidělena výnosová cena. Výnosová cena je přidělena, pouze pokud existují dvě nebo více jedinečných položek a pokud jsou tyto položky nastaveny pro přidělení výnosových cen.

Pokud je tato nová prodejní objednávka jedinou změnou ve smlouvě odběratele, lze nyní spustit proces opětovného přidělení. V jedné ze dvou prodejních objednávek volbou **Opětovné přidělení ceny k novým řádkům objednávky** otevřete stránku **Opětovné přidělení ceny k novým řádkům objednávky**. Alternativně přejděte na **Uznání výnosů \> Periodické úkoly \> Opětovné přidělení ceny k novým řádkům objednávky**. Vyberte obě prodejní objednávky a odpovídající řádky a poté vyberte **Aktualizovat opětovné přidělení**. Sloupec **Opětovně přidělená částka** zobrazuje pro každý řádek prodejní objednávky novou výnosovou cenu.

[![Nové výnosové ceny na stránce Opětovné přidělení ceny k novým řádkům objednávky](./media/10_rev-rec-scenarios.png)](./media/10_rev-rec-scenarios.png)

Pokud vyberete **Očekávaný doklad**, nic se nezobrazí, protože nebyly zaúčtovány žádné faktury.

Opětovné přidělení dokončíte tlačítkem **Zpracovat**. Zobrazí se výzva k zadání data zaúčtování, a to i v případě, že není nic zaúčtováno. Po dokončení opětovného přidělení se na stránce **Přidělení výnosové ceny** zobrazí u všech položek obou prodejních objednávek přidělené ceny. Jinými slovy, stránka **Přidělení výnosové ceny** bude pro každou prodejní objednávku obsahovat položku, která na dané prodejní objednávce neexistuje, protože je součástí stejné smlouvy, ale jiné prodejní objednávky.

> [!TIP]
> Chcete-li zadat kontext, proč se zobrazují tyto další položky, můžete do mřížky přidat další sloupce, například **ID opětovného přidělení** a **Prodejní objednávka**.
> 
> [![Další sloupce na stránce Opětovné přidělení výnosových cen](./media/11_rev-rec-scenarios.png)](./media/11_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

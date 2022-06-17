---
title: Opětovné přidělení uznání výnosů – scénář 2
description: Tento článek se zabývá scénářem opětovného přidělení, kdy jsou zadány dvě prodejní objednávky a po fakturaci první z nich odběratel přidá položku do smlouvy. Je-li do smlouvy přidána nová položka, lze ji přidat buď do nové, nebo do existující prodejní objednávky.
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
ms.openlocfilehash: dec8dba9848b77e5c0a1007102789c8f88185fbc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904837"
---
# <a name="revenue-recognition-reallocation--scenario-2"></a>Opětovné přidělení uznání výnosů – scénář 2

[!include [banner](../includes/banner.md)]

Tento článek se zabývá scénářem opětovného přidělení, kdy jsou zadány dvě prodejní objednávky a po fakturaci první z nich odběratel přidá položku do smlouvy. Je-li do smlouvy přidána nová položka, lze ji přidat buď do nové, nebo do existující prodejní objednávky.

V tomto scénáři je možnost **Zaúčtovat opravy faktur do pohledávek při opětovném přidělení** na kartě **Uznání výnosů** na stránce **Parametry hlavní knihy** (**Uznání výnosů \> Nastavení \> Parametry hlavní knihy**) nastavena na **Ne**.

[![Možnost Zaúčtovat opravy faktur do pohledávek je nastavena na Ne](./media/12_rev-rec-scenarios.png)](./media/12_rev-rec-scenarios.png)

Pro odběratele US\_SI\_0003 je vytvořena prodejní objednávka. Odběratel kupuje instalační služby (číslo položky S0001) a plán podpory (číslo položky S0008) pro přenosný počítač, ale dosud si nevybral počítač. Výnosy z instalačních služeb budou odloženy až na datum zakoupení přenosného počítače. Výnosy za plán podpory budou odloženy a uznány za 12 měsíců, jak je definováno časovým obdobím ve smlouvě.

[![Řádky prodejní objednávky pro instalační služby a plán podpory](./media/13_rev-rec-scenarios.png)](./media/13_rev-rec-scenarios.png)

Prodejní objednávka je potvrzena. Protože jsou obě položky nastaveny pro přidělení výnosové ceny, při potvrzení prodejní objednávky se vypočítá výnosová cena. Výnosy, které budou uznány, můžete zobrazit na stránce **Přidělení výnosové ceny** (na stránce **Prodejní objednávka** v podokně akcí na kartě **Spravovat** ve skupině **Uznání výnosů** vyberte **Přidělení výnosové ceny**). Výnosy za instalační služby budou zaúčtovány na účet odložených výnosů ve výši $250. Výnosy za plán podpory budou také zaúčtovány na účet odložených výnosů ve výši $150. Součet výnosových cen se musí rovnat součtu řádků, které byly nastaveny pro zachytávání přidělení výnosových cen (400 USD).

[![Stránka Přidělení výnosové ceny](./media/14_rev-rec-scenarios.png)](./media/14_rev-rec-scenarios.png)

Prodejní objednávka je plně fakturována. Následující obrázek znázorňuje účetní položku, která je zaúčtovaná pro fakturu.

[![Účetní položka pro plně fakturovanou prodejní objednávku](./media/15_rev-rec-scenarios.png)](./media/15_rev-rec-scenarios.png)

Je také vytvořen plán uznání výnosů, ale žádný z výnosů zatím není uznán.

[![Stránka plánu uznání výnosů](./media/16_rev-rec-scenarios.png)](./media/16_rev-rec-scenarios.png)

O několik dní později si odběratel vybere přenosný počítač. Pro odběratele je zadána druhá prodejní objednávka.

[![Řádek prodejní objednávky pro přenosný počítač](./media/17_rev-rec-scenarios.png)](./media/17_rev-rec-scenarios.png)

Druhá prodejní objednávka je potvrzena. Protože tato prodejní objednávka obsahuje pouze jeden řádek, při jejím potvrzení není přidělena výnosová cena. Výnosová cena je přidělena, pouze pokud existují dvě nebo více jedinečných položek a pokud jsou tyto položky nastaveny pro přidělení výnosových cen.

Pokud je tato nová prodejní objednávka jedinou změnou ve smlouvě odběratele, lze nyní spustit proces opětovného přidělení. V jedné ze dvou prodejních objednávek volbou **Opětovné přidělení ceny k novým řádkům objednávky** otevřete stránku **Opětovné přidělení ceny k novým řádkům objednávky**. Alternativně přejděte na **Uznání výnosů \> Periodické úkoly \> Opětovné přidělení ceny k novým řádkům objednávky**. Vyberte obě prodejní objednávky a odpovídající řádky a poté vyberte **Aktualizovat opětovné přidělení**. Sloupec **Opětovně přidělená částka** zobrazuje pro každý řádek prodejní objednávky novou výnosovou cenu.

[![Nové výnosové ceny na stránce Opětovné přidělení ceny k novým řádkům objednávky](./media/18_rev-rec-scenarios.png)](./media/18_rev-rec-scenarios.png)

Dále volbou **Očekávaný doklad** zobrazte účetní položky, které budou zaúčtovány pouze do hlavní knihy. Protože je možnost **Zaúčtovat opravy faktur do pohledávek při opětovném přidělení** na stránce **Parametry hlavní knihy** nastavena na **Ne**, při zpracování opětovného přidělení nedojde k žádným změnám pohledávky.

[![Účetní položky na stránce Očekávaný doklad](./media/19_rev-rec-scenarios.png)](./media/19_rev-rec-scenarios.png)

Poslední tři řádky na stránce **Očekávaný doklad** stornují původní účetní položku ze zaúčtované faktury. První čtyři řádky tvoří novou účetní položku, která je zaúčtována pro fakturu. Je důležité vědět, že odběrateli není nepředložena nová faktura. Po opětovném přidělení odběratel stále dluží $426, což je částka, která musí být zaúčtována do pohledávek v nové účetní položce. Započtená daň a odložené výnosy se rovnají $188,69 + $314,48 + $26 = $529,17. Výše odložených výnosů se z důvodu opětovného přidělení změnila. Rozdíl $103,17 je zaúčtován na clearingový účet výnosů částečné faktury. Tento zůstatek bude vymazán při zaúčtování faktury pro druhou prodejní objednávku, která byla součástí opětovného přidělení.

Opětovné přidělení dokončíte tlačítkem **Zpracovat**. Zobrazí se výzva k zadání data zaúčtování, a to i v případě, že není nic zaúčtováno. Po dokončení opětovného přidělení se na stránce **Přidělení výnosové ceny** zobrazí u všech položek obou prodejních objednávek přidělené ceny. Jinými slovy, stránka **Přidělení výnosové ceny** bude pro každou prodejní objednávku obsahovat položku, která na dané prodejní objednávce neexistuje, protože je součástí stejné smlouvy, ale jiné prodejní objednávky.

> [!TIP]
> Chcete-li zadat kontext, proč se zobrazují tyto další položky, můžete do mřížky přidat další sloupce, například **ID opětovného přidělení** a **Prodejní objednávka**.
> 
> [![Další sloupce na stránce Opětovné přidělení výnosových cen](./media/20_rev-rec-scenarios.png)](./media/20_rev-rec-scenarios.png)

V prodejní objednávce 00036 byl také aktualizován plán uznání výnosů na základě nové ceny vzniklé opětovným přidělením výnosů. Z této prodejní objednávky otevřete stránku **Plán uznání výnosů**. Dříve měla položka S0008 13 řádků (této položce byl přiřazen 12měsíční plán). Nyní má 39 řádků: 13 řádků původního plánu, 13 řádků plánu stornování a 13 řádků, které vycházejí z nové výnosové ceny.

[![Aktualizovaná stránka plánu uznání výnosů s 39 řádky pro položku S0008](./media/21_rev-rec-scenarios.png)](./media/21_rev-rec-scenarios.png)

Obdobně předtím měla položka S0001 dva řádky, ale nyní je jich šest.

[![Aktualizovaná stránka plánu uznání výnosů s šesti řádky položky S0001](./media/22_rev-rec-scenarios.png)](./media/22_rev-rec-scenarios.png)

Když v prodejní objednávce 000036 vyberete **Doklad**, deník faktur obsahuje původní účetní položku. Chcete-li zobrazit stornující a novou účetní položku prodejní objednávky, v podokně akcí vyberte **Úpravy výnosů** a poté vyberte **Doklad**.

[![Prodejní objednávka 000036](./media/23_rev-rec-scenarios.png)](./media/23_rev-rec-scenarios.png)

Dále otevřete stránku **Všichni odběratelé** (**Pohledávky \> Odběratelé \> Všichni odběratelé**), vyberte odběratele **US\_SI\_0003** a potom vyberte **Transakce**. Zobrazí se otevřená faktura z prodejní objednávky 000036. Pokud vyberete doklad, zobrazí se původní účetní položka namísto nové účetní položky z opětovného přidělení. Z pohledávek nelze zobrazit stornovací a novou účetní položku.

Nyní je fakturována druhá prodejní objednávka. Celková faktura předložená odběrateli je ve výši $1099 + daň $71,44 = $1170,44. Následující obrázek znázorňuje zaúčtovanou účetní položku.

[![Stránka transakcí dokladů se zaúčtovanou účetní položkou](./media/24_rev-rec-scenarios.png)](./media/24_rev-rec-scenarios.png)

Protože součet výnosů a prodeje je vyšší než 1170,44 USD, zaúčtovaný rozdíl je -130,17 USD. Tato částka vymaže zůstatek z clearingového účtu výnosů částečné faktury. Tento zůstatek je po opětovném přidělení zaúčtován v nové účetní položce.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

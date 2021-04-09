---
title: Opětovné přidělení uznání výnosů – scénář 4
description: Toto téma popisuje scénář opětovného přidělení, kdy je z existující, částečně fakturované prodejní objednávky odebrán řádek. Odebráním řádku z prodejní objednávky nebo jeho nastavením do stavu Zrušeno dojdete ke stejnému výsledku.
author: kweekley
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 2b53145ac1ef4b277afadb4262fd1e704a2e7662
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830657"
---
# <a name="revenue-recognition-reallocation--scenario-4"></a>Opětovné přidělení uznání výnosů – scénář 4

[!include [banner](../includes/banner.md)]

Toto téma popisuje scénář opětovného přidělení, kdy je z existující, částečně fakturované prodejní objednávky odebrán řádek. Odebráním řádku z prodejní objednávky nebo jeho nastavením do stavu Zrušeno dojdete ke stejnému výsledku.

V tomto scénáři je možnost **Zaúčtovat opravy faktur do pohledávek při opětovném přidělení** na kartě **Uznání výnosů** na stránce **Parametry hlavní knihy** (**Uznání výnosů \> Nastavení \> Parametry hlavní knihy**) nastavena na **Ne**.

[![Možnost Zaúčtovat opravy faktur do pohledávek je nastavena na Ne](./media/37_rev-rec-scenarios.png)](./media/37_rev-rec-scenarios.png)

Pro odběratele US\_SI\_0003 je vytvořena prodejní objednávka. Odběratel si koupí přenosný počítač (číslo položky S0012), instalační služby (číslo položky S0001) a plán podpory přenosného počítače (číslo položky S0008, „Trvalé inženýrské služby“). Výnosy za přenosný počítač a instalační služby jsou okamžitě uznány. Výnosy za plán podpory budou odloženy a uznány za 12 měsíců, jak je definováno časovým obdobím ve smlouvě.

[![Řádky prodejní objednávky pro přenosný počítač, instalační služby a plán podpory](./media/38_rev-rec-scenarios.png)](./media/38_rev-rec-scenarios.png)

Prodejní objednávka je potvrzena. Protože jsou všechny tři položky nastaveny pro přidělení výnosové ceny, při potvrzení prodejní objednávky se vypočítá výnosová cena. Výnosy, které budou uznány, můžete zobrazit na stránce **Přidělení výnosové ceny** (na stránce **Prodejní objednávka** v podokně akcí na kartě **Spravovat** ve skupině **Uznání výnosů** vyberte **Přidělení výnosové ceny**). Výnos za přenosný počítač bude zaúčtován na účet výnosů ve výši $995,84. Výnosy za instalační služby budou také zaúčtovány na účet výnosů ve výši $314,47. Výnosy za plán podpory budou zaúčtovány na účet odložených výnosů ve výši $188,69. Součet výnosových cen se musí rovnat součtu řádků, které byly nastaveny pro zachytávání přidělení výnosových cen ($1499).

[![Stránka Přidělení výnosové ceny](./media/39_rev-rec-scenarios.png)](./media/39_rev-rec-scenarios.png)

Odběrateli je fakturován přenosný počítač a plán podpory, nikoli však instalační služby. Následující obrázek znázorňuje účetní položku, která je zaúčtovaná pro fakturu.

[![Účetní položka pro fakturovanou prodejní objednávku](./media/40_rev-rec-scenarios.png)](./media/40_rev-rec-scenarios.png)

Účetní položka zaúčtuje do pohledávek částku $1276,94. Protože je však tato faktura částečná, výnosy nebo odložené výnosy plus daň se nerovnají výši pohledávek. Rozdíl -$14,47 je zaúčtován na clearingový účet výnosů částečné faktury.

Je také vytvořen plán uznání výnosů.

[![Stránka plánu uznání výnosů pro částečnou fakturu](./media/41_rev-rec-scenarios.png)](./media/41_rev-rec-scenarios.png)

Později se zákazník rozhodne nekupovat instalační služby. Proto je tento řádek odebrán z prodejní objednávky. Nyní nelze prodejní objednávku znovu potvrdit, protože na ní zůstávají pouze fakturované řádky.

[![Prodejní objednávka po odebrání řádku instalačních služeb](./media/42_rev-rec-scenarios.png)](./media/42_rev-rec-scenarios.png)

Ačkoli nelze prodejní objednávku potvrdit, lze ji opětovně přidělit. V prodejní objednávce volbou **Opětovné přidělení ceny k novým řádkům objednávky** otevřete stránku **Opětovné přidělení ceny k novým řádkům objednávky**. Vyberte dva zbývající řádky prodejní objednávky a poté vyberte **Aktualizovat opětovné přidělení**. Sloupec **Opětovně přidělená částka** zobrazí pro každý zbývající řádek prodejní objednávky novou výnosovou cenu.

[![Nové výnosové ceny na stránce Opětovné přidělení ceny k novým řádkům objednávky](./media/43_rev-rec-scenarios.png)](./media/43_rev-rec-scenarios.png)

Dále volbou **Očekávaný doklad** zobrazíte účetní položky.

[![Účetní položky na stránce Očekávaný doklad](./media/44_rev-rec-scenarios.png)](./media/44_rev-rec-scenarios.png)

Posledních pět řádků na stránce **Očekávaný doklad** stornuje původní účetní položku ze zaúčtované faktury. První čtyři řádky jsou nové účetní položky, které jsou zaúčtovány pro fakturu. Je důležité vědět, že odběrateli není nepředložena nová faktura. Po opětovném přidělení dluží odběratel stále $1276,94, což je částka, která musí být zaúčtována do pohledávek v nové účetní položce. Nové výnosy nebo odložené výnosy plus daň se rovnají částce $1276,94. Proto nemusíte provést zaúčtování na clearingový účet výnosů částečné faktury.

Opětovné přidělení dokončíte tlačítkem **Zpracovat**. Je zadáno datum zaúčtování. Po dokončení se opětovné přidělení projeví u obou zbývajících položek na stránce **Přidělení výnosové ceny**.

[![Opětovné přidělení ceny pro zbývající položky na stránce Přidělení výnosové ceny](./media/45_rev-rec-scenarios.png)](./media/45_rev-rec-scenarios.png)

Na základě nové ceny vzniklé opětovným přidělením výnosů byl rovněž aktualizován plán uznání výnosů. Z prodejní objednávky otevřete stránku **Plán uznání výnosů**. Dříve měla položka S0008 13 řádků (této položce byl přiřazen 12měsíční plán). Nyní má 39 řádků: 13 řádků původního plánu, 13 řádků plánu stornování a 13 řádků, které vycházejí z nové výnosové ceny.

[![Aktualizovaná stránka plánu uznání výnosů s 39 řádky pro položku S0008](./media/46_rev-rec-scenarios.png)](./media/46_rev-rec-scenarios.png)

Když vyberete **Doklad**, deník faktur obsahuje původní účetní položku. Chcete-li zobrazit stornující a novou účetní položku prodejní objednávky, v podokně akcí vyberte **Úpravy výnosů** a poté vyberte **Doklad**.

Dále otevřete stránku **Všichni odběratelé** (**Pohledávky \> Odběratelé \> Všichni odběratelé**), vyberte odběratele **US\_SI\_0003** a potom vyberte **Transakce**. Stránka **Transakce odběratele** obsahuje pouze původní fakturu (000008) spolu s původní účetní položkou. Protože je možnost **Zaúčtovat opravy faktur do pohledávek při opětovném přidělení** na stránce **Parametry hlavní knihy** nastavena na **Ne**, aktualizuje se pouze hlavní kniha. Proto se nezobrazují stornovací a aktualizované účetní položky. Všimněte si, že jsou zobrazeny transakce úprav výnosů, které byly vytvořeny ve [scénáři 3](rev-rec-reallocation-scenario-3.md).

[![Původní účetní položka na stránce Transakce odběratele](./media/47_rev-rec-scenarios.png)](./media/47_rev-rec-scenarios.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
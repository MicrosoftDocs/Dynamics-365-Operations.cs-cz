---
title: Opětovné přidělení uznání výnosů – scénář 3
description: Toto téma popisuje scénář opětovného přidělení, kdy je do existující fakturované prodejní objednávky přidán nový řádek. Je-li do smlouvy přidána nová položka, lze ji přidat buď do nové, nebo do existující prodejní objednávky.
author: kweekley
manager: aolson
ms.date: 12/21/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-21
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 51646d27fe8c343c99360815d22949ffe0757979
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003347"
---
# <a name="revenue-recognition-reallocation--scenario-3"></a>Opětovné přidělení uznání výnosů – scénář 3

[!include [banner](../includes/banner.md)]

Toto téma popisuje scénář opětovného přidělení, kdy je do existující fakturované prodejní objednávky přidán nový řádek. Je-li do smlouvy přidána nová položka, lze ji přidat buď do nové, nebo do existující prodejní objednávky. Tento scénář také ukazuje, co se stane, když jsou kvůli opětovnému přidělení aktualizovány pohledávky.

V tomto scénáři je možnost **Zaúčtovat opravy faktur do pohledávek při opětovném přidělení** na kartě **Uznání výnosů** na stránce **Parametry hlavní knihy** (**Uznání výnosů \> Nastavení \> Parametry hlavní knihy**) nastavena na **Ano**.

[![Možnost Zaúčtovat opravy faktur do pohledávek je nastavena na Ano](./media/25_rev-rec-scenarios.png)](./media/25_rev-rec-scenarios.png)

Pro odběratele US\_SI\_0003 je vytvořena prodejní objednávka. Odběratel si kupuje přenosný počítač (číslo položky S0012) a plán podpory (číslo položky S0008, „Trvalé inženýrské služby“). Výnosy za přenosný počítač jsou okamžitě uznány. Výnosy za plán podpory budou odloženy a uznány za 12 měsíců, jak je definováno časovým obdobím ve smlouvě.

[![Řádky prodejní objednávky pro přenosný počítač a plán podpory](./media/26_rev-rec-scenarios.png)](./media/26_rev-rec-scenarios.png)

Prodejní objednávka je potvrzena. Protože jsou obě položky nastaveny pro přidělení výnosové ceny, při potvrzení prodejní objednávky se vypočítá výnosová cena. Výnosy, které budou uznány, můžete zobrazit na stránce **Přidělení výnosové ceny** (na stránce **Prodejní objednávka** v podokně akcí na kartě **Spravovat** ve skupině **Uznání výnosů** vyberte **Přidělení výnosové ceny**). Výnos za přenosný počítač bude zaúčtován na účet výnosů ve výši $1008,01. Výnosy za plán podpory budou zaúčtovány na účet odložených výnosů ve výši $190,99. Součet výnosových cen se musí rovnat součtu řádků, které byly vytvořeny pro zachytávání přidělení výnosových cen ($1199,00).

[![Stránka Přidělení výnosové ceny](./media/27_rev-rec-scenarios.png)](./media/27_rev-rec-scenarios.png)

Prodejní objednávka je plně fakturována. Následující obrázek znázorňuje účetní položku, která je zaúčtovaná pro fakturu.

[![Účetní položka pro plně fakturovanou prodejní objednávku](./media/28_rev-rec-scenarios.png)](./media/28_rev-rec-scenarios.png)

Je také vytvořen plán uznání výnosů. Po nějakém čase dojde k uznání výnosů za dva měsíce v rámci plánu podpory.

[![Stránka s plánem uznání výnosů po uplynutí dvou měsíců](./media/29_rev-rec-scenarios.png)](./media/29_rev-rec-scenarios.png)

V tomto okamžiku se odběratel rozhodne přidat instalační služby (číslo položky S0001). Tato položka je přidána na existující prodejní objednávku. Odběratel je vyzván k potvrzení, že chce upravit plně fakturovanou prodejní objednávku, a vybere **Ano**.

[![Prodejní objednávka po přidání řádku instalačních služeb](./media/30_rev-rec-scenarios.png)](./media/30_rev-rec-scenarios.png)

Pokud je tato nová položka jedinou změnou ve smlouvě odběratele, lze nyní spustit proces opětovného přidělení. V prodejní objednávce volbou **Opětovné přidělení ceny k novým řádkům objednávky** otevřete stránku **Opětovné přidělení ceny k novým řádkům objednávky**. Vyberte všechny řádky prodejní objednávky a poté vyberte **Aktualizovat opětovné přidělení**. Sloupec **Opětovně přidělená částka** zobrazuje pro každý řádek prodejní objednávky novou výnosovou cenu.

[![Nové výnosové ceny na stránce Opětovné přidělení ceny k novým řádkům objednávky](./media/31_rev-rec-scenarios.png)](./media/31_rev-rec-scenarios.png)

Dále volbou **Očekávaný doklad** zobrazíte účetní položky. Protože je možnost **Zaúčtovat opravy faktur do pohledávek při opětovném přidělení** na stránce **Parametry hlavní knihy** nastavena na **Ano**, tyto účetní položky budou zaúčtovány do hlavní knihy prostřednictvím dokumentu akreditivu a v pohledávkách bude vytvořena nová faktura.

[![Účetní položky na stránce Očekávaný doklad](./media/32_rev-rec-scenarios.png)](./media/32_rev-rec-scenarios.png)

Poslední čtyři řádky na stránce **Očekávaný doklad** stornují původní účetní položku ze zaúčtované faktury. Prvních pět řádků jsou nové účetní položky, které jsou zaúčtovány pro fakturu. Je důležité vědět, že odběrateli není nepředložena nová faktura. Po opětovném přidělení dluží odběratel stále $1276,94, což je částka, která musí být zaúčtována do pohledávek v nové účetní položce. Započtená daň a výnosy nebo odložené výnosy se rovnají $995,83 + $188,69 + $77,94 = $1262,46. Výše výnosů nebo odložených výnosů se z důvodu opětovného přidělení změnila. Rozdíl -$14,48 je zaúčtován na clearingový účet výnosů částečné faktury. Tento zůstatek bude vymazán při zaúčtování faktury pro novou položku, která byla přidána na prodejní objednávku.

Opětovné přidělení dokončíte tlačítkem **Zpracovat**. Je zadáno datum zaúčtování. Po dokončení se opětovné přidělení projeví u všech třech položek na stránce **Přidělení výnosové ceny**.

[![Opětovně přidělené ceny u všech tří položek na stránce Přidělení výnosové ceny](./media/33_rev-rec-scenarios.png)](./media/33_rev-rec-scenarios.png)

Na základě nové ceny vzniklé opětovným přidělením výnosů byl rovněž aktualizován plán uznání výnosů. Z prodejní objednávky otevřete stránku **Plán uznání výnosů**. Dříve měla položka S0008 13 řádků (této položce byl přiřazen 12měsíční plán). Nyní má 39 řádků: 13 řádků původního plánu, 13 řádků plánu stornování a 13 řádků, které vycházejí z nové výnosové ceny.

[![Aktualizovaná stránka plánu uznání výnosů s 39 řádky pro položku S0008](./media/34_rev-rec-scenarios.png)](./media/34_rev-rec-scenarios.png)

Když vyberete **Doklad**, deník faktur obsahuje původní účetní položku. Chcete-li zobrazit stornující a novou účetní položku prodejní objednávky, v podokně akcí vyberte **Úpravy výnosů** a poté vyberte **Doklad**.

Dále otevřete stránku **Všichni odběratelé** (**Pohledávky \> Odběratelé \> Všichni odběratelé**), vyberte odběratele **US\_SI\_0003** a potom vyberte **Transakce**. Stránka **Transakce odběratele** obsahuje původní fakturu (000006), stornovací doklad (000006-1) a novou fakturu (000006-2). Původní faktura a stornovací doklad jsou vzájemně vyrovnány a mají zůstatek 0 (nula). Pokud chcete vidět dopad v hlavní knize, pro jednotlivé dokumenty zobrazte doklad.

[![Původní faktura, stornovací doklad a nová faktura na stránce Transakce odběratele](./media/35_rev-rec-scenarios.png)](./media/35_rev-rec-scenarios.png)

Pro přidanou položku je znovu zaúčtována prodejní objednávka. Celková faktura předložená odběrateli je ve výši $300 + daň $19,50 = $319,50. Následující obrázek znázorňuje zaúčtovanou účetní položku.

[![Stránka transakcí dokladů se zaúčtovanou účetní položkou](./media/36_rev-rec-scenarios.png)](./media/36_rev-rec-scenarios.png)

Protože součet výnosů a prodeje je vyšší než $319,50, zaúčtovaný rozdíl je $14,48. Tato částka vymaže zůstatek z clearingového účtu výnosů částečné faktury. Tento zůstatek byl aktualizován v nové účetní položce zaúčtované po opětovném přidělení.

---
title: "Výpočty kusovníků se standardními náklady"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcGroup, BOMCalcTable, ProdParmBOMCalc
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 65571
ms.assetid: ca17e6dd-b16a-4bbc-8682-b16345ab9906
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0f539e286b9f16aec3c73934403ba41f2641e6e0
ms.contentlocale: cs-cz
ms.lasthandoff: 05/25/2017


---

# <a name="bom-calculations-with-standard-costs"></a>Výpočty kusovníků se standardními náklady

[!include[banner](../includes/banner.md)]




Mezi informace o zakoupené položce, které jsou použity ve výpočtu kusovníku pro standardní náklady, patří následující:
-   Náklady: Náklady na zakoupenou položku jsou spravovány jako záznamy nákladů specifické podle pracovišť v rámci nákladové verze pro standardní náklady. Každému záznamu o nákladech odpovídá efektivní datum a datum výpočtu kusovníku určuje záznam nákladů, který bude použit. Může se například stát, že ve výpočtu kusovníku s budoucím datem výpočtu bude použit záznam nákladů s nevyřízeným stavem a budoucím efektivním datem.
-   Nákladová skupina − Nákladová skupina, která je přiřazena k zakoupené položce, poskytuje základ pro rozdělení nákladů do segmentů v rámci vypočtených nákladů vyráběné položky.
-   Podmínky pro varovnou zprávu vložené do skupiny výpočtu kusovníku položky umožňují ve výpočtu kusovníku identifikovat možné problémy. To může být v případech, kdy má zakoupená položka nulové náklady, když je nulové množství v kusovníku nebo když je zastaralý záznam nákladů. Použitelné podmínky pro varovnou zprávu mohou být při inicializaci výpočtu kusovníku potlačeny.

Mezi údaje o vyráběné položce, které jsou použity ve výpočtu kusovníku pro standardní náklady, patří následující:
-   Standardní množství objednávky pro sklad: Standardní množství objednávky pro položku pro sklad, je použito jako výchozí účetní velikost šarže pro amortizaci konstantních nákladů ve výpočtu kusovníku. Účetní velikost šarže bude také odrážet násobek množství objednávky (je-li zadán).
-   Podmínky pro varovnou zprávu vložené do skupiny výpočtu kusovníku položky umožňují ve výpočtu kusovníku identifikovat možné problémy. Jako jeden příklad může být vyrobená položka, která nemá kusovník nebo postup. Použitelné podmínky pro varovnou zprávu mohou být při inicializaci výpočtu kusovníku potlačeny.

Mezi údaje kusovníku, které jsou použity ve výpočtu kusovníku pro standardní náklady, patří následující:
-   Verze kusovníku − Verze kusovníku, která je přiřazena k vyráběné položce, má efektivní počáteční a koncové datum a schválený a aktivní stav. Verze kusovníku může být platná pro celou společnost nebo specifická pro jednotlivé pracoviště a může volitelně odrážet různé množstevní kategorie.
-   Množství položky na řádku kusovníku − Komponenta má obvykle požadované variabilní množství, avšak může se jednat o konstantu. Množství komponenty je obvykle vyjádřeno pro výrobu jedné nadřazené položky, avšak může být také vyjádřeno s použitím 100 nebo 1000 jednotek s cílem zajistit vyšší desetinnou přesnost. Množství komponenty může být vypočteno také na základě měření.
-   Odpad položky řádku kusovníku − Komponentě může pro plánovaný odpad odpovídat variabilní nebo konstantní množství.
-   Platná data položky řádku kusovníku − Komponenta může mít platné počáteční a koncové datum.
-   Typ výroby položky řádku kusovníku: Velikost nákladové šarže pro amortizaci konstantních nákladů bude odrážet množství z výpočtu kusovníku a režim rozpadu zhotovení na objednávku, protože pro výpočet kusovníku je předpokládáno, že vyráběná komponenta bude vyráběna do dosažení přesného množství (namísto příslušného standardního množství objednávky).
-   Dílčí kusovník pro vyráběnou komponentu − Vyráběná komponenta může volitelně mít specifikovanou verzi kusovníku, která bude ve výpočtu kusovníku používána namísto aktuální aktivní verze kusovníku pro danou položku.
-   Dílčí postup pro vyráběnou komponentu - Vyráběná komponenta může volitelně mít specifikovanou verzi postupu, která bude ve výpočtu kusovníku používána namísto aktuální aktivní verze postupu pro danou položku.
-   Číslo operace a dopad procentuální hodnoty odpadu pro operaci − Číslo operace odkazuje na komponentu pro specifickou operaci a operacím mohou také odpovídat procentuální hodnoty odpadu. Toto propojení umožňuje, aby ve výpočtech kusovníku byly započítány procentuální hodnoty odpadu nebo také kumulativní procentuální hodnoty odpadu přes více operací pro zjištění požadovaného množství komponenty.
-   Ignorovat položku řádku kusovníku − Určitou komponentu lze pro účely výpočtu ignorovat.

Mezi informace o provozních prostředcích, které jsou použity ve výpočtu standardních nákladů kusovníku, patří následující:
-   Hodinové náklady: Hodinové náklady, které jsou asociovány s provozním prostředkem, jsou vyjádřeny jako nákladové kategorie přiřazených k času přípravy a operačnímu času. Tyto nákladové kategorie musí být určeny pro skupiny prostředků a provozní prostředky. Hodinové náklady asociované s nákladovou kategorií mohou být platné v celé společnosti nebo mohou být specifické podle pracovišť.
-   Jednotkové náklady: V některých výrobních prostředích se přiřazují náklady provozního prostředku na výstupní jednotku, což by bylo vyjádřeno jako jiná nákladová kategorie pro množství. Náklady související s množstvím mohou například odrážet pracovní sazby na jeden kus nebo například výrobce barev může přiřadit náklady provozního prostředku na litr výstupního produktu.
-   Přepsání údajů provozního prostředku pro operace postupu: Údaje prostředku o nákladových kategoriích budou zděděny různými operacemi, kde mohou být přepsány. Ve výpočtech kusovníku budou použity údaje nákladových kategorií specifikované pro operace postupu.
-   Nákladová skupina pro nákladovou kategorii − Nákladová skupina, která je přiřazena k nákladové kategorii, zajišťuje rozdělení nákladů do segmentů ve vypočtených nákladech na vyráběnou položku. Různé nákladové skupiny mohou být například použity pro segmentaci vypočtených nákladů, které jsou asociovány se stroji a s prací nebo s časem přípravy a operačním časem.

Mezi informace postupů, které jsou použity ve výpočtu standardních nákladů kusovníku, patří následující:
-   Verze postupu - Verze postupu, která je přiřazena k vyráběné položce, má efektivní počáteční a koncové datum a schválený a aktivní stav. Verze postupu musí být specifická pro jednotlivé pracoviště a může volitelně odrážet různé množstevní kategorie.
-   Operační čas postupu − Čas může být vyjádřen jako operační čas a čas přípravy. Množství komponenty je obvykle vyjádřeno pro výrobu jedné nadřazené položky, avšak může být také vyjádřeno s použitím 100 nebo 1000 jednotek s cílem zajistit vyšší desetinnou přesnost.
-   Operační čas postupu pro sekundární prostředky: Sekundární prostředek má stejné číslo operace jako primární prostředek a má stejný operační čas postupu. Určitá operace může například vyžadovat jako primární zdroj některý stroj a jako sekundární zdroje práci a nástroje.
-   Procentuální hodnota odpadu pro operaci postupu: Výpočty kusovníku zohlední procentuální hodnoty odpadu nebo také kumulativní procentuální hodnoty odpadu přes více operací. To se vztahuje na požadovanou dobu pro operace postupu a požadované množství pro komponenty, které jsou propojeny s čísly operací.
-   Nákladové kategorie pro operace postupu: Údaje provozního prostředku ohledně kategorií nákladů budou zděděny operacemi, kde mohou být přepsány. Ve výpočtech kusovníku budou použity údaje nákladových kategorií specifikované pro operace postupu.

Mezi informace o výrobní režii, které jsou použity ve výpočtu standardních nákladů kusovníku, patří následující:
-   Příplatek − Vzorec pro výpočet příplatku odráží procentuální hodnotu (například 100 procent), která se váže na určitou nákladovou skupinu (například práce).
-   Sazba − Vzorec pro výpočet sazby odráží jednotkové množství (například 10,00 USD za hodinu), které se váže ke specifické nákladové skupině (například práce).
-   Režijní náklady založené na čase v porovnání s režijními náklady založenými na materiálu − Režijní náklady na výrobu mohou být vázány na operace postupu nebo na komponenty materiálu.

Mezi informace o nákladových verzích, které jsou použity ve výpočtu standardních nákladů kusovníku, patří následující:
-   Typ nákladů − Nákladová verze musí obsahovat standardní náklady. Pro výpočty kusovníku, které používají standardní náklady, platí určitá omezení. Tato omezení například určují, že do jednotkových nákladů musí být zahrnuty vedlejší náklady a že režim rozpadu výpočtu kusovníku musí mít jedinou úroveň.
-   Mandátní záložní princip − V nákladové verzi může být určeno povinné použití záložního principu, jako například použití určené nákladové verze nebo aktivních záznamů nákladů. Mandátní záložní princip se obvykle týká nákladové verze, která reprezentuje přírůstkové aktualizace pro metodu aktualizace nákladů se dvěma verzemi.
-   Příznak blokování pro nevyřízené náklady − Příznak blokování může zabránit výpočtům kusovníku pro nevyřízené náklady na vyráběné položky.
-   Určené počáteční datum − Určené počáteční datum bude považováno za výchozí datum výpočtu pro všechny výpočty kusovníku, které zahrnují danou nákladovou verzi.
-   Určené pracoviště − Při zadání určeného pracoviště budou výpočty kusovníku omezeny na jediné pracoviště.
-   Obsah nákladové verze musí zahrnovat náklady − Obsah musí zahrnovat náklady. Může volitelně zahrnovat prodejní ceny s cílem vypočítat navržené prodejní ceny pro vyráběné položky.

Při inicializaci výpočtu kusovníku lze určit několik zdrojů informací. Mezi ně patří pracoviště, datum výpočtu nebo nákladová verze.







---
title: Metoda přidělení celkových nákladů
description: Toto téma obsahuje pokyny pro používání celkových přidělených nákladů. Celkové přidělené náklady je metoda výpočtu nákladů mezi hlavní položkou receptury pro dávkovou objednávku a vedlejšími produkty, které jsou definovány pro recepturu.
author: AndersGirke
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMConsistOf, PmfFormulaCoBy
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83852
ms.assetid: 7c14c3e5-9476-4a79-a210-e77fc91cc7fc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cda1c5251b81a3bb73d4d8703d7c3fa1ab4e9c16
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/29/2019
ms.locfileid: "341573"
---
# <a name="total-cost-allocation-method"></a>Metoda přidělení celkových nákladů

[!include [banner](../includes/banner.md)]

Toto téma obsahuje pokyny pro používání celkových přidělených nákladů. Celkové přidělené náklady je metoda výpočtu nákladů mezi hlavní položkou receptury pro dávkovou objednávku a vedlejšími produkty, které jsou definovány pro recepturu.

Celkové přidělené náklady je metoda výpočtu nákladů mezi hlavní položkou receptury pro dávkovou objednávku a vedlejšími produkty, které jsou definovány pro recepturu. Tato metoda je dynamická. Vypočítává náklady jako vážený průměr mezi množstvím, která jsou hlášena jako dokončená pro položku receptury a vedlejší produkty. Při použití celkových přidělených nákladů nemusíte kontrolovat přidělení nákladů pro každou dávkovou objednávku. Pokud nejsou použity celkové přidělené náklady, kalkulace receptury používá existující funkce.

## <a name="using-tca-for-coproducts"></a>Použití celkových přidělených nákladů pro vedlejší produkty
Zde jsou uvedeny některé pokyny týkající se použití celkových přidělených nákladů pro vedlejší produkty:

-   Nastavíte-li posuvník **Celkové přidělené náklady** na **Ano** pro verzi receptury, musí mít vedlejší produkty nákladovou cenu, která je větší než 0 (nula). Hodnota může být získána z aktivní nákladové verze pro stejné pracoviště, nebo pro první pracoviště pro recepturu, která není specifická pro pracoviště. Tento stav je ověřen při schválení receptury.

    -   Není nutné zadávat procento přidělených nákladů pro vedlejší produkty ručně. Místo toho systém automaticky vytvoří procento přidělených nákladů jako průměr aktivních nákladových cen vedlejších produktů. 
    -   Nemusíte zadávat standardní náklady pro nestandardní nákladové položky, které jsou vedlejšími produkty. Existují dva typy nákladových verzích v systému: standardní náklady a plánované náklady 
    -   Pokud je položka ohodnocena podle oceňovací metody standardních nákladů, doporučujeme použít aktivní nákladové ceny ve verzi plánovaných nákladů. Tato cena je použita pro odhad nákladů, například výpočte kusovníku, odhad výrobních nákladů a záložní cenu v procesu ocenění zásob. 

-   Nastavíte-li posuvník **Celkové přidělené náklady** na **Ano** pro verzi receptury a následující podmínky budou splněny, je jako metoda použita **Celkové přidělené náklady** a procentuální hodnota přidělení nákladů se nemění:
    -   Přidali jste vedlejší produkty.
    -   Použili jste jinou metodu přidělení nákladů pro vedlejší produkty.
-   Nastavíte-li posuvník **Celkové přidělené náklady** na **Ne** pro verzi receptury a následující podmínky budou splněny, je jako metoda použita **Ručně** a procentuální hodnota přidělení nákladů se nemění:
    -   Přidali jste vedlejší produkty.
    -   Procento přidělení nákladů je vyšší než 0 (nula).
-   Před úspěšným provedením výpočtu receptury je nutné odhadnout procento přidělení nákladů. Tento krok lze dokončit ručně nebo pomocí možnosti **Odhadnout náklady** na stránce **Vedlejší produkty**. **Poznámka:** možnost **Odhadnout náklady** je dostupná pouze v případě, že je posuvník **Celkové přidělené náklady** nastaven na **Ano** pro verzi receptury. Můžete si prohlédnout předpokládané přidělení, pokud množství dávkové objednávky, která jsou hlášena jako dokončená, odpovídají množství uvedenému v receptuře.
-   Pokud je dávková objednávka vytvořena ručně, nebo je plánovaná dávková objednávka upevněna, posuvník **Celkové přidělené náklady** pro verzi receptury je zkopírován do dávkové objednávky. Lze však změnit toto nastavení pro dávkovou objednávku. Pokud je posuvník **Celkové přidělené náklady** nastaven na **Ne** pro verzi receptury, a poté převeden na **Ano** pro dávkovou objednávku, metoda přidělení nákladů pro každý řádek, který byl nastaven na **Ručně**, se změní na **Celkové přidělené náklady**. Přidělení nákladů **Žádná** zůstane nezměněn. Pokud je posuvník **Celkové přidělené náklady** nastaven na **Ano** pro verzi receptury, a poté převeden na **Ne** pro dávkovou objednávku, metoda přidělení nákladů pro každý vedlejší produkt typu **Výroba** se změní na **Ručně**. Všechna odhadovaná procenta přidělení nákladů zůstávají nezměněna.
-   Stránka **Přidělení nákladů vedlejšího produktu** zobrazuje vypočtené procento přidělení nákladů. Můžete otevřít tuto stránku ze stránky **Dávková objednávka**. Tyto informace jsou užitečné, pokud se výrobky a množství, která jsou hlášena, liší od plánovaného nebo zahájeného množství z dávkové objednávky. Po dokončení nákladů se tato nová přidělení procenta z celkových přidělených nákladů zobrazí na stránce **Přidělení nákladů vedlejšího produktu**.

## <a name="calculating-the-burden-for-byproducts"></a>Výpočet režie pro vedlejší produkty
Pole **Přidělení nákladů vedlejšího produktu** na stránce **Vedlejší produkty** je čítací pole, které se používá jen u vedlejších produktů. Pro vedlejší produkty je hodnota v tomto poli vždy **Žádný**. Pro řádky vedlejších produktů toto pole určuje, jak je částka nákladů pro daný řádek vedlejšího produktu přidán do celkových nákladů na výrobu. Existují tyto možnosti:

-   **Žádná** ─ žádná částka není přidána do celkových nákladů na výrobu pro tento řádek vedlejšího produktu.
-   **Procento** ─ částka nákladů se vypočítá jako procento z celkových nákladů na suroviny, které jsou spotřebovány ve výrobě. Do pole se zadává podíl, který se používá pro výpočet.
-   **Po řadách** ─ částka nákladů se vypočítává jako částka pro standardní velikost dávky ve výrobní zakázce. Tato částka je nezávislá na hlášeném množství ve výrobě. Do pole se zadává částka, která se používá pro výpočet.
-   **Podle množství** ─ částka nákladů se vypočítává jako částka za hlášené množství položky receptury ve výrobě. Do pole se zadává částka, která se používá pro výpočet.





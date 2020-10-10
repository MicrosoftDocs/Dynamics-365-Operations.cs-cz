---
title: Výpočty hodnoty BOM
description: Shrnutí nákladů a výpočty prodejní ceny jsou označovány jako výpočty kusovníku a spouštějí se ze stránky Výpočty. V tomto tématu jsou informace o výpočtech kusovníku.
author: AndersGirke
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion, InventItemPrice, ProdSetupCostEstimation
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 273763
ms.assetid: c6fa3348-eafa-4847-9132-e65c5f55cbf4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: f90e5babb440a2226638f7d96f111816732f0e70
ms.sourcegitcommit: 175f9394021322c685c5b37317c2f649c81a731a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/21/2020
ms.locfileid: "3826759"
---
# <a name="bom-calculations"></a>Výpočty hodnoty BOM

[!include [banner](../includes/banner.md)]

Shrnutí nákladů a výpočty prodejní ceny jsou označovány jako výpočty kusovníku a spouštějí se ze stránky Výpočty. V tomto tématu jsou informace o výpočtech kusovníku.

Shrnutí nákladů a výpočty prodejní ceny jsou označovány jako výpočty kusovníku a spouštějí se ze stránky **Výpočty**. Stránka **Výpočty** slouží k provádění následujících úkolů:

-   Výpočet nákladů na vyráběnou položku a generování přidruženého záznamu nákladů na položku v rámci verze stanovení nákladů.
-   Výpočet prodejní ceny vyráběné položky a generování přidruženého záznamu prodejní ceny položky v rámci verze stanovení nákladů.

Způsob, kterým používáte stránku **Výpočty**, se mírně liší v závislosti na tom, jakým způsobem zahájíte výpočet kusovníku. Způsob, jakým používáte stránku **Výpočty**, rovněž závisí na tom, zda kalkulace kusovníku zahrnuje nákladovou verzi pro standardní náklady nebo pro plánované náklady. Záleží také na některých zásadách definovaných v rámci nákladové verze použité v kalkulaci kusovníku. **Poznámka:** Varianta stránky **Výpočty** se používá v souvislosti s prodejní objednávkou, prodejní nabídkou nebo v souvislosti s řádkem servisní zakázky. Tyto výpočty se označují jako výpočty kusovníku pro konkrétní objednávku. Výpočet kusovníku specifický podle objednávky nevygeneruje záznam o nákladech na položku v rámci nákladové verze. Místo toho vygeneruje záznam výpočtu, který se zobrazí na stránce **Podrobnosti výpočtu kusovníku**. Záznam o kalkulaci obsahuje vypočtené náklady a vypočtenou prodejní cenu. Stránku **Výpočty** lze otevřít pro jednu vyrobenou položku nebo pro nákladovou verzi:

-   K výpočtu nákladů na jednu vyrobenou položku spusťte kalkulace kusovníku ze stránky **Cena položky**. Stránka **Výpočty** dědí identifikátor položky. Musí být zadána verze nákladů, verze kusovníku, verze postupu, množství pro výpočet, datum výpočtu a pracoviště.
    -   Podle výchozího nastavení jsou verze kusovníku a verze postupu nastaveny na aktivní verzi pro položku, pracoviště, datum a výpočet množství. Výchozí hodnoty se schválenými verzemi však lze přepsat.
    -   Ve výchozím nastavení je množství pro výpočet nastaveno na standardní množství objednávky položky. Výchozí hodnotu však můžete přepsat.
    -   Datum výpočtu nebo pracoviště mohou být dány nákladovou verzí nebo lze nastavit hodnoty specifikované uživatelem, pokud nejsou určené v nákladové verzi. Budoucí datum výpočtu určuje způsob použití čekajících záznamů o nákladech. V kalkulacích kusovníku bude použit čekající záznam o nákladech, jehož nejbližší datum zahájení odpovídá dni výpočtu kusovníku nebo je před tímto datem.
-   Pokud chcete vypočítat náklady pro všechny vyráběné položky nebo vybrané položky nebo aktualizovat položky na základě využití, můžete spustit výpočty kusovníku ze stránky **Nastavení verze výpočtu nákladů** nebo **Údržba verze výpočtu nákladů**. Stránka **Výpočty** dědí verzi výpočtu nákladů.
    -   Při výpočtech se předpokládá použití aktivní verze kusovníku a aktivní verze technologického postupu pro vyrobenou položku (a souvisejícího skladu, data a množství), pokud vyrobené součásti nemají zadaný dílčí kusovník nebo dílčí technologický postup.
    -   U výpočtů se předpokládá, že se používá standardní množství na objednávce pro vyrobené položky. Standardní množství objednávky poskytuje základnu pro výpočet množství součástí, určení platných verzí kusovníků a technologických postupů (když používáte kusovníky a postupy citlivé na množství) a amortizaci konstantních nákladů. Uvedený předpoklad se však nepoužije, pokud vyrobená součást má řádek kusovníku typu **výroba** nebo **dodavatel**, případně když při výpočtech kusovníku používáte režim rozpadu zakázkové výroby, tento předpoklad neplatí, protože množství bude odrážet zadané vypočtené množství.
    -   Datum výpočtu nebo pracoviště mohou být dány nákladovou verzí nebo lze nastavit hodnoty specifikované uživatelem, pokud nejsou určené v nákladové verzi.

Ostatní varianty výpočtů kusovníků odrážejí nákladový typ a omezení nákladové verze:

-   Kalkulace kusovníků, které používají standardní náklady, musí být omezeny zásadami nákladové verze, protože tato omezení pomáhají zajistit použití standardních zásad výpočtu nákladů. Standardní principy ocenění vyžadují dodržování zásad, které se týkají používání standardních cen nakupovaných položek, jednoúrovňového režimu rozpadu a zahrnutí vedlejších nákladů do jednotkových nákladů.
-   Naproti tomu kalkulace kusovníků využívající plánované náklady se nemusejí řídit standardními principy ocenění. V těchto kalkulacích se mohou používat různé režimy rozpadu, alternativní zdroje dat o cenách nakupovaných položek a volitelná vynucení omezení v rámci nákladové verze.

### <a name="bom-calculations-that-use-standard-costs"></a>Kalkulace kusovníků se standardními náklady

Zásady v rámci nákladové verze (pro standardní náklady) umožňují nařídit dodržování pěti zásad v kalkulacích kusovníků. Možnost **Omezení záznamu** v nákladové verzi nařizuje jednu z těchto zásad, kde vedlejší náklady musejí být zahrnuty do jednotkové ceny. Zatímco vedlejší náklady pro nakoupené položky lze zadat ručně, zatímco vedlejší náklady pro vyrobené položky představují vypočítanou amortizaci konstantních nákladů. Možnost **Omezení výpočtu** v rámci nákladové verze nařizuje zbývající čtyři zásady kalkulace kusovníků:

-   Zdroj příspěvku nákladů u nakoupených položek musí být založen na standardních nákladech. Jinými slovy to znamená, že kalkulace kusovníku musejí používat záznamy o ceně položky v rámci určité nákladové verze nebo v rámci zálohy, která obsahuje standardní náklady.
-   Na pomoc při zajištění přesných a konzistentních výpočtů standardních nákladů musí být režim rozpadu jednoúrovňový, což zajišťuje přesný a konzistentní výpočet standardních nákladů.
-   Mají-li být při výpočtu prodejní ceny položky dosaženy konzistentní výsledky, musí být nastavení zisku nařízeno. Chcete-li použít nastavení zisku a generovat záznamy o prodejních cenách položek, musí nákladová verze umožnit zahrnutí prodejních cen.
-   Princip zálohy musí být nařízen a nastaven na **Žádný**, **Aktivní** (u aktivních záznamů nákladů) nebo **Verze výpočtu nákladů** (pro konkrétní verzi výpočtu nákladů).

### <a name="bom-calculations-that-use-planned-costs"></a>Kalkulace kusovníků využívající plánované náklady

Zásady v rámci nákladové verze (pro plánované náklady) umožňují volitelně nařídit dodržování pěti zásad v kalkulacích kusovníků. Alternativně zásady mohou jen poskytovat výchozí hodnoty. Možnost **Omezení záznamu** v nákladové verzi určuje, zda zásada pro kalkulaci kusovníku týkající se vedlejších nákladů bude nařízena, nebo se bude jednat o výchozí hodnotu. Vedlejší náklady mohou být volitelně zahrnuty do jednotkové ceny. Možnost **Omezení výpočtu** v nákladové verzi určuje, zda budou ostatní čtyři zásady kalkulace kusovníku nařízeny nebo se bude jednat o výchozí hodnoty:

-   Zdroj příspěvku nákladů na zakoupenou položku může znamenat záznamy nákladů v rámci verze výpočtu nákladů. Alternativně může být zdroj definován skupinou výpočtu kusovníku přiřazeného k položce. Skupina výpočtu kusovníků může jako zdroj dat o příspěvcích nákladů definovat uzavřené smlouvy o nákupních cenách.
-   Režim rozpadu může být jednoúrovňový, víceúrovňový, může se jednat o výrobu na zakázku nebo může vycházet z řádkové položky kusovníku. Režim rozpadu pro typ řádku kusovníku kopíruje logiku výpočtu nákladů pro odhady výrobních zakázek.
-   Nastavení zisku může bít nařízeno nebo se může jednat o výchozí hodnotu. Chcete-li použít nastavení zisku a generovat záznamy o prodejních cenách položek, musí nákladová verze umožnit zahrnutí prodejních cen.
-   Princip zálohy může být nařízený nebo se může jednat o výchozí hodnotu. Princip zálohy může být nastaven na **Žádný**, **Aktivní** (u aktivních záznamů nákladů) nebo **Verze výpočtu nákladů** (pro konkrétní verzi výpočtu nákladů).

Kalkulace kusovníků generuje varovné zprávy a další typy zpráv. Několik zásad výpočtu kusovníku určuje typy zpráv. Přepsání použitelných podmínek výstrah definovaných pro skupinu výpočtů kusovníku, která je přiřazená položkám. Při zahájení výpočtu kusovníku je však možné tyto podmínky výstrah přepsat. Při použití záložního principu je často vhodné, když se zálohy zobrazují jako zpráva s informací. Pokud se pokoušíte aktualizovat vypočtené náklady pro položky s chybějícími záznamy nákladů, je rovněž vhodné, pokud informační zpráva identifikuje položky, které nebyly aktualizovány.

## <a name="bom-calculations-that-use-the-fallback-principle"></a>Výpočty kusovníku s použitím principu zálohy
V následujících situacích jsou uvedeny dva příklady použití záložního principu:

-   **Metoda aktualizací standardních nákladů s použitím dvou verzí** − Nákladová verze může obsahovat přírůstkové změny standardních nákladů (například nevyřízené záznamy nákladů, které reprezentují nové položky nebo změny nákladů). V této situaci lze pomocí záložního principu identifikovat použití aktivních standardních nákladů, které jsou obsaženy v jiných nákladových verzích.
-   **Změny simulace dopadu nákladů pomocí plánovaných nákladů** – nákladová verze pro plánované náklady může obsahovat přírůstkové změny pro účely simulace. Nákladová verze bude obsahovat nevyřízené záznamy nákladů, které reprezentují simulované změny nákladů na položky, nákladové kategorie nebo výpočetní vzorce pro nepřímé náklady. V této situaci lze pomocí záložního principu identifikovat použití aktivních standardních nákladů, které jsou obsaženy v jiných nákladových verzích.

## <a name="bom-calculation-of-a-suggested-sales-price"></a>Výpočet navrhované prodejní ceny v kusovníku
Při použití principu "náklady plus přirážka" vypočtená prodejní cena položky odpovídá nastavení procenta nastavení zisku, které je zadáno pro výpočet kusovníku, a náklady, které jsou přidruženy ke komponentám položky, operacím postupů a režijním nákladům na výrobu použitelné položky. Značky odráží procentuální hodnoty nastavení zisku, které jsou přiřazeny nákladovým skupinám, a nákladové skupiny přiřazené k položkám, nákladovým kategoriím pro operace postupu a výpočetním vzorcům nepřímých nákladů pro výrobní režie. Sady procent nastavení zisku jsou označeny **standardní**, **zisk 1**, **zisk 2**, a **zisk 3**. V rámci sady zisk 1 například nastavení procenta 50 procent lze definovat pro skupinu nákladů, která je přiřazena k zakoupenému materiálu, a 80 % procent nastavení zisku může být definováno pro nákladovou skupinu přiřazenou k nákladové kategorii pro operace postupu. Kontext výpočtu kusovníku určí způsob použití vypočtené prodejní ceny:

-   **Výpočet kusovníku pro položku a zadanou nákladovou verzi** − Při výpočtu kusovníku se v rámci nákladové verze generuje čekající záznam o prodejní ceně. Tento záznam poskytuje výchozí bod pro zobrazení podrobností o výpočtu (například na stránce **Vypočítat náklady na položku**). Záznam o prodejní ceně slouží především jako referenční informace a nepoužívá se jako základ prodejní ceny v prodejních objednávkách.
-   **Výpočet kusovníku podle objednávky** – Varianta stránky **Výpočet kusovník**u se používá v souvislosti s prodejní objednávkou, prodejní nabídkou nebo v souvislosti s řádkem servisní zakázky. Výpočet kusovníku specifický podle objednávky nevygeneruje záznam o nákladech na položku v rámci nákladové verze. Místo toho vygeneruje záznam výpočtu, který se zobrazí na stránce **Výsledky výpočtu kusovníku**. Tento záznam výpočtu poskytuje výchozí bod pro zobrazení podrobností o výpočtu (například na stránce **Vypočítat náklady na položku**). Informace o vybraném záznamu výpočtu lze převést na původní položku řádku. Například lze převést vypočtenou prodejní cenu na řádkovou položku prodejní objednávky.

## <a name="order-specific-bom-calculations"></a>Výpočty kusovníků specifických podle objednávek
Výpočet kusovníku specifický podle objednávky reprezentuje odchylku výpočtu kusovníku pro vyráběnou položku. Výpočet kusovníku specifický podle objednávky je prováděn v kontextu položky řádku servisní zakázky, prodejní objednávky nebo prodejní nabídky. Při výpočtu kusovníku specifického podle objednávky se vygeneruje záznam výpočtu, který se zobrazí na stránce **Výsledky výpočtu kusovníku**. Záznam výpočtu obsahuje vypočtenou váhu, vypočtené náklady založené na aktivních záznamech nákladů a vypočtenou prodejní cenu. Záznam výpočtu, který každý výpočet kusovníku pro položku generuje na stránce **Výsledky výpočtu kusovníku** je jedinečným způsobem identifikován číslem výpočtu. Výsledky záznamu výpočtu mohou být volitelně přeneseny do původní položky řádku. Výpočet kusovníku specifický podle objednávky se liší od výpočtu kusovníku pro vyráběnou položku dvěma způsoby:

-   Výpočet kusovníku specifický podle objednávky nevygeneruje záznam o nákladech na položku v rámci nákladové verze. To znamená, že zásady výpočtu kusovníku nejsou použity pro vytváření záznamů o nákladech na položku ani pro přepsání záznamů o nákladech.
-   Při výpočtu kusovníku specifickém podle objednávky jsou vždy použity aktivní záznamy nákladů pro komponenty, nákladové kategorie a vzorce nepřímého výpočtu nákladů.






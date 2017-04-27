---
title: "Převod zúčtovací měny nebo měny vykazování"
description: 
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: RobinARH
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 78223
ms.assetid: 31c56f9a-9c64-40a2-90e3-1969a760614b
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: b75ac168ac6cc78d021c3e15f7a18722eeabc84c
ms.lasthandoff: 03/31/2017


---

# <a name="convert-accounting-or-reporting-currencies"></a>Převod zúčtovací měny nebo měny vykazování

[!include[banner](../includes/banner.md)]




Společnost, která musí změnit zúčtovací měnu nebo měnu vykazování, má dvě možnosti. První možnost je vytvoření nové společnosti a postup od začátku. Druhou možností je spuštění procesu převodu zúčtovací měny a měny vykazování. Jedná se o velmi časově náročná proces, který změní každou transakci v systému. Před spuštěním procesu je nutné provést některá nastavení.

## <a name="preparing-the-legal-entity-for-currency-conversion"></a>Příprava právnické osoby na převod měny
Před převodem měny právnické osoby musíte vrátit všechna přecenění cizí měny v účtech odběratelů a dodavatelů a uzavřít předchozí fiskální roky. Musíte také připravit databázi na převod a pak provést požadované změny na účtu právnické osoby, u které probíhá převod měny. Po dokončení převodu měny je nutné dokončit některé další kroky. Musíte odsouhlasit rozdíly zaokrouhlení v převedených částkách, přepočítat obchodní statistiky, zapsat do deníku transakce hlavní knihy, omezit přístup k nástroji pro převod a přecenit částky v cizí měně pro účty odběratele a dodavatele.

## <a name="setting-up-accounts-for-automatic-transactions"></a>Nastavení účtů pro automatické transakce
Během procesu převodu měny jsou zisky nebo ztráty nebo rozdíly zaokrouhlení zaúčtovány na účtech, které jsou definovány na stránce **Účty pro automatické transakce**. Před spuštěním procesu převodu je nutné přiřadit hlavní účty k následujícím typům transakcí:

-   Zisk z převodu zúčtovací měny
-   Ztráta z převodu zúčtovací měny
-   Haléřový rozdíl v zúčtovací měně
-   Haléřový rozdíl v měně vykazování
-   Roční uzávěrka

## <a name="posting-rounding-differences-and-sum-recalculations"></a>Zaúčtování rozdílů zaokrouhlení a přepočty součtů
Tyto informace vysvětlují, v jakém případě mohou nastat rozdíly zaokrouhlení:

-   Pokud byly ceny produktů převedeny na 0 (nulu), vytvoří se sestava zobrazující číslo produktu, typ modulu, cenu před převodem a jednotku.
-   Zaokrouhlování rozdílů mezi DPH a hlavní knihou jsou zaúčtovány do hlavního deníku.
-   Částky přecenění cizí měny jsou přepočítány a jsou přepočítány částky transakcí odběratelů a dodavatelů.
-   Záznamy vyrovnání zákazníka a dodavatele jsou vytvořeny pro zaokrouhlení rozdílů pro každou transakci zákazníka a dodavatele.
-   Rozdíly zaokrouhlení pro zákazníka a dodavatele jsou zaúčtovány do hlavního deníku.
-   Částky vyrovnaných nákladů a částek upravených nákladů jsou přepočítány v uzavřených skladových transakcích.
-   Rozdíly zaokrouhlení v řízení zásob jsou zaúčtovány do hlavního deníku.
-   Množství na skladě je přepočítáno.
-   Celkové částky v denících hlavní knihy jsou přepočítávány.
-   Tabulky s uzávěrkami jsou přepočítány.
-   Účetní zůstatky jsou přepočítány.
-   Rozdíly zaokrouhlení v hlavní knize jsou zaúčtovány do hlavního deníku.
-   Otevírané transakce hlavní knihy jsou přepočítány.
-   Konečná částka zůstatků hlavní knihy je vypočtena.

Pokud převádíte na novou zúčtovací měnu hlavní knihy a dojde k chybě během přepočítání celkových částek nebo zaúčtování rozdílů zaokrouhlení, je nutné zavřít stránku **Převod zúčtovací měny hlavní knihy**. Celkové částky se potom přepočítají a budou zaúčtovány rozdíly zaokrouhlení.

## <a name="processing-the-currency-conversion"></a>Zpracování převodu měny
Při zahájení procesu převodu měny musí být ze systému odhlášeni všichni uživatelé. Je nutné definovat novou hlavní knihu nebo měnu vykazování a směnné kurzy. Po kliknutí na tlačítko **OK** se proces spustí a aktualizuje se každá transakce v systému. Převod měny je velmi dlouhý proces. Po dokončení se na stránce **Hlavní kniha** zobrazí aktualizovaná zúčtovací měna nebo měna vykazování.

## <a name="completing-the-currency-conversion"></a>Dokončení převodu měny
Po převodu měny musíte znovu vygenerovat všechny sestavy odsouhlasení, a tím ověřit, že všechny převedené částky jsou správné.

-   Pokud převod zúčtovací měny hlavní knihy způsobí rozdíly zaokrouhlení, nezaúčtují se tyto rozdíly pomocí dokladu, kde došlo k rozdílům zaokrouhlení. Místo toho jsou rozdíly zaúčtovány pomocí dokladu, který byl zadán pro zaúčtování převodu. Po převodu budou všechny výkazy, které provádí kontrolu na základě dokladu a data, zahrnovat tyto rozdíly zaokrouhlení. To chování je správné a můžete je ignorovat.
-   Pokud výkazy odsouhlasení pro odběratele a dodavatele zobrazí částku rozdílu na řádku celkem a před převodem neexistoval žádný rozdíl, je nezbytné částku rozdílu zaúčtovat. Jedná se o součtový účet pro odběratele a dodavatele. Protiúčet je účtem hlavní knihy pro převodní ztrátu nebo převodní zisk.

Když jsou smazány veškeré deníky transakce hlavní knihy, můžete provést zápisy do deníku transakcí hlavní knihy. Klikněte na položku **Hlavní kniha** &gt; **Periodicky** &gt; **Deníky** &gt; **Zapisování do deníku**. Po převodu měny lze přecenit částky v cizí měně, pokud je přecenění vyžadováno. Přecenění částek v cizí měně lze provést výběrem položky **Standardní** v poli **Metoda** pro přecenění.





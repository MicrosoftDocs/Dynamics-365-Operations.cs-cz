---
title: Nákladové formuláře
description: Nastavení nákladového formuláře má dva cíle. Prvním je definovat formát zobrazení informací o nákladech na prodané zboží, které se týkají vyrobených položek nebo výrobní zakázky. Vytvořený formát zobrazení je pojmenován nákladový formulář. Druhým je definovat základnu pro výpočet nepřímých nákladů. Nastavení nákladového formuláře je založeno na funkcích nákladové skupiny pro zobrazení informací a vzorců pro výpočet nepřímých nákladů. V tomto článku jsou popsány dva cíle nastavení nákladového formuláře.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostSheetDesigner, CostSheetCalculationFactor
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53201
ms.assetid: e7d72b43-3892-49ae-8821-9eede3f4d24a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d1453357649c2617c5daaa1a38af772ae5eeea80adf9f0ab8316e9f46f1a78fb
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6721408"
---
# <a name="costing-sheets"></a>Nákladové formuláře

[!include [banner](../includes/banner.md)]

Nastavení nákladového formuláře má dva cíle. Prvním je definovat formát zobrazení informací o nákladech na prodané zboží, které se týkají vyrobených položek nebo výrobní zakázky. Vytvořený formát zobrazení je pojmenován nákladový formulář. Druhým je definovat základnu pro výpočet nepřímých nákladů. Nastavení nákladového formuláře je založeno na funkcích nákladové skupiny pro zobrazení informací a vzorců pro výpočet nepřímých nákladů. V tomto článku jsou popsány dva cíle nastavení nákladového formuláře. 

Nákladový formulář představuje způsob formátovaného zobrazení informací o nákladech na prodané zboží pro vyrobenou položku nebo výrobní zakázku. Při nastavení nákladového formuláře definujete formát informací a také základ pro výpočet nepřímých nákladů. Nastavení nákladového formuláře je založeno na funkcích nákladové skupiny pro zobrazení informací a vzorců použitých pro výpočet nepřímých nákladů. Zde jsou další informace o dvou cílech nastavení nákladového formuláře:
-   **Definujte formát nákladového formuláře.** Uživatelem definovaný formát nákladového formuláře identifikují segmentaci nákladů, které zahrnují náklady na prodané zboží pro vyráběnou položku. Například informace o nákladech prodaného zboží položky mohou být rozděleny na materiál, práci a režii na základě skupin nákladů. Tyto nákladových skupiny jsou přiřazeny položkám, nákladovým kategoriím pro operace postupu a vzorcům pro výpočet nepřímých nákladů. Formát nákladového formuláře obvykle vyžaduje průběžné součty, pokud bylo definováno více nákladových skupin. Například lze agregovat více nákladových skupin, které se vztahují k materiálu. I když definice formátu nákladového formuláře není povinná, musí být tento formát definován, pokud se budou počítat nepřímé náklady.
-   **Definovat základnu pro výpočet nepřímých nákladů.** Nepřímé náklady odrážejí výrobní režii spojenou se zhotovením výrobku. Vzorec pro výpočet nepřímých nákladů lze vyjádřit jako přirážku nebo jako sazbu. Přirážka představuje procento hodnoty a sazba představuje hodinovou částku pro operaci technologického postupu. Nákladová skupina definuje základnu vzorce pro výpočet, jako je 100% přirážka pro mzdovou nákladovou skupinu nebo hodinovou sazbu ve výši 50,00 USD pro strojovou nákladovou skupinu. Chcete-li definovat vzorec pro výpočet a základ nákladové skupiny, je nutné při nastavení nákladového formuláře určit nákladovou skupinu, která představuje režii, a vybrat, zda se použije přirážka nebo sazba.

Každý vzorec pro výpočet musí být zadán jako záznam o nákladech. Záznam o nákladech je složen z určité nákladové verze, procenta přirážky nebo výše sazby, základu nákladové skupiny, stavu a data platnosti. Při prvním zadání záznamu o nákladech má záznam stav **Čeká na zpracování** a datum platnosti. Pokud záznam nákladů aktivujete, stav se aktualizuje tak, že záznam bude aktuálním aktivním záznamem a datum platnosti se aktualizuje na datum aktivace. Záznam nákladů může také uvádět pracoviště pro výpočetní vzorec specifický pro určitá pracoviště. Případně můžete ponechat pole **Pracoviště** prázdné, což bude značit, že výpočetní vzorec je vzorcem pro celý podnik. Záznam o nákladech se může volitelně skládat ze zadané položky nebo skupiny položek, pokud byl vzorec výpočtu označen jako vzorec pro položku. 

Aktuálně aktivní záznamy nákladů pro vzorce výpočtu nepřímých nákladů jsou použity k odhadu nákladů na výrobní zakázku. Rovněž se používají pro výpočet skutečných nákladů, které souvisejí se skutečnou spotřebou času a materiálu. Záznamy očekávaných nákladů jsou použity ve výpočtech kusovníku k budoucímu datu. 

Pro nákladové verze existují dvě zásady blokování, které určují, zda může probíhat údržba čekajících nákladů a zda čekající náklady mohou být aktivovány. Zásady blokování použijte k povolení údržby dat a potom k zakázání údržby dat o nákladech v nákladové verzi. 

Po definování formátu nákladového formuláře a výpočtu nepřímých nákladů je nutné provést samostatný krok, ve kterém informace ověříte a uložíte. Nákladový formulář představuje celopodnikový formát pro konzistentní zobrazení informací o nákladech na prodané zboží. 

Nákladový formulář je zobrazen jako součást stránky **Vypočítat náklady na zboží**. Nákladový formulář lze zobrazit pro záznam o vypočtených nákladech na vyrobenou položku na stránce **Cena položky** nebo pro záznam o výpočtu pro určitou zakázku na stránce **Výsledky výpočtu kusovníku**. Lze jej také zobrazit jako součást stránky **Kalkulace ceny** pro výrobní zakázku.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
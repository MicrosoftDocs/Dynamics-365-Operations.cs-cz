---
title: Možnosti mřížky
description: Toto téma popisuje několik výkonných funkcí ovládacího prvku mřížky. Chcete-li mít přístup k těmto funkcím, je nutné povolit novou funkci mřížky.
author: jasongre
manager: AnnBe
ms.date: 02/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: DefaultDashboard
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 7136edba828bf97b6e0c8d2a698b884640d680e5
ms.sourcegitcommit: 880f617d1d6e95eccbed762c7ea04398553c2ec0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/11/2020
ms.locfileid: "3036258"
---
# <a name="grid-capabilities"></a>Možnosti mřížky

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Nový ovládací prvek mřížky poskytuje řadu užitečných a výkonných funkcí, které lze použít k vylepšení produktivity uživatelů, vytvoření zajímavějších zobrazení dat a získání smysluplných přehledů dat. Tento článek se týká následujících možností: 

-  Výpočet součtů
-  Seskupování dat
-  Zadávání před systémem
-  Vyhodnocování matematických výrazů 

## <a name="calculating-totals"></a>Výpočet součtů
V aplikacích Finance and Operations mají uživatelé možnost zobrazit součty v dolní části číselných sloupců v mřížkách. Tyto součty se zobrazí v části zápatí v dolní části mřížky. 

### <a name="showing-the-grid-footer"></a>Zobrazení zápatí mřížky
Aplikace Finance and Operations obsahují oblast zápatí v dolní části každé tabulkové mřížky. V zápatí je možné zobrazit cenné informace související s daty, která se zobrazí v mřížce. Následuje několik příkladů těchto informací:

- Počet vybraných řádků v tabulce (při výběru více než jednoho záznamu)
- Celkové součty v dolní části konfigurovaných číselných sloupců
- Počet řádků v sadě dat 

Toto zápatí je ve výchozím nastavení skryto, ale lze je snadno zapnout. Chcete-li zobrazit zápatí pro mřížku, klikněte pravým tlačítkem na záhlaví sloupce v mřížce a vyberte možnost **Zobrazit zápatí**. Po zapnutí zápatí pro určitou mřížku bude toto nastavení zapamatováno, dokud uživatel neskryje zápatí, což lze provést kliknutím pravým tlačítkem na záhlaví sloupce a výběrem možnosti **Skrýt zápatí**.  Pamatujte, že akce **Zobrazit zápatí / Skrýt zápatí** bude v budoucí aktualizaci přemístěna. 

### <a name="specifying-columns-with-totals"></a>Určení sloupců se součty
V současné době nebudou ve výchozím nastavení nakonfigurovány žádné sloupce pro zobrazení součtů. Namísto toho je tato činnost považována za jednorázovou, podobně jako nastavení šířky sloupců v mřížce. Jakmile určíte, že chcete zobrazit součty pro sloupec, toto nastavení se při další návštěvě stránky zapamatuje.  

Existují dva způsoby konfigurace sloupce pro zobrazení celkového součtu: 

- Pravým tlačítkem klikněte na sloupec, pro který chcete zjistit celkovou hodnotu, a vyberte **Sečíst tento sloupec**. Tato akce způsobí provedení tří událostí:

    1. Zápatí se zobrazí. 
    2. Bude uložena vaše preference pro zobrazení součtu v tomto sloupci. 
    3. Tato akce zahájí výpočet součtu pro tento sloupec a všechny dříve konfigurované, pro zobrazení celkových hodnot. Čas potřebný k zobrazení celkového součtu závisí na velikosti sady dat, kterou vytváříte.

- Poté, co je zápatí viditelné, vyberte **Zobrazit součet** v oblasti zápatí v dolní části sloupce, pro který chcete zobrazit součet. Pokud neexistují žádné konfigurované sloupce, tlačítko **Zobrazit součet** bude k dispozici pro všechny číselné sloupce. 

    Je-li pro součty nakonfigurován alespoň jeden sloupec, budou tlačítka **Zobrazit součet** k dispozici pouze při přechodu nebo výběru. Akce vybírání **Zobrazit součet** pouze ukládá vaši předvolbu pro zobrazení součtu v tomto sloupci, takže přednost bude uplatněna během příštích návštěv na stránce. V zápatí je tento stav označen pomlčkou, která se zobrazí ve sloupci. (Případně, je-li sada dat dostatečně malá, součet se zobrazí okamžitě.)

Pokud uděláte chybu a již nechcete zobrazovat celkový součet v určitém sloupci, klikněte pravým tlačítkem na sloupec a vyberte možnost **Skrýt součet**, nebo v zápatí daného sloupce zvolte tlačítko **Skrýt součet**. Tato preference bude také uložena pro budoucí návštěvy na stránce. 

### <a name="calculating-totals"></a>Výpočet součtů
Když přejdete na stránku se zobrazeným zápatím a sloupci, které jsou již pro součty nakonfigurovány, mohou být součty zobrazeny v zápatí nebo nikoliv. Chování je závislé na velikosti datové sady na stránce. Pokud je datová sada dostatečně malá, součty se zobrazí automaticky spolu s počtem řádků v sadě dat. Pokud v zápatí existují pomlčky pod sloupci, které jste nakonfigurovali pro součty, je sada dat příliš velká, aby systém mohl zobrazit součty okamžitě, a k výpočtu součtů je nutné provést explicitní akci. Tu provedete kliknutím na tlačítko **Vypočítat** v zápatí, nebo klikněte pravým tlačítkem na sloupec, pro který chcete vytvořit součet a vyberte možnost **Sečíst tento sloupec**.  

Pokud výpočet trvá příliš dlouho, můžete operaci zrušit kliknutím na tlačítko **Zrušit**. Někdy je však datová sada příliš velká pro výpočet součtů (limit stanovený vaší organizací) a místo toho budete upozorněni na filtrování dat.

Součty se aktualizují automaticky při aktualizaci, odstranění nebo vytvoření řádků v sadě dat.  

## <a name="grouping-data"></a>Seskupování dat
Obchodní uživatelé často potřebují provádět ad hoc analýzu dat. I když to lze provést exportem dat do aplikace Microsoft Excel a použitím kontingenčních tabulek, možnost **Seskupení** v tabulkových mřížkách umožňuje uživatelům organizovat svá data v rámci aplikací Finance and Operations. Protože tato funkce rozšiřuje funkci **součtů**, **seskupení** také umožňuje získat smysluplné přehledy o datech poskytnutím mezisoučtů na úrovni skupiny.

Chcete-li použít tuto funkci, klikněte pravým tlačítkem na sloupec, který chcete seskupit a zvolte **Seskupit tento sloupec**. Tato akce seřadí data podle vybraného sloupce, přidá nový sloupec Seskupit podle na začátek mřížky a vloží "řádky záhlaví" na začátek každé skupiny. Tyto řádky záhlaví obsahují následující informace o každé skupině: 
-  Hodnota dat pro skupinu 
-  Popisek sloupce (tyto informace budou obzvlášť užitečné po podporování více úrovní seskupení.)
-  Počet datových řádků v této skupině
-  Mezisoučty pro všechny sloupce konfigurované pro zobrazení součtů

Pokud jsou povolena [uložená zobrazení](saved-views.md), lze toto seskupení uložit přizpůsobením jako součást zobrazení pro rychlý přístup při další návštěvě stránky.  

Pokud vyberete možnost **Seskupit podle tohoto sloupce** v jiném sloupci, bude nahrazeno původní seskupení, protože v aktualizaci 10.0.9 s Platform Update 33 je podporována pouze úroveň seskupení.

Chcete-li zrušit seskupení v mřížce, klikněte pravým tlačítkem na sloupec seskupení a vyberte možnost **Zrušit seskupení**.  


## <a name="evaluating-math-expressions"></a>Vyhodnocování matematických výrazů
Jedná se o prostředek pro zvýšení produktivity, uživatelé mohou zadávat matematické vzorce do číselných buněk v mřížce. Není nutné provádět výpočet v aplikaci mimo systém. Zadáte-li například hodnotu **=15\*4** a poté se stisknutím klávesy **Tab** přesunete mimo pole, systém vyhodnotí výraz a do pole zapíše hodnotu **60**.

Chcete-li, aby systém rozpoznal hodnotu jako výraz, zahajte tuto hodnotu znaménkem rovná se (**=**). Další informace o podporovaných operátorech a syntaxi naleznete v tématu [Podporované matematické symboly](http://bugwheels94.github.io/math-expression-evaluator/#supported-maths-symbols).  

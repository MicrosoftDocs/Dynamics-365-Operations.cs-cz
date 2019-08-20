---
title: Typy majetku
description: Toto téma vysvětluje, jak vytvořit typy majetku v modulu Správa majetku. Popisuje také prvky, které souvisejí s typy majetku.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 288dac77f9d999012ec930ef2bca5c0921c2955f
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783130"
---
# <a name="asset-types"></a>Typy majetku

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Toto téma vysvětluje postup při vytváření typů majetku. Popisuje také prvky, které souvisejí s typy majetku. Typy majetku se používají jako obecné kategorie majetku. Jedná se například o CNC stroje, měřicí zařízení a nákladní motory. Typy majetku se používají ke správě typů úloh (úkolů údržby), stavů životního cyklu majetku, měr majetku, atributů majetku, šablon vyhodnocení podmínek a modelů majetku, které lze vybrat pro majetek. Při vytváření majetku je nutné zadat jeho typ.

Pro každý typ majetku lze vytvořit varianty nastavení typu majetku. Máte-li například typ majetku s názvem **Nákladní automobily**, můžete vytvořit varianty tohoto typu majetku pro různé výrobce a modely majetku. Ke každému nastavení typu majetku můžete přidat požadované náhradní díly a plány údržby.

Nejdříve nastavte požadované typy majetku. Dále vytvoříte modely majetku, které by měly souviset s typy majetku. Nakonec na stránce **Výchozí typy majetku** vytvoříte všechny varianty typů majetku, které jsou požadovány pro vaše zařízení.

## <a name="create-an-asset-type"></a>Vytvořit typ majetku

1. Vyberte **Správa majetku**\>**Nastavení**\> **Typy majetku** \>**Typy majetku**.
2. Vyberte **Nový**, chcete-li vytvořit typ majetku.
3. V poli **Typ majetku** zadejte ID typu majetku.
4. Do pole **Název** zadejte název.
5. V poli **Model životního cyklu majetku** vyberte model životního cyklu majetku. Další informace o stavech životního cyklu majetku a modelech životního cyklu majetku naleznete v tématu [Stavy životního cyklu majetku](object-stages.md).
6. Nastavte možnost **Celkem** na **Ano**, pokud mají být pro majetek, který má tento typ majetku, vypočítány souhrnné hodnoty klíčového ukazatele výkonu (KPI).
7. Zvolte **Uložit**.
8. Na pevné záložce **Typy úloh** vyberte typy úloh, které mají souviset s typem majetku:

    - Chcete-li vybrat typ úlohy, vyberte jej v poli **Zbývající typy úloh** a potom výběrem tlačítka šipky vpravo ![Tlačítko šipka vpravo](media/29-setup-for-objects.png) jej přesuňte do části **Vybrané typy úloh**.
    - Chcete-li vybrat všechny dostupné typy úloh, vyberte tlačítko ![Šipka přesunout vše](media/30-setup-for-objects.png). Všechny typy úloh jsou přeneseny z pole **Zbývající typy úloh** do pole **Vybrané typy úloh**.
    - Chcete-li zrušit výběr typu úlohy, vyberte jej v poli **Vybrané typy úloh** a potom výběrem tlačítka šipky vlevo ![Tlačítko šipka vlevo](media/31-setup-for-objects.png) jej přesuňte do pole **Zbývající typy úloh**.

9. Také můžete vybrat měření majetku, které by mělo souviset s typem majetku. Na pevné záložce **Měření majetku** proveďte své výběry pomocí metod popsaných pro typy úloh v kroku 8. Další informace o nastavení měření majetku naleznete v tématu [Měření objektu údržby](counters.md)
10. Také můžete vybrat typy atributů, které by měly souviset s typem majetku. Na pevné záložce **Typy atributů** proveďte své výběry pomocí metod popsaných pro typy úloh v kroku 8. Chcete-li potom vytvořit upřednostňovanou posloupnost typů atributů, vyberte typ atributu v poli **Vybrané typy atributů** a pomocí tlačítek se šipkami nahoru a dolů jej přesuňte. Posloupnost typů atributů bude zobrazena u majetku, který používá tento typ majetku. Další informace o atributech majetku naleznete v části [Typy atributů údržby](../setup-for-functional-locations/specification-types.md).

    > [!NOTE]
    > Při přidání nových typů atributů na pevné záložce **Typy atributů** je existující majetek automaticky aktualizován těmito informacemi.

11. Také můžete vybrat šablony hodnocení podmínek, které by měly souviset s typem majetku. Na pevné záložce **Hodnocení podmínek** proveďte své výběry pomocí metod popsaných pro typy úloh v kroku 8. Další informace o šablonách hodnocení podmínek a registracích naleznete v tématu [Hodnocení podmínek](../setup-for-objects/condition-assessment.md).
12. Pevná záložka **Model majetku** zobrazuje všechny kombinace výrobců a modelů majetku nastavených pro vybraný typ majetku. Chcete-li zobrazit kombinace rozdělené podle výrobce, vyberte **Model majetku** pro otevření stránky **Model majetku**.

    Na stránce **Model majetku** můžete přidat vztahy model majetku – typ majetku. Dále na stránce **Typy majetku** můžete přidat vztahy výrobce majetku – model majetku přímo k typu majetku. Nakonec na stránce **Model majetku** (**Správa majetku** \> **Nastavení** \> **Majetek** \> **Model majetku**), můžete vytvořit nové vztahy výrobce majetku – model majetku – typ majetku. Existují tedy tři způsoby nastavení a úpravy vztahů výrobce majetku – model majetku – typ majetku. Všechny dostupné kombinace jsou zobrazeny z různých perspektiv a při práci s nastavením můžete vybrat preferovaný vstupní bod.

> [!NOTE]
> - Pokud vyberete pro typ majetku měření majetku, výběry se automaticky aktualizují na stránce **Měření majetku** (**Správa majetku** \> **Nastavení** \> **Majetek** \> **Typy majetku** \> **Měření majetku**).
> - Pole v části **Podrobnosti** na pevné záložce **Obecné** zobrazují počet typů úloh, měření majetku, atributů atd., které jsou nastaveny u vybraného typu majetku.

Ručně vytvořené pracovní příkazy jsou obvykle spojeny s opravnou údržbou, zatímco automaticky vytvořené pracovní příkazy souvisejí s preventivní údržbou. Při ručním vytváření pracovních příkazů lze použít pouze typy úloh, které jsou vybrány na záložce **Typy úloh** na stránce **Typy majetku**. Automaticky vytvořené pracovní příkazy však mohou používat všechny typy úloh, které vytvoříte na stránce **Typy úloh** (**Správa majetku** \> **Nastavení** \> **Úlohy** \> **Typy úloh**).

## <a name="create-asset-type-setup-lines"></a>Vytvoření řádků nastavení typu majetku

1. Vyberte **Správa majetku** \> **Nastavení** \> **Majetek** \> **Typy majetku** \> **Nastavení typu majetku**. Alternativně vyberte položku **Správa majetku** \> **Nastavení** \> **Majetek** \> **Typy majetku** \> **Typy majetku**, vyberte typ majetku a pak vyberte **Nastavení typu majetku**.
2. Při prvním použití stránky **Nastavení typu majetku** se vám může hodit tlačítko **Vytvořit kombinace**. Toto tlačítko můžete použít k rychlému vytvoření všech kombinací modelu majetku na typu majetku. Vyberte **Vytvořit kombinace**, vyberte typ majetku, pro který chcete vytvořit kombinace, a pak vyberte **OK**.

    > [!NOTE]
    > Pokud nebudete používat všechny kombinace nastavení typu majetku, které byly automaticky vytvořeny, můžete nastavení odstranit tak, že je vyberete a pak vyberete příkaz **Odstranit**.

3. Vyberte **Nový**, chcete-li ručně vytvořit nastavení typu majetku.
4. V závislosti na konkrétním nastavení typu majetku proveďte výběr v polích **Typ majetku**, **Výrobce** a **Model**.
5. Pokud se záruční smlouva vztahuje k typu majetku, vyberte smlouvu v polích **Záruka dodavatele** a **Záruka zákazníka** . 
6. Na pevné záložce **Náhradní díly** vyberte **Přidat** pro přidání náhradních dílů do nastavení vybraného typu majetku.
7. Chcete-li schválit náhradní díl, vyberte řádek náhradního dílu a pak vyberte možnost **Schválit**. Můžete vybrat více řádků ke schválení.
8. Chcete-li zjistit, zda se náhradní část používá někde jinde v modulu Správa majetku (například ve vztahu k majetku a pracovním příkazům), vyberte řádek náhradní části a pak vyberte **Položka, kde se používá** k otevření stránky **Položka, kde se používá**. Chcete-li zobrazit všechny aktivní náhradní díly v seznamu, zaškrtněte políčko **Aktivní**. Chcete-li zobrazit pouze schválené náhradní díly, zaškrtněte políčko **Schválené**.
9. Na pevné záložce **Plány údržby** vyberte **Přidat** pro přidání plánů údržby do nastavení vybraného typu majetku.
10. Chcete-li zkopírovat nastavení typu majetku do jiného nastavení, můžete použít funkci Kopírovat. Vyberte nastavení typu majetku pro zkopírování nastavení, vyberte **Kopírovat nastavení** a vyberte nastavení typu majetku, ze kterého chcete nastavení zkopírovat. Nastavení různých možností určuje, jaké množství informací bude zahrnuto. Po dokončení vyberte **OK** pro zkopírování nastavení.

> [!NOTE]
> Pokud máte mnoho řádků s náhradními díly a řádků plánu údržby, které budete používat znovu, umožňuje funkce Kopírovat rychle a snadno nastavit údaje pro mnoho kombinací nastavení typu majetku.

## <a name="spare-parts-on-the-asset-type-setup"></a>Náhradní díly v nastavení typu majetku

Jak bylo popsáno v části „Vytvoření řádků nastavení typu majetku“, jsou náhradní díly nastaveny v modelech majetku na stránce **Nastavení typu majetku**. Proto když otevřete stránku **Nastavení typu majetku**, zobrazí se pouze náhradní díly, které souvisejí s vybranou kombinací typu majetku, výrobce majetku a modelu majetku. Chcete-li zobrazit seznam všech záznamů náhradních dílů, otevřete stránku **Náhradní díly** (**Správa majetku** \> **Dotazy** \> **Náhradní díly**).

Na stránce **Náhradní díly** můžete také vytvořit nové náhradní díly pro existující kombinace typu majetku, výrobce majetku a modelu majetku. Můžete se rozhodnout, zda chcete vytvořit záznamy náhradních dílů na stránce **Nastavení typu majetku** nebo na stránce **Náhradní díly**. Stránka **Nastavení typu majetku** poskytuje přehled dat o zvolené kombinaci typu majetku, výrobce majetku a modelu majetku, zatímco stránka **Náhradní díly** poskytuje úplný přehled o všech řádcích nastavení typu majetku. Pokud stránka **Náhradní díly** obsahuje mnoho záznamů, může vám stránka **Nastavení typu majetku** poskytnout lepší přehled.

Chcete-li zjistit, zda se náhradní díl na vybraném řádku používá někde jinde v modulu Správa majetku (například ve vztahu k majetku a pracovním příkazům), vyberte řádek náhradní části a pak vyberte **Položka, kde se používá** k otevření stránky **Položka, kde se používá**. 


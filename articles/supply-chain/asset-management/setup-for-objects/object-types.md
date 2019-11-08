---
title: Typy majetku
description: Toto téma vysvětluje, jak vytvořit typy majetku v modulu Správa majetku. Popisuje také prvky, které souvisejí s typy majetku.
author: josaw1
manager: AnnBe
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a19b8c40dd7d48b2d78723c4411f1699819c4026
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626078"
---
# <a name="asset-types"></a>Typy majetku

[!include [banner](../../includes/banner.md)]



Toto téma vysvětluje postup při vytváření typů majetku. Popisuje také prvky, které souvisejí s typy majetku. Typy majetku se používají jako obecné kategorie majetku. Jedná se například o CNC stroje, měřicí zařízení a nákladní motory. Typy majetku se používají ke správě typů úloh údržby (úkolů údržby), stavů životního cyklu majetku, čítačů, atributů majetku, šablon vyhodnocení podmínek a modelů majetku, které lze vybrat pro majetek. Při vytváření majetku je nutné zadat jeho typ.

Pro každý typ majetku lze vytvořit varianty nastavení typu majetku. Máte-li například typ majetku s názvem **Nákladní automobily**, můžete vytvořit varianty tohoto typu majetku pro různé výrobce a modely majetku. Ke každému nastavení typu majetku můžete přidat požadované náhradní díly a plány údržby.

Nejdříve nastavte požadované typy majetku. Dále vytvoříte modely majetku, které by měly souviset s typy majetku. Nakonec na stránce **Výchozí typy majetku** vytvoříte všechny varianty typů majetku, které jsou požadovány pro vaše zařízení.

## <a name="create-an-asset-type"></a>Vytvořit typ majetku

1. Vyberte **Správa majetku** > **Nastavení** > **Typy majetku** > **Typy majetku**.
2. Vyberte **Nový**, chcete-li vytvořit typ majetku.
3. V poli **Typ majetku** zadejte ID typu majetku.
4. Do pole **Název** zadejte název.
5. V poli **Model životního cyklu majetku** vyberte model životního cyklu majetku. Další informace o stavech životního cyklu majetku a modelech životního cyklu majetku naleznete v tématu [Stavy životního cyklu majetku](object-stages.md).
6. Nastavte možnost **Celkem** na **Ano**, pokud mají být pro majetek, který má tento typ majetku, vypočítány souhrnné hodnoty klíčového ukazatele výkonu (KPI).
7. Zvolte **Uložit**.
8. Na pevné záložce **Typy práce údržby** vyberte typy práce údržby, které mají souviset s typem majetku:

    - Chcete-li vybrat typ práce údržby, vyberte jej v poli **Zbývající typy práce údržby** a potom výběrem tlačítka se šipkou vpravo ![Tlačítko se šipkou vpravo](media/29-setup-for-objects.png) jej přesuňte do části **Vybrané typy práce údržby**.
    - Chcete-li vybrat všechny dostupné typy práce údržby, vyberte tlačítko ![Šipka přesunout vše](media/30-setup-for-objects.png). Všechny typy práce údržby jsou přeneseny z pole **Zbývající typy práce údržby** do pole **Vybrané typy práce údržby**.
    - Chcete-li zrušit výběr typu práce údržby, vyberte jej v poli **Vybrané typy práce údržby** a potom výběrem tlačítka šipky vlevo ![Tlačítko šipka vlevo](media/31-setup-for-objects.png) jej přesuňte do pole **Zbývající typy práce údržby**.

9. Také můžete vybrat čítače, které by měly souviset s typem majetku. Na pevné záložce **Čítače** proveďte své výběry pomocí metod popsaných pro typy práce údržby v kroku 8. Další informace o nastavení čítačů naleznete v tématu [Čítače](counters.md).
10. Také můžete vybrat typy atributů, které by měly souviset s typem majetku. Na pevné záložce **Typy atributů** proveďte své výběry pomocí metod popsaných pro typy práce údržby v kroku 8. Chcete-li potom vytvořit upřednostňovanou posloupnost typů atributů, vyberte typ atributu v poli **Vybrané typy atributů** a pomocí tlačítek se šipkami nahoru a dolů jej přesuňte. Posloupnost typů atributů bude zobrazena u majetku, který používá tento typ majetku. Další informace o atributech majetku naleznete v části [Typy atributů údržby](../setup-for-functional-locations/specification-types.md).

    > [!NOTE]
    > Při přidání nových typů atributů na pevné záložce **Typy atributů** je existující majetek automaticky aktualizován těmito informacemi.

11. Také můžete vybrat šablony hodnocení podmínek, které by měly souviset s typem majetku. Na pevné záložce **Hodnocení podmínek** proveďte své výběry pomocí metod popsaných pro typy práce údržby v kroku 8. Další informace o šablonách hodnocení podmínek a registracích naleznete v tématu [Hodnocení podmínek](../setup-for-objects/condition-assessment.md).
12. Pevná záložka **Model majetku** zobrazuje všechny kombinace výrobců a modelů majetku nastavených pro vybraný typ majetku. Chcete-li zobrazit kombinace rozdělené podle výrobce, vyberte **Model majetku** pro otevření stránky **Model majetku**.

    Na stránce **Model majetku** můžete přidat vztahy model majetku – typ majetku. Dále na stránce **Typy majetku** můžete přidat vztahy výrobce majetku – model majetku přímo k typu majetku. Nakonec na stránce **Model majetku** (**Správa majetku** \> **Nastavení** \> **Majetek** \> **Model majetku**), můžete vytvořit nové vztahy výrobce majetku – model majetku – typ majetku. Existují tedy tři způsoby nastavení a úpravy vztahů výrobce majetku – model majetku – typ majetku. Všechny dostupné kombinace jsou zobrazeny z různých perspektiv a při práci s nastavením můžete vybrat preferovaný vstupní bod.

> [!NOTE]
> - Pokud v typu majetku vyberete čítače, výběry se automaticky aktualizují na stránce **Čítače** (**Správa majetku** > **Nastavení** > **Majetek** > **Typy majetku** > **Čítače**).
> - Pole v části **Podrobnosti** na pevné záložce **Obecné** zobrazují počet typů úloh údržby, čítačů, atributů atd., které jsou nastaveny u vybraného typu majetku.

Ručně vytvořené pracovní příkazy jsou obvykle spojeny s opravnou údržbou, zatímco automaticky vytvořené pracovní příkazy souvisejí s preventivní údržbou. Při ručním vytváření pracovních příkazů lze použít pouze typy práce údržby, které jsou vybrány na pevné záložce **Typy práce údržby** na stránce **Typy majetku**. Automaticky vytvořené pracovní příkazy však mohou používat všechny typy práce údržby, které vytvoříte na stránce **Typy práce údržby** (**Správa majetku** \> **Nastavení** \> **Úlohy** \> **Typy práce údržby**).

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


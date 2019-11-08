---
title: Prognózy údržby
description: Toto téma popisuje prognózy údržby v modulu Správa majetku.
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
ms.openlocfilehash: a1596b283c3eaffca25ff7f03c722a2bcce109fb
ms.sourcegitcommit: deb87e518a151d8bb084891851a39758938a96e4
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/15/2019
ms.locfileid: "2626286"
---
# <a name="maintenance-forecasts"></a>Prognózy údržby

[!include [banner](../../includes/banner.md)]



Při vytváření pracovního příkazu vytváříte úlohy pracovních příkazů se souvisejícími položkami majetku a typy práce údržby. Pokud vyberete typ práce údržby obsahující prognózy údržby, budou prognózy automaticky zkopírovány do tohoto pracovního příkazu.

Měli byste být schopni přidat řádky prognózy do pracovního příkazu nebo je z něho odstranit. Nastavení stavu životního cyklu pracovního příkazu, související typ projektu a pravidla fáze související s typem projektu určují, zda lze přidávat nebo upravovat řádky prognózy. Další informace o stavech životního cyklu pracovního příkazu a souvisejících fázích projektu naleznete v tématu [Prognózy, pracovní příkazy a projekty](../integration-to-project-management-and-accounting/forecasts-work-orders-and-projects.md).

1. Vyberte **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. Vyberte pracovní příkaz v seznamu a pak v podokně akcí na kartě **Pracovní příkaz** ve skupině **Projekt** vyberte **Prognóza**. Stránka **Prognóza údržby pracovního příkazu** ukazuje řádky prognózy z typu práce údržby vybrané v pracovním příkazu.


## <a name="add-an-hours-forecast-to-a-work-order"></a>Přidání prognózy hodin do pracovního příkazu

1. Na stránce **Prognóza údržby pracovního příkazu** vyberte úlohu pracovního příkazu, do které chcete přidat prognózu.

2. Na záložce s náhledem **Hodiny** výběrem tlačítka **Přidat** vytvořte nový řádek.

3. V poli **Kategorie** vyberte kategorii.

4. Do pole **Hodiny** zadejte počet prognózovaných hodin.

5. V poli **Vlastnost řádku** vyberte typ poplatku, který má být na řádku použit.


## <a name="add-an-items-forecast-to-a-work-order"></a>Přidání prognózy položek do pracovního příkazu

Existují tři způsoby přidání položek do prognózy údržby pracovních příkazů. Existují tři způsoby přidání položek do prognózy údržby pracovního příkazu: můžete vytvořit řádky pro položky (náhradní díly) nebo kusovníky (BOM) majetku, které nejsou zahrnuty do seznamu náhradních dílů nebo kusovníku majetku, můžete vybrat náhradní díly ze seznamu schválených náhradních dílů a vybrat položky z kusovníku majetku.

- Na stránce **Prognóza údržby pracovního příkazu** vyberte úlohu pracovního příkazu, do které chcete přidat prognózu.

- Na pevné záložce **Položky** přidejte do prognózy údržby položky pomocí odpovídající metody.

Chcete-li vytvořit nový řádek pro náhradní díl, který není v seznamu náhradních dílů nebo v seznamu kusovníků majetku, postupujte takto:

1. Vyberte **přidat**.
2. V poli **Číslo položky** vyberte položku.
3. Do pole **Množství prodeje** zadejte množství.
4. V poli **Jednotka** vyberte měrnou jednotku pro množství.
5. V poli **Cena nákladů** a **Měna** zadejte příslušné hodnoty.
6. V poli **Vlastnost řádku** vyberte vlastnost řádku.
7. Chcete-li změnit seznam dimenzí zobrazený na řádcích položek, vyberte **Zásoby** > **Zobrazit dimenze**, vyberte dimenze a pak nastavte možnost **Uložit nastavení** na **Ano**.

Chcete-li přidat náhradní díl ze seznamu schválených náhradních dílů, postupujte takto:

1. Vyberte možnost **Přidat náhradní díly**.
2. Vyberte náhradní díl a upravte související informace podle potřeby.
3. Vyberte **OK**.

Chcete-li přidat položku z kusovníku majetku, postupujte následujícím způsobem:

1. Vyberte **Přidat položky kusovníku**.
2. Vyberte položku a upravte související informace podle potřeby.
3. Vyberte **OK**.

Chcete-li získat přehled o tom, kde se ve správě majetku používá položka na vybraném řádku, ve vztahu k majetku, výchozím typům práce, náhradním dílům a pracovním příkazům, vyberte **Položka, kde se používá**. Další informace o tomto přehledu naleznete v tématu [Položka, kde se používá](../controlling-and-reporting/item-where-used.md)se používá.


## <a name="add-an-expense-forecast-to-a-work-order"></a>Přidání prognózy výdajů do pracovního příkazu

1. Na stránce **Prognóza údržby pracovního příkazu** vyberte úlohu pracovního příkazu, do které chcete přidat prognózu.

2. Na pevné záložce **Výdaje** výběrem tlačítka **Přidat** vytvořte nový řádek.

3. V poli **Kategorie** vyberte kategorii.

4. Poté zadejte množství v poli **Množství**.

5. Do polí **Nákladová cena**, **Prodejní měna** a **Prodejní cena** zadejte příslušné hodnoty.

6. V poli **Vlastnost řádku** vyberte typ poplatku, který má být na řádku použit.

>[!NOTE]
>Na pevné záložce **Součty prognóz údržby** můžete zobrazit přehled počtu řádků vytvořených na jednotlivých kartách, pro vybranou úlohu pracovního příkazu a pro daný pracovní příkaz. Zobrazuje také součet prognózovaných pracovních hodin pro úlohu pracovního příkazu a pro daný pracovní příkaz.

Na následujícím obrázku je uveden příklad stránky **Prognóza údržby pracovního příkazu**.

![Obrázek č. 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Automatická aktualizace prognóz pracovních příkazů

Pokud jsou hodinové náklad,y náklady na položku a výdaje aktualizovány v ostatních modulech aplikace Microsoft Dynamics 365 for Finance and Operations, můžete automaticky aktualizovat změny prognóz pracovních příkazů ve správě majetku, aby se tyto změny projevily. To pomáhá zajistit, aby v prognózách pracovního příkazu byly vždy nejnovější nákladové ceny. Je také možné provést podobné aktualizace pro [prognózy typů práce údržby](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

1. Vyberte položky **Správa majetku** > **Pravidelně** > **Prognóza** > **Aktualizovat prognózu pracovního příkazu**.

2. V dialogovém okně **Aktualizovat prognózu pracovního příkazu** na pevné záložce **Záznamy k zahrnutí** můžete přidat výběry týkající se konkrétních pracovních příkazů nebo úloh pracovních příkazů podle potřeby. Kliknutím na tlačítko **Filtr** proveďte příslušné výběry.

3. Na záložce s náhledem **Spustit na pozadí** můžete dle potřeby nastavit automatickou aktualizaci jako dávkovou úlohu.

4. Kliknutím na tlačítko **OK** spustíte aktualizaci prognózy.


Na následujícím obrázku je uveden příklad stránky **Aktualizovat prognózu údržby pracovního příkazu**.

![Obrázek č. 2](media/07-work-orders.png)

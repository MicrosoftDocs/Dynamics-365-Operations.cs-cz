---
title: Prognózy údržby
description: Toto téma popisuje prognózy údržby v modulu Správa majetku.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
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
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 383c910b40199f2da863144c6dc85a579d0091e9
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024492"
---
# <a name="maintenance-forecasts"></a>Prognózy údržby

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Při vytváření pracovního příkazu vytváříte úlohy pracovních příkazů se souvisejícími položkami majetku a typy práce údržby. Pokud vyberete typ práce údržby obsahující prognózy údržby, budou prognózy automaticky zkopírovány do tohoto pracovního příkazu.

Řádky prognózy můžete přidávat nebo odstraňovat v rámci pracovního příkazu. Nastavení stavu životního cyklu pracovního příkazu, související typ projektu a pravidla fáze související s typem projektu určují, zda lze přidávat nebo upravovat řádky prognózy. 

1. Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. V seznamu vyberte požadovaný pracovní příkaz a klepněte na možnost **Prognóza**. V části **Prognóza údržby pracovního příkazu** jsou zobrazeny řádky prognózy z typu práce údržby vybrané na pracovním příkazu.


## <a name="add-hours-forecast-to-a-work-order"></a>Přidat hodiny prognózy do pracovního příkazu

1. Vyberte úlohu pracovního příkazu, do níž chcete přidat prognózu.

2. Na záložce s náhledem **Hodiny** kliknutím na tlačítko **Přidat** vytvořte nový řádek.

3. V poli **Kategorie** vyberte kategorii.

4. Do pole **Hodiny** zadejte počet prognózovaných hodin.

5. V poli **Vlastnost řádku** vyberte typ poplatku, který má být na řádku použit.


## <a name="add-items-forecast-to-a-work-order"></a>Přidání prognózy položek do pracovního příkazu

Existují tři způsoby přidání položek do prognózy údržby pracovního příkazu: můžete vytvořit řádky pro položky (náhradní díly), které nejsou zahrnuty do seznamu náhradních dílů nebo kusovníku majetku, můžete vybrat náhradní díly ze seznamu schválených náhradních dílů a vybrat položky z kusovníku majetku.

1. Vyberte úlohu pracovního příkazu, do níž chcete přidat prognózu.

2. Vyberte záložku s náhledem **Položky**.

3. Chcete-li vytvořit nový řádek pro náhradní díl, který není v seznamu náhradních dílů nebo v seznamu kusovníků majetku, klepněte na možnost **Přidat**.

4. V poli **Číslo položky** vyberte položku.

5. Vložte množství do pole **Prodejní množství** a vyberte jednotku množství v poli **Jednotka**.

6. Do příslušných polí vložte nákladovou cenu a měnu a vyberte **Vlastnost řádku**.

7. Chcete-li změnit seznam dimenzí zobrazený na řádcích položek, klepněte na volby **Zásoby** > **Zobrazit dimenze**, vyberte dimenze a na přepínacím tlačítku **Uložit nastavení** vyberte možnost „Ano“.

8. Chcete-li do prognózy údržby přidat schválený náhradní díl, klikněte na možnost **Přidat náhradní díly**, v případě potřeby vyberte náhradní díl, upravte související informace a klepněte na tlačítko **OK**.

9. Chcete-li do prognózy přidat položky kusovníku majetku, klikněte na možnost **Přidat položkykusovníku**, vyberte položku, upravte související informace a klikněte na tlačítko **OK**.

10. Klikněte na možnost **Kde byla položka použita,** chcete-li získat přehled o tom, kde se ve Správě majetku používá položka na vybraném řádku ve vztahu k majetku, výchozím typům práce údržby, náhradním dílům a pracovním příkazům. 



## <a name="add-expense-forecast-to-a-work-order"></a>Přidání prognózy výdajů do pracovního příkazu

1. Tohle téma popisuje, jak přidat prognózu výdajů do pracovního příkazu. Na levé straně formuláře vyberte úlohu pracovního příkazu, do které chcete přidat prognózu.

2. Vyberte záložku s náhledem **Výdaje**.

3. Kliknutím na **Přidat** vytvořte nový řádek.

4. V poli **Kategorie** vyberte kategorii.

5. Poté zadejte množství v poli **Množství**.

6. Do příslušných polí zadejte nákladovou cenu, prodejní měnu a prodejní cenu.

7. V poli **Vlastnost řádku** vyberte typ poplatku, který má být na řádku použit.

>[!NOTE]
>Na záložce s náhledem **Součty prognóz údržby** můžete zobrazit přehled počtu řádků vytvořených na jednotlivých kartách, pro vybranou úlohu pracovního příkazu a pro daný pracovní příkaz. Můžete také zobrazit součet prognózovaných pracovních hodin pro úlohu pracovního příkazu a pro daný pracovní příkaz.

![Obrázek č. 1](media/06-work-orders.png)


## <a name="automatic-update-of-work-order-forecasts"></a>Automatická aktualizace prognóz pracovních příkazů

V modulu Správa majetku můžete automaticky aktualizovat všechny změny prognóz pracovních příkazů ohledně hodinových nákladů, nákladů na položky a výdajů, které byly aktualizovány v jiných modulech. Je to proto, aby v prognózách pracovního příkazu byly vždy nejnovější nákladové ceny. Je také možné provést podobné aktualizace pro [prognózy typů práce údržby](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md).

1. Klikněte na položky **Správa majetku** > **Pravidelně** > **Prognóza** > **Aktualizovat prognózu pracovního příkazu**.

2. V rozevíracím dialogovém okně **Aktualizovat prognózu pracovního příkazu** můžete přidat výběr týkající se konkrétních pracovních příkazů nebo úloh pracovních příkazů, pokud je to nutné. Kliknutím na tlačítko **Filtr** proveďte tento výběr.

3. Pokud je to nutné, na záložce s náhledem **Spustit na pozadí** můžete dle potřeby nastavit automatickou aktualizaci jako dávkovou úlohu.

4. Kliknutím na tlačítko **OK** spustíte aktualizaci prognózy.


![Obrázek č. 2](media/07-work-orders.png)


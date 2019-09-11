---
title: Skupiny pracovních příkazů
description: V tomto tématu je popsán postup při práci se skupinami pracovních příkazů v modulu Správa majetku.
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
ms.openlocfilehash: 069fa02073808fd7bbaac9bc1603e49ce4d450eb
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875547"
---
# <a name="work-order-pools"></a>Skupiny pracovních příkazů


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Skupiny pracovních příkazů lze použít k seskupení pracovních příkazů, které mají něco společného. Můžete například vytvořit skupiny pracovních příkazů pro

- Pracovní skupiny, např. skupina údržby A, skupina údržby B  

- profesionální dovednosti, např. elektrikáři nebo instalatéři  

- fyzická umístění  

- časové plány, například týdny nebo jiná období  


V případě potřeby lze vložit jeden pracovní příkaz do mnoha skupin pracovních příkazů.


## <a name="create-work-order-pool"></a>Vytvořit skupinu pracovních příkazů

Ve **Všech skupinách pracovních příkazů** nebo **Aktivních skupinách pracovních příkazů** můžete získat přehled o vašich skupinách pracovních příkazů a vytvořit nové skupiny.

1. Klikněte na **Správa majetku** > **Společné** > **Skupiny pracovních příkazů** > **Všechny skupiny pracovních příkazů** nebo **Aktivní skupiny pracovních příkazů**.

2. Klepněte na možnost **Nový**.

3. Zadejte ID skupiny pracovních příkazů do pole **Skupina** a název do pole **Název**.

4. Výběrem možnosti Ano na přepínacím tlačítku **Aktivní** označíte, že skupina pracovních objednávek je aktivní.

5. Výběrem možnosti Ano na přepínacím tlačítku **Odebrat vztahy pracovních příkazů**, chcete-li automaticky odebrat pracovní příkazy ze skupiny pracovních příkazů.

6. V poli **Odstranit stav životního cyklu** vyberte stav životního cyklu pracovního příkazu. Například stav životního cyklu pracovního příkazu pro dokončení pracovního příkazu může být nastaven tak, aby automaticky odstranil vztahy ke skupinám pracovních příkazů.

7. Do skupiny pracovních příkazů můžete ihned přidávat pracovní příkazy. Na pevné záložce **Pracovní příkazy** klikněte na tlačítko **Přidat řádek**.

8. V poli **Pracovní příkaz** vyberte pracovní příkaz. Související pole se automaticky aktualizují.

9. Chcete-li přidat další pracovní příkazy, zopakujte kroky 7–8.

10. V poli **Pořadí řazení** lze určit, zda mají být pracovní příkazy prováděny v určitém pořadí. Vložením čísel 1, 2, 3 atd. určete specifickou posloupnost pro vybrané pracovní příkazy.

11. Chcete-li zobrazit seznam všech pracovních příkazů zahrnutých ve fondu pracovních příkazů, klikněte na tlačítko **Pracovní příkazy**.

12. Klikněte na tlačítko **Vytížení kapacity** pro otevření **Vytížení kapacity**, chcete-li vypočítat a zobrazit vytížení kapacity pro rozvrh údržby, nenaplánované pracovní příkazy a naplánované pracovní příkazy.

13. Klikněte na tlačítko **Prognóza položek** pro otevření **Prognózy položek**, chcete-li vypočítat a zobrazit prognózu položek pro položky (náhradní díly a další požadované položky) související s rozvrhem údržby, nenaplánovanými pracovními příkazy a naplánovanými pracovními příkazy.

14. Klikněte na tlačítko **Nákupní žádanka pracovního příkazu** pro otevření **Nákupní žádanky pracovního příkazu**, chcete-li zobrazit seznam nákupních žádanek souvisejících s pracovními příkazy ve skupině pracovních příkazů.

15. Klikněte na tlačítko **Nákupní pracovní příkaz** pro otevření **Nákupního pracovního příkazu**, chcete-li zobrazit seznam pracovních příkazů souvisejících s pracovními příkazy ve skupině pracovních příkazů.

>[!NOTE]
>Není-li pro plánování práce relevantní skupina pracovních příkazů, nastavte zaškrtávací políčko **Aktivní** dané skupiny na Ne v zobrazení seznamu **Skupina pracovních příkazů**.

Zaškrtněte políčko **Odstranit vztahy pracovního příkazu**, chcete-li odstranit všechny řádky pracovního příkazu, například pro vytvoření prázdné skupiny, kterou lze později použít pro jiné pracovní příkazy. Nezapomeňte zrušit zaškrtnutí políčka **Odstranit vztahy pracovního příkazu**, pokud chcete použít skupinu pracovních příkazů k vytvoření nových vztahů pracovních příkazů později.


![Obrázek č. 1](media/22-work-orders.png)


## <a name="add-work-order-to-a-work-order-pool"></a>Přidání pracovních příkazů do skupiny pracovních příkazů.

Jak je popsáno výše, můžete při vytvoření skupiny přidat do skupiny pracovních příkazů pracovní příkazy. Pracovní příkaz lze rovněž přidat do skupiny pracovních příkazů ze seznamu **Všechny pracovní příkazy**.

1. Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

2. V seznamu vyberte požadovaný pracovní příkaz a klepněte na možnost **Skupina pracovních příkazů**.

3. V poli **Přidat nebo odebrat** vyberte možnost „Přidat“.

4. Vyberte skupinu pracovních příkazů v poli **Skupina**.

5. Klikněte na tlačítko **OK**.

6. Po přidání pracovního příkazu do skupiny pracovních příkazů, pokud chcete umístit pracovní příkaz do skupiny v určitém pořadí: otevřete jednu ze stránek se seznamem skupin pracovních příkazů, vyberte skupinu a klikněte na tlačítko **Upravit** a upravte pořadí řazení pro pracovní příkazy ve skupině ve formuláři **Skupina pracovních příkazů** > pevná záložka **Pracovní příkazy** > pole **Pořadí řazení**.

Chcete-li vybraný pracovní příkaz odebrat ze skupiny pracovních příkazů, vyberte v kroku 3 možnost „Odebrat“.


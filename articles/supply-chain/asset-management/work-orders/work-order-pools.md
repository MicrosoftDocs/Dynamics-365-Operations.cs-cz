---
title: Skupiny pracovních příkazů
description: V tomto článku je popsán postup při práci se skupinami pracovních příkazů v modulu Správa majetku.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetWorkOrderTablePoolPart, EntAssetWorkOrderPoolReferenceInfoPart, EntAssetWorkOrderPool, EntAssetWorkOrderPoolPreviewPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: dc9eaf82c2f3336f8c3400fcd3f1165ed4fa56d8
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014932"
---
# <a name="work-order-pools"></a>Skupiny pracovních příkazů

[!include [banner](../../includes/banner.md)]


Skupiny pracovních příkazů lze použít k seskupení pracovních příkazů, které mají něco společného. Zde je několik příkladů akcí, které lze vytvořit z následujících skupin pracovních příkazů:

- Pracovní skupiny, např. skupina údržby A nebo skupina údržby B  

- Profesionální dovednosti, např. elektrikáři nebo instalatéři  

- Fyzická umístění  

- Časové plány, například týdny nebo jiná období  

Podle potřeby lze do více skupin pracovních příkazů vložit jednu pracovní objednávku.


## <a name="create-a-work-order-pool"></a>Vytvoření fondu pracovních příkazů

Na stránce se seznamem **Všechny skupiny pracovních příkazů** nebo **Aktivní skupiny pracovních příkazů** můžete získat přehled o vašich skupinách pracovních příkazů a vytvořit nové skupiny.

1. Vyberte **Správa majetku** > **Skupiny pracovních příkazů** > **Všechny skupiny pracovních příkazů** nebo **Aktivní skupiny pracovních příkazů**.

2. Zvolte **Nové**.

3. V poli **Fond** zadejte identifikátor fondu pracovního příkazu.

4. Do pole **Název** zadejte název.

5. Natavením možnosti **Ano** na přepínacím tlačítku **Aktivní** označíte, že skupina pracovních objednávek je aktivní.

6. Nastavte možnost **Ano** na přepínacím tlačítku **Odstranit vztahy pracovních příkazů**, chcete-li automaticky odebrat pracovní příkazy ze skupiny pracovních příkazů.

7. V poli **Odstranit stav životního cyklu** vyberte stav životního cyklu pracovního příkazu. Například stav životního cyklu pracovního příkazu pro dokončení pracovního příkazu může být nastaven tak, aby automaticky odstranil vztahy ke skupinám pracovních příkazů.

    Do skupiny pracovních příkazů můžete ihned přidávat pracovní příkazy.

8. Na pevné záložce **Pracovní příkazy** vyberte tlačítko **Přidat řádek**.

9. V poli **Pracovní příkaz** vyberte pracovní příkaz. Související pole se automaticky aktualizují.

10. Opakováním kroků 8 až 9 přidejte další pracovní příkazy.

11. Pokud mají být přidané pracovní příkazy prováděny v určitém pořadí, můžete v poli **Pořadí řazení** zadat čísla **1**, **2**, **3** atd. a určit tak pořadí.

12. Chcete-li zobrazit seznam všech pracovních příkazů, které jsou zahrnuty ve fondu pracovních příkazů, na kartě **Fond pracovních příkazů** ve skupině **Zobrazit související fond pracovních příkazů** vyberte možnost **Pracovní příkazy**, pro kterou chcete otevřít stránku se seznamem **Všechny pracovní příkazy**.

13. Chcete-li vypočítat a zobrazit vytížení kapacity pro plán údržby, neplánované pracovní příkazy a plánované pracovní příkazy, v podokně akcí na kartě **Fond pracovních příkazů** ve skupině **Zobrazit související fond pracovních příkazů** vyberte **Vytížení kapacity** k otevření dialogového okna **Vypočítat vytížení kapacity**.

14. Chcete-li vypočítat a zobrazit prognózy položek (náhradní díly a další požadované položky), které souvisí splánem údržby, neplánovanými pracovními příkazy a plánovanými pracovními příkazy, v podokně akcí na kartě **Fond pracovních příkazů** ve skupině **Zobrazit související fond pracovních příkazů** vyberte **Prognóza položky** k otevření dialogového okna **Vypočítat prognózu položky**.

15. Chcete-li zobrazit seznam nákupních žádanek, které souvisí s pracovními příkazy ve fondu pracovních příkazů, v podokně akcí na kartě **Fond pracovních příkazů** ve skupině **Nákup** vyberte možnost **Nákupní žádanka pracovního příkazu** k otevření stránky se seznamem **Nákupní žádanka pracovního příkazu**.

16. Chcete-li zobrazit seznam nákupních objednávek, které souvisí s pracovními příkazy ve fondu pracovních příkazů, v podokně akcí na kartě **Fond pracovních příkazů** ve skupině **Nákup** vyberte možnost **Nákupní objednávka pracovního příkazu** k otevření stránky se seznamem **Nákupní objednávka pracovního příkazu**.

>[!NOTE]
>Není-li pro vaše plánování práce dále relevantní fond pracovních příkazů, nastavte možnost **Aktivní** daného fondu na **Ne** v zobrazení seznamu na stránce **Fond pracovních příkazů**.

Chcete-li odstranit všechny řádky pracovního příkazu, nastavte možnost **Odstranit vztahy pracovního příkazu** na hodnotu **Ano**. Tato možnost je užitečná například tehdy, chcete-li vytvořit prázdný fond, který lze použít později pro další pracovní příkazy. Až budete později připravení použít fond pracovního příkazu k vytvoření nových vztahů pracovního příkazu, nezapomeňte nastavit možnost **Odstranit vztahy pracovního příkazu** na **Ne**.

Na následujícím obrázku je uveden příklad stránky se seznamem **Fond pracovního příkazu**.

![Obrázek č. 1.](media/22-work-orders.png)


## <a name="add-a-work-order-to-a-work-order-pool"></a>Přidání pracovního příkazu do skupiny pracovních příkazů

Jak je popsáno v předchozí části, můžete při vytvoření skupiny přidat do skupiny pracovních příkazů pracovní příkazy. Můžete také přidat pracovní příkazy do fondu pracovních příkazů na stránce se seznamem **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy**.

1. Vyberte pracovní příkaz v seznamu a pak v podokně akcí na kartě **Pracovní příkaz** ve skupině **Údržba** vyberte **Fond pracovního příkazu**.

2. V seznamu vyberte požadovaný pracovní příkaz a klepněte na možnost **Skupina pracovních příkazů**.

3. V dialogovém okně **Spravovat fond pracovních příkazů** v poli **Přidat/odebrat** vyberte **Přidat**.

4. Vyberte fond pracovních příkazů v poli **Fond**.

5. Vyberte **OK**.

6. Chcete-li vložit pracovní příkaz, který jste přidali v určitém pořadí ve fondu pracovních příkazů, vyberte stránku se seznamem **Všechny fondy pracovních příkazů** nebo **Aktivní fondy pracovních příkazů**, vyberte požadovaný fond a poté vyberte **Upravit**. Pak na stránce **Fond pracovních příkazů** na pevné záložce **Pracovní příkazy** použijte pole **Pořadí řazení** k nastavení pořadí pracovních příkazů zahrnutých ve fondu.

Chcete-li vybraný pracovní příkaz odebrat z fondu pracovních příkazů, vyberte v kroku 3 možnost **Odebrat**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
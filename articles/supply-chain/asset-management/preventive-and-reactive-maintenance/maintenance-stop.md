---
title: Aktivity prostoje údržby
description: Tohle téma popisuje, jak se používá prostoj údržby k získání přehledu o kapacitě potřebné k provádění prací údržby určitých položek majetku během určitého období.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetMaintenanceStopCopy, EntAssetMaintenanceStopObject, EntAssetObjectProductionStop, EntAssetProductionStopType, EntAssetMaintenanceStop
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 617fca55226e216197c385c88a9d7a8e3de03b03
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889978"
---
# <a name="maintenance-downtime-activities"></a>Aktivity prostoje údržby

[!include [banner](../../includes/banner.md)]

Prostoj údržby slouží k získání přehledu o kapacitě potřebné k provádění prací údržby určitých položek majetku během určitého období. Můžete například vytvořit registraci prostoje údržby pro řádek výroby 10 ve výrobní hale 29-A na výrobním pracovišti 02. Registrace prostojů údržby má počáteční a koncový čas označující období, ve kterém položky majetku související se zastavením údržby nejsou dostupné pro výrobu.

**Aktivity prostojů údržby** představují přehled řádků rozvrhu údržby a prací údržby pracovních příkazů pro související položky majetku během určitého období. Řádky související s pracemi údržby pracovních příkazů mají všechny v období zastavení údržby očekávané datum zahájení. Můžete extrahovat užitečné informace a upravovat plánované práce údržby:

- Získejte přehled o požadovaných dobách vypnutí výrobních zařízení (položek majetku).  
- Získejte přehled o plánované údržbě (v hodinách) seskupený podle kompetencí (skupiny zodpovědných pracovníků údržby nebo pracovníků údržby), například vytížení kapacity elektrikářů, kovářů nebo jiných pracovních skupin údržby vyžadované pro plánované práce údržby.  
- Upravujte řádky rozvrhu údržby nebo prací údržby pracovních příkazů souvisejících s položkami majetku, například změňte očekávané počáteční a koncové časy na řádku nebo vyberte další pracovníky údržby pro optimalizaci workflowu pro pracovníky údržby a skupiny pracovníků údržby.

Pokud byly při registraci prostojů údržby vybrány položky majetku, do registrace prostojů údržby budou zahrnuty všechny otevřené řádky rozvrhu údržby a práce údržby pracovních příkazů související s aktivními pracovními příkazy.

## <a name="maintenance-downtime-activities"></a>Aktivity prostoje údržby

Kliknutím na položky **Správa majetku** > **Společné** > **Aktivity prostojů údržby** > **Všechny aktivity prostojů údržby** otevřete seznam všech aktivit prostojů údržby a prohlédněte si některé informace související s aktivitami. Kliknutím na odkaz ve sloupci **Aktivity prostojů údržby** otevřete podrobné zobrazení. Následující ilustrace znázorňuje příklad stránky **Aktivity prostoje údržby**.

![Obrázek č. 1](media/19-preventive-maintenance.png)


## <a name="create-a-maintenance-downtime-activity"></a>Vytvoření aktivity prostoje údržby

1. Klikněte na položky **Správa majetku** > **Společné** > **Aktivity prostojů údržby** > **Všechny aktivity prostojů údržby** nebo **Aktivní aktivity prostojů údržby**.

2. Klepněte na možnost **Nový**.

3. Zadejte ID do pole **Aktivity prostojů údržby** a název do pole **Název**.

4. Vložte období pro zastavení údržby do polí datum a **Počáteční datum a čas** a **Koncové datum a čas**.

5. Na pevné záložce **Majetek aktivit prostojů údržby** kliknutím na **Přidat řádek** přidejte jednu po druhé položky majetku do aktivity prostoje údržby.

6. Po přidání všech položek majetku klikněte na **Uložit**. Na následujícím obrázku je znázorněn příklad aktivity prostoje údržby se souvisejícími aktivy a úlohami údržby.

7. Práce údržby pracovních příkazů a otevřené řádky rozvrhu údržby související s vybranými položkami majetku zobrazených na pevných kartách **Výsledné práce údržby pracovních příkazů** a **Řádky rozvrhu údržby**. Klikněte na pevné záložce **Obecné** > ve skupině **Pracovní příkazy** > v poli **Hodiny prognózy údržby** a pevné záložce **Obecné** > ve skupině **Rozvrh údržby** > v poli **Hodiny prognózy údržby** vidíte celkový počet hodin prognózovaných pro práce údržby pracovních příkazů a řádky rozvrhu údržby.

Následující ilustrace znázorňuje zobrazení podrobností okna **Aktivity prostoje údržby**.

![Obrázek č. 2](media/20-preventive-maintenance.png)

>[!NOTE]
>Práce údržby pracovních příkazů a řádky rozvrhu údržby související s vybraným majetkem se automaticky aktualizují, pokud jsou po vytvořeny nové pracovní příkazy nebo řádky rozvrhu údržby poté, co jste vytvořili aktivitu prostoje údržby. Pokud například naplánujete plány údržby nebo pořadí údržby pro související položky majetku dva dny po vytvoření aktivity prostoje údržby, budou nové řádky rozvrhu údržby automaticky přidány do prostoje údržby.

8. V části **Všechny aktivity prostoj; údržby** > **Aktivity prostojů údržby** > vyberte ze seznamu aktivitu prostoje údržby a kliknutím na **Vytížení kapacity** otevřete dialogové okno **Vypočítat vytížení kapacity**. V tomto dialogovém okně se nachází přehled o vytížení kapacity: například data, položky majetku, typy položek majetku a typy prací údržby. Všimněte si, že data zobrazená v dialogovém okně představují počáteční a koncové datum pro **Aktivity prostojů údržby**. Tento výpočet zahrnuje položky majetku související s aktivitou prostoje údržby.

9. V dialogovém **Výpočet vytížení kapacity** upravte v případě potřeby počáteční a koncové časy a vyberte, zda chcete do výpočtu zahrnout pracovní příkazy a rozvrhy údržby. V poli **Úroveň** určete, jak detailní má být výpočet vytížení kapacity v případě funkčních míst. Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny položky majetku pro funkční místo, která jsou vybrána v aktivitě prostoje údržby, a proto lze navýšit hodiny na řádku z funkčních míst na nižší úrovni. Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky vytížení kapacity na všech úrovních funkčních míst, ke kterým se vztahují.

10. Výpočet zahájíte klepnutím na tlačítko **OK**. Celkový počet hodin je zobrazen v přehledu **Vytížení kapacity**. Na kartě **Vytížení kapacity** > ve skupinách podokna akce **Seskupit podle...** klikněte na příslušná tlačítka, čímž získáte podrobnější přehled o přidělení prognózovaných hodin. Na následujícím obrázku jsou uvedeny výsledky výpočtu nákladů **vytížení kapacity**.

![Obrázek č. 3](media/21-preventive-maintenance.png)

11. Po získání přehledu vytížení kapacity, pokud chcete upravit práce údržby pracovních příkazů nebo řádky plánu údržby, vraťte se do podrobného zobrazení **Aktivity prostoje údržby** a vyberte řádky, které chcete upravit na pevných záložkách **Výsledné práce údržby pracovních příkazů** a **Řádky rozvrhu údržby**.

12. Klikněte na tlačítko **Upravit** a upravte očekávaná počáteční a koncová data, úroveň služeb nebo zodpovědné pracovníky údržby pro vybrané práce údržby pracovních příkazů nebo řádky rozvrhu údržby.

13. Po provedení požadovaných úprav klepněte na tlačítko **OK**. 

>[!NOTE]
>Práce údržby pracovních příkazů a řádky rozvrhu údržby, které nejsou zahrnuty do období prostoje údržby po provedení úprav, budou automaticky odebrány z **Aktivit prostojů údržby**.

14. V části **Všechny aktivity prostoj; údržby** > **Aktivity prostojů údržby** > vyberte ze seznamu aktivitu prostoje údržby a kliknutím na možnost **Prognóza položky** otevřete dialogové okno **Vypočítat prognózu položky**. V tomto dialogovém okně můžete vypočítat prognózy pro položky (náhradní díly a jiné povinné položky) a jejich seskupením například podle data, majetku, typu majetku a typu úlohy údržby získat přehled. Všimněte si, že data zobrazená v dialogovém okně představují počáteční a koncové datum pro **Aktivity prostojů údržby**. Tento výpočet zahrnuje náhradní díly a položky související s položkami majetku vybranými v aktivitě prostoje údržby.

15. V dialogovém **Výpočet prognózu položky** upravte v případě potřeby počáteční a koncové časy a vyberte, zda chcete do výpočtu zahrnout pracovní příkazy a rozvrhy údržby. V poli **Úroveň** určete, jak detailní má být výpočet vytížení kapacity v případě funkčních míst. Pokud například do pole zadáte číslo „1“ a máte strukturu funkčních míst o více úrovních, budou na nejvyšší úrovni zobrazeny všechny položky majetku pro funkční místo, která jsou vybrána v aktivitě prostoje údržby, a proto lze navýšit hodiny na řádku z funkčních míst na nižší úrovni. Pokud do pole **Úroveň** zadáte číslo „0“, zobrazí se podrobný výsledek znázorňující všechny řádky vytížení kapacity na všech úrovních funkčních míst, ke kterým se vztahují.

16. Výpočet zahájíte klepnutím na tlačítko **OK**. Celkový počet prognóz položky je zobrazen v přehledu **Prognóza položky**. Na kartě **Prognóza položky** > ve skupinách podokna akce **Seskupit podle**... klikněte na příslušná tlačítka, čímž získáte podrobnější přehled o přidělení prognózovaných položek. Následující obrázek ukazuje výsledky výpočtu **Prognóza položky**.

![Obrázek č. 4](media/22-preventive-maintenance.png)

- Položky majetku lze kopírovat z jedné aktivity prostoje údržby do jiné. V části **Všechny aktivity prostojů údržby** vyberte tlačítko **Kopírovat aktivity prostoje údržby** a vyberte požadované položky v polích **Z aktivit prostoje údržby** a **Do aktivit prostoje údržby** prostoje a klikněte na tlačítko **OK**.
- V části **Všechny aktivity prostoje údržby** kliknutím na tlačítko **Řádky rozvrhu údržby** nebo **Aktivní pracovní příkazy** otevřete související seznamy a zobrazíte řádky související s vybranou aktivitou prostoje údržby.


---
title: Naplánovat pracovní příkazy
description: Toto téma vysvětluje, jak plánovat pracovní příkazy v modulu Správa majetku.
author: josaw1
manager: tfehr
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a594bacb1fcf53ae4a278dbb26f1de174e22288c
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275595"
---
# <a name="schedule-work-orders"></a>Naplánovat pracovní příkazy

[!include [banner](../../includes/banner.md)]

 

Toto téma vysvětluje, jak plánovat pracovní příkazy v modulu Správa majetku. 

Požadovaný počet hodin pro pracovní příkaz je definován součtem předpokládaných hodin minus zaúčtované hodiny. Je-li vyžadováno více času, musí být prognóza upravena odpovídajícím způsobem. Ve volbě **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy** nebo **Aktivní pracovní příkazy** můžete zobrazit nebo upravit prognózy na pracovním příkazu výběrem pracovního příkazu a kliknutím na **Prognóza** na kartě **Pracovní příkaz**. Po vytvoření a odhadu pracovních příkazů je dalším krokem přidělení požadovaných pracovníků a nástrojů údržby, které dokončí pracovní příkazy.

Je možné naplánovat pouze pracovní příkazy se stavem životního cyklu pracovního příkazu, který umožňuje plánování. Možnost Povolit plánování je nastaveno ve **Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Stavy životního cyklu** >  pevná záložka **Obecné** > přepínací tlačítko **Povolit plánování**.

1. Klikněte na **Správa majetku** > **Společné** > **Pracovní příkazy** > **Všechny pracovní příkazy**.

2. Ze seznamu vyberte pracovní příkazy, které chcete naplánovat. Seznam lze například seřadit podle **Aktuálního stavu životního cyklu**.

3. Na kartě **Obecné** klikněte na volbu **Plánovat**.

4. V dialogovém okně **Naplánovat pracovní příkazy** můžete přidat výběr týkající se očekávaného data zahájení a úrovně služeb, je-li to nutné. Pokud by proces plánování měl zohledňovat omezení kapacity týkající se již naplánovaných zdrojů pro jiné úlohy, zkontrolujte, zda jsou přepínací tlačítka **Majetek**, **Nástroj** a **Pracovník** nastavena na hodnotu „Ano“.

    [!NOTE]
    Nastavíte-li přepínací tlačítka **Majetek**, **Nástroj** a **Pracovník** a pracovník na hodnotu „Ne“, existující rezervace budou ignorovány. V informačním protokolu se zobrazí seznam překrývajících se plánů pracovních příkazů a kliknutím na zprávy otevřete pracovní příkaz a v případě potřeby přeplánujte.

5. Chcete-li zobrazit podrobné informace o procesu plánování, vyberte v přepínacím tlačítku **Podrobný** možnost „Ano“. To znamená, že v informačním protokolu budou zobrazeny podrobné informace o vypočtených hodnotách pro pracovní příkazy a pracovníky údržby.

6. Klepnutím na tlačítko **OK** spusťte proces plánování.

7. Po dokončení plánování se v informačním protokolu zobrazí počet plánovaných pracovních příkazů a podrobnější informace, pokud bylo přepínací tlačítko **Podrobný** nastaveno na hodnotu „Ano“.

>[!NOTE]
>Pracovní příkazy jsou naplánovány v jednom cyklu na pracovní příkaz, nikoli na úlohu pracovního příkazu. Dialogové okno **Naplánovat pracovní příkazy** lze rovněž otevřít přímo ve **Správa majetku** > **Periodické** > **Pracovní příkazy** > **Plánovat pracovní příkazy**. Proveďte výběry a kliknutím na tlačítko **OK** spusťte plánování pracovních příkazů. V dialogovém okně **Plánovat pracovní příkazy** > pevná záložka **Spustit na pozadí** lze nastavit plánování pracovních příkazů jako dávkovou úlohu.

*Příklad:* v níže uvedeném obrázku bude vzorec vložený do pole **Očekávaný začátek** generovat pracovní příkaz pro všechny pracovní příkazy s očekávaným počátečním datem týdne od nynějška a později. Tento vzorec může být užitečný, když provádíte plánování pracovních příkazů průběžně, ale chcete mít jistotu, že pracovní příkazy naplánované pro následující 5-6 dnů nebudou přeplánovány.

![Obrázek č. 1](media/03-work-order-scheduling.png)

Typ pracovního příkazu vztahující se k pracovním objednávkám může nastavovat plánování jednoho pracovníka údržby (**Správa majetku** > **Nastavení** > **Pracovní příkazy** > **Typ pracovních příkazů** >  přepínací tlačítko **Jeden pracovník údržby** nastavené na hodnotu „Ano“). To znamená, že pokud je typ pracovního příkazu použit v rámci pracovního příkazu, bude přepínací tlačítko **Jeden pracovník údržby** nastaveno na „Ano“ na stránce s podrobnostmi **Všechny pracovní příkazy** > zobrazení **Záhlaví** > pevná záložka **Plánovat**. Při plánování pracovních příkazů budou všechny úlohy pracovních příkazů vytvořené v daném pracovním příkazu následně naplánovány na stejného pracovníka údržby. V případě potřeby můžete upravit výběr pomocí přepínacího tlačítka **Jeden pracovník údržby** ve volbě **Všechny pracovní příkazy** tak, aby bylo možné plánovat několik pracovníků nebo jednoho pracovníka na úlohy pracovních příkazů.

Proces plánování ve správě majetku zahrnuje několik faktorů ve výpočtu plánu:

- Výpočet hodnocení jak pro pracovní příkazy, tak pro pracovníky údržby. Skóre pro pracovní příkazy a pracovníky údržby se nastavují v **Parametrech správy majetku**. 
- Probíhá kontrola odpovídajících kompetencí, což jsou dovednosti a certifikáty, které jsou nutné k provedení úlohy. Dovednosti a certifikáty se nastavují u pracovníků údržby v modulu **Lidské zdroje** (**Lidské zdroje** > **Pracovníci** > **Pracovníci** > vybrat pracovníka v seznamu > karta **Pracovník** > sekce **Kompetence** > tlačítka **Dovednosti** a **Certifikáty**). Rovněž je možné přidat dovednosti a certifikáty k typům práce údržby a k oborům práce údržby. Více informací o kompetencích a typech prací údržby najdete v tématu [Kategorie typů práce údržby, typy práce údržby , varianty typů práce údržby, obory práce údržby a kontrolní seznamy údržby](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)  

## <a name="scores-used-in-work-order-scheduling"></a>Skóre použité při plánování pracovního příkazu

Výpočet skóre pro úlohu pracovního příkazu je založen na očekávaném počátečním datu a na úrovni služeb pracovního příkazu.

Výpočet **Počátečního data**: pro každé budoucí datum vypočtené od očekávaného počátečního data je skóre počátečního data odečteno a násobeno skórem, které je "10" v níže uvedených příkladech.

Výpočet **Kritičnosti**: skóre kritičnosti vynásobené kritičností pracovního příkazu.

Výpočet **Úrovně služeb**: skóre úrovně služeb vydělené úrovní služeb na pracovním příkazu.

V níže uvedených příkladech je skóre kritičnosti "2" a skóre úrovně služeb je "5" a "100".

**Příklad 1:**

| ID pracovního příkazu | Očekávané počáteční datum | Kritičnost pracovního příkazu | Úroveň služby pracovního příkazu | Výpočet               | Hodnocení      |
|---------------|---------------------|------------------------|--------------------------|---------------------------|------------|
| WO-00010816   | Zítra            | 2                      | 20              | (-1 \* 10) + (2 \* 2) + 5 / 20     | \- 5.75    |
| WO-00010817   | Dva dny od teď   | 2                      | 20              | (-2 \* 10) + (2 \* 2) + 5 / 20     | \- 15.75   |
| WO-00010818   | Dva dny od teď   | 3                      | 5               | (-2 \* 10) + (2 \* 3) + 5 / 5      | \- 13      |

Pracovní příkazy budou naplánovány v následujícím pořadí: WO-000108**16**, WO-000108**18**, WO-000108**17**.

**Příklad 2:**

| ID pracovního příkazu | Očekávané počáteční datum | Kritičnost pracovního příkazu | Úroveň služby pracovního příkazu | Výpočet                 | Hodnocení    |
|---------------|---------------------|------------------------|---------------------|----------------------------------|----------|
| WO-00010816   | Zítra            | 2                      | 20                  | (-1 \* 10) + (2 \* 2) + 100 / 20 | \- 1     |
| WO-00010817   | Dva dny od teď   | 2                      | 20                  | (-2 \* 10) + (2 \* 2) + 100 / 20 | \- 11    |
| WO-00010818   | Dva dny od teď   | 3                      | 5                   | (-2 \* 10) + (2 \* 3) + 100 / 5  | 6        |

Pokud je skóre úrovně služeb zvýšeno na 100 namísto 5, bude pořadí plánování následující: WO-000108**18**, WO-000108**16**, WO-000108**17**.

Skóre hodnocení, která se týkají výpočtu, kteří pracovníci údržby mají pracovat na pracovních příkazech, jsou nastavena jako čísla, která se přidávají ke kalkulacím pracovníka údržby při plánování pracovních příkazů. Pracovník údržby s nejvyšším skóre je vybrán na pracovní příkaz. Zde je stručný popis hodnocení pracovníků údržby:

| Skóre pracovníka údržby| Popis |
|---|---|
| Odpovědný pracovník | Pokud je pracovník údržby vybrán jako odpovědný pracovník na pracovní příkaz, skóre bude přidáno. |
| Odpovědná skupina pracovníků údržby | Pokud je pracovník údržby součástí skupiny odpovědných pracovníků na pracovním příkazu, skóre bude přidáno. |
| Preferovaný pracovník údržby         | Pokud je pracovník údržby vybrán jako preferovaný pracovník údržby majetku, skóre bude přidáno. |
| Preferovaná skupina pracovníků údržby   | Pokud je pracovník údržby součástí skupiny preferovaných pracovníků údržby majetku, skóre bude přidáno.  |
| Umístění  | Pokud vaše společnost používá funkční místa, pracovníci údržby dostanou plné skóre, pokud jsou umístěni na funkčním místě souvisejícím s majetkem. Pokud má funkční místo majetku nadřazené umístění, pracovníci údržby na tomto funkčním místě dostanou 1/2 skóre. Pokud má toto místo také nadřazenou položku, pracovníci údržby na tomto místě získají 1/3 skóre. Pokud má toto místo také nadřazenou položku, pracovníci údržby na tomto místě získají 1/4 skóre atd. Pokud vaše společnost používá místo majetku, které nedoporučujeme, místo, oblast a zóna se používají k výpočtu skóre místa. Pracovníci dostanou plné skóre, pokud jsou umístěni v místě a oblasti a zóně související s majetkem. Pokud se místo pracovníka shoduje pouze s místem a oblastí, je skóre hodnocení pro pracovníka údržby 2/3 plného skóre. Pokud se místo pracovníka údržby shoduje pouze s místem, je skóre hodnocení pro pracovníka údržby 1/3 plného skóre. |
| Počáteční datum pracovníka  | U každého data, kdy je plánované datum zahájení pozdější než očekávané datum zahájení, bude skóre odečteno.  |

>[!NOTE]
>Je-li skóre nastaveno na hodnotu 0, hodnocení se nevypočítává. To je užitečné například v případě, že nechcete do plánování zahrnout odpovědného pracovníka.

## <a name="competencies-used-in-work-order-scheduling"></a>Kompetence použité při plánování pracovního příkazu

Požadavky na dovednosti a certifikáty lze nastavit na typech prací údržby (**Správa majetku** > **Nastavení** > **Úlohy** > **Typy prací údržby**) a oborech prací údržby (**Správa majetku** > **Nastavení** > **Úlohy** > **Obory prací údržby**). 

Typ prací údržby a obory prací údržby se vybírají u úloh pracovních příkazů. Pokud byly pro práci údržby nebo na obor práce údržby vybrány dovednosti nebo certifikáty a v úloze pracovního příkazu je použit typ práce údržby nebo obor úloha údržby, jsou naplánováni pouze pracovníci s odpovídajícími dovednostmi a certifikáty na pracovní příkaz.

<a name="gantt"></a>

## <a name="work-with-scheduled-work-orders-using-a-gantt-chart"></a>Práce s plánovanými pracovními příkazy pomocí Ganttova diagramu

**Ganttův graf plánovaných pracovních objednávek** poskytuje grafické rozhraní, ve kterém můžete zobrazit a přeplánovat pracovní příkazy.

Postup při zobrazení a práci s Ganttovým grafem:

1. Přejděte na **Správa majetku > Pracovní příkazy > Ganttův graf plánovaných pracovních příkazů**.

1. Pomocí rozevíracích seznamů a polí v části **Nastavení** můžete nastavit, jaké funkční umístění, časové období a časové měřítko se mají zobrazit v Ganttově diagramu.

1. Zvolte **Použít**.

    - Aktualizace Ganttova diagramu pro zobrazení plánovaných pracovních příkazů odpovídajících zadaným nastavením. Každá pracovní objednávka je zastoupena modrým obdélníkem.
    - Chcete-li přeplánovat zobrazenou pracovní objednávku, vyberte položku a přetáhněte ji do příslušného nového data a času.

1. Pokud jste provedli změny, vyberte **Uložit** v podokně akcí a uložte je.

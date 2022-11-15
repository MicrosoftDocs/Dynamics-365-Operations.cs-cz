---
title: Plánování s omezenou kapacitou
description: Plánování s omezenou kapacitou vám pomůže pochopit, kolik práce lze udělat během určitého období, když se vezmou v úvahu omezení různých prostředků.
author: t-benebo
ms.date: 09/19/2022
ms.topic: article
ms.search.form: ReqParameters, ReqPlanSched, WrkCtrTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-09-19
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 5f02ec58c88cfd0d663a97de4e3e4dff1cdd5e90
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740079"
---
# <a name="finite-capacity-planning-and-scheduling"></a>Plánování s omezenou kapacitou

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!--KFM: Preview until 10.0.31 GA -->

Plánování s omezenou kapacitou je přístup, kterýv vám pomůže pochopit, kolik práce lze udělat během určitého období, když se vezmou v úvahu omezení různých prostředků. Účelem plánování s omezenou kapacitou je zajistit, aby práce probíhaly rovnoměrným a efektivním tempem v celém závodě.

Plánování s omezenou kapacitou vytváří realističtější plán výrobních procesů než plánování bez omezení. Pokud není dostatečná kapacita prostředků, datum dodání bude posunuto a úloha bude naplánována až na dobu s dostatečnou kapacitou.

> [!NOTE]
> Pokud používáte optimalizaci plánování, nebo zastaralý hlavní plánovací modul, plánování s omezenou kapacitou funguje téměř stejně. Optimalizace plánování však nepoužívá parametr **kritické ochranné doby**. Když používáte optimalizaci plánování, kritické prostředky jsou vždy naplánovány pomocí stejné ochranné doby jako nekritické prostředky (jak je označeno ochrannou dobou konečné kapacity).

## <a name="set-up-finite-capacity-functionality"></a>Nastavení funkce omezené kapacity

Chcete-li používat funkci omezené kapacity, musíte povolit globální plánování kapacity a také plánování omezené kapacity jak pro hlavní plán, kde jej chcete použít, tak pro každý prostředek, pro který má platit. U plánů a prostředků, pro které je povolena omezená kapacita, budou plánované výrobní zakázky brát v potaz již rezervovanou kapacitu. Plánované výrobní zakázky se plánují zpětně od požadovaného data. Pokud není k dispozici kapacita pro splnění optimálního plánu, systém se pokusí požadovat položky komponent k dřívějšímu datu. Pokud se vaše kapacita může změnit spolu se změnou požadavků (například používáte směny), neměli byste používat funkci omezené kapacity, protože vypočítané časy zpracování budou chybné. Plánování počítá pouze s kapacitou, která je již rezervována pro prostředky, pro které je povolena omezená kapacita. Povolením omezené kapacity pro prostředek umožníte změnit ochrannou dobu omezené kapacity.

### <a name="activate-master-planning-parameters"></a>Aktivace parametrů hlavního plánování

Chcete-li používat funkci omezené kapacity, musíte povolit plánování kapacity na stránce **Parametry hlavního plánování**.

1. Přejděte na **Hlavní plánování \> Nastavení \> Parametry hlavního plánování**.
1. Na kartě **Plánované zakázky** v sekci **Plánovaní kapacity** nastavte možnost **Výroba** na hodnotu *Ano*.

### <a name="activate-a-master-plan"></a>Aktivace hlavního plánu

Pro každý hlavní plán musíte povolit plánování s omezenou kapacitou tam, kde jej chcete používat.

1. Přejděte na **Hlavní plánování \> Nastavení \> Plány \> Hlavní plány**.
1. V podokně seznamu vyberte hlavní plán, který chcete nastavit na používání plánování s omezenou kapacitou.
1. Na pevné záložce **Obecné** v sekci **Plánované výrobní zakázky** nastavte možnost **Omezená kapacita** na hodnotu *Ano*.
1. Opakujte kroky 2 a 3 pro každý další hlavní plán, který chcete nastavit.

### <a name="activate-resources"></a>Aktivace prostředků

Pro každý prostředek musíte povolit plánování s omezenou kapacitou tam, kde jej chcete používat.

1. Přejděte na **Řízení výroby \> Nastavení \> Prostředky \> Prostředky**.
1. V podokně seznamu vyberte prostředek, který chcete nastavit na používání plánování s omezenou kapacitou.
1. Na pevné záložce **Operace** v části **Tlačítko Kapacita** nastavte možnost **Omezená kapacita** na *Ano*.
1. Opakujte kroky 2 a 3 pro každý další prostředek, který chcete nastavit.

## <a name="examples"></a>Příklad

Tato část obsahuje následující příklady, které ukazují, jak pracovat s plánováním s neomezenou i omezenou kapacitou:

- Příklad 1 – Plánování s neomezenou kapacitou
- Příklad 2 – Plánování s omezenou kapacitou a ochrannou dobou jednoho dne
- Příklad 3 – Plánování s omezenou kapacitou a ochrannou dobou dvou dní

### <a name="preconditions"></a>Předpoklady

Všechny tři příklady počítají s předpoklady popsané v této části.

Produkt *Produkt1* má cestu, která obsahuje následující operace.

| Č. operace | Název operace | Prostředek        | Operační čas | Zpracované množství | Další |
|---------------|----------------|-----------------|----------|--------------|------|
| 10            | Svařování        | Svařovací linka    | 1        | 2            | 20   |
| 20            | Sestavení     | Montážní linka | 1        | 4            |      |

Pracovníci ve vaší společnosti pracují v jedné směně po dobu osmi hodin (8:00–16:00).

Existuje plánovaná výrobní zakázka na *24 ks* pro *Produkt1*. Její datum doručení je *Dnes + 3 dny*.

V důsledku plánování systém načte prostředky následujícím způsobem:

- **Svařovací linka:** Tento prostředek je načten od *Dnes v 8:00* do *Dnes + 1 ve 12:00*.
- **Montážní linka:** Tento prostředek je načten od *Dnes + 1 ve 12:00* do *Dnes + 2 v 10:00*.

Následující obrázek ukazuje výsledný Ganttův diagram (jeho výběrem zvětšíte zobrazení).

[![Ganttův diagram zobrazující předpoklady.](media/finite-examples-conditions-small.png "Ganttův diagram zobrazující předpoklady")](media/finite-examples-conditions.png)

### <a name="example-1--infinite-capacity-planning"></a>Příklad 1 – Plánování s neomezenou kapacitou

Tento příklad ukazuje výsledky plánování, když místo plánování s omezenou kapacitou použijete plánování s neomezenou kapacitou.

Hlavní plán má následující relevantní nastavení, které deaktivuje plánování s omezenou kapacitou:

- **Omezená kapacita:** *Ne*

Možnost **Omezená kapacita** je také nastavena na *Ne* pro oba relevantní prostředky, abyste pro ně zakázali plánování s omezenou kapacitou:

- Svařovací linka
- Montážní linka

Nyní přidáte novou prodejní objednávku na *8 ks* pro *Produkt1* a spustíte plán. Výsledkem je, že systém načte svařovací linku od *Dnes v 8:00* do *Dnes ve 12:00*. Po dokončení operací na svařovací lince systém načte montážní linku od *Dnes ve 12:00* do *Dnes ve 14:00*.

Následující obrázek ukazuje výsledný Ganttův diagram (jeho výběrem zvětšíte zobrazení).

[![Ganttův diagram ukazující příklad plánování s neomezenou kapacitou.](media/finite-examples-example1-small.png "Ganttův diagram ukazující příklad plánování s neomezenou kapacitou")](media/finite-examples-example1.png)

### <a name="example-2--finite-capacity-planning-with-a-time-fence-of-one-day"></a>Příklad 2 – Plánování s omezenou kapacitou a ochrannou dobou jednoho dne

Tento příklad ukazuje výsledky plánování, když místo použijete plánování s omezenou kapacitou a ochrannou dobu jednoho dne.

Hlavní plán má následující relevantní nastavení, které povoluje plánování s omezenou kapacitou a nastaví ochrannou dobu:

- **Omezená kapacita:** *Ano*
- **Ochranná doba omezené kapacity:** *1*

Možnost **Omezená kapacita** je také nastavena na *Ano* pro oba relevantní prostředky, abyste pro ně povolili plánování s omezenou kapacitou:

- Svařovací linka
- Montážní linka

Nyní přidáte novou prodejní objednávku na *8 ks* pro *Produkt1* a spustíte plán. Výsledkem je, že systém načte svařovací linku od *Dnes + 1 v 8:00* do *Dnes + 1 ve 12:00*. Po dokončení operací na svařovací lince systém načte montážní linku od *Dnes + 1 ve 12:00* do *Dnes + 1 ve 14:00*. Systém bere v úvahu omezenou kapacitu pouze na jeden den.

Následující obrázek ukazuje výsledný Ganttův diagram (jeho výběrem zvětšíte zobrazení).

[![Ganttův diagram ukazující plánování s omezenou kapacitou a ochrannou dobou jednoho dne.](media/finite-examples-example2-small.png "Ganttův diagram ukazující plánování s omezenou kapacitou a ochrannou dobou jednoho dne")](media/finite-examples-example2.png)

### <a name="example-3--finite-capacity-planning-with-a-time-fence-of-two-days"></a>Příklad 3 – Plánování s omezenou kapacitou a ochrannou dobou dvou dní

Tento příklad ukazuje výsledky plánování, když místo použijete plánování s omezenou kapacitou a ochrannou dobu dvou dní.

Hlavní plán má následující relevantní nastavení, které povoluje plánování s omezenou kapacitou a nastaví ochrannou dobu:

- **Omezená kapacita:** *Ano*
- **Ochranná doba omezené kapacity:** *2*

Možnost **Omezená kapacita** je také nastavena na *Ano* pro oba relevantní prostředky, abyste pro ně povolili plánování s omezenou kapacitou:

- Svařovací linka
- Montážní linka

Nyní přidáte novou prodejní objednávku na *8 ks* pro *Produkt1* a spustíte plán. Výsledkem je, že systém načte svařovací linku od *Dnes + 1 v 12:00* do *Dnes + 1 ve 16:00*. Po dokončení operací na svařovací lince systém načte montážní linku od *Dnes + 2 ve 8:00* do *Dnes + 2 ve 10:00*. Systém bere v úvahu omezenou kapacitu pouze na dva dny.

Následující obrázek ukazuje výsledný Ganttův diagram (jeho výběrem zvětšíte zobrazení).

[![Ganttův diagram ukazující plánování s omezenou kapacitou a ochrannou dobou dvou dní.](media/finite-examples-example3-small.png "Ganttův diagram ukazující plánování s omezenou kapacitou a ochrannou dobou dvou dní")](media/finite-examples-example3.png)

> [!IMPORTANT]
> Ochrannou dobu omezené kapacity byste vždy měli nastavit podle vašich obchodních potřeb. Příklady uvedené v tomto článku pouze ukazují možnosti funkce. Ve skutečnosti je jednodenní ochranná doba pravděpodobně příliš krátká pro většinu výrobců, kteří používají plánování s omezenou kapacitou.

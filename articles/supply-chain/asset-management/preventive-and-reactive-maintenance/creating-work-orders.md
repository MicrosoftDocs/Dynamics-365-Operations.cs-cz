---
title: Vytvoření pracovních příkazů
description: Toto téma vysvětluje, jak vytvořit pracovní příkazy v modulu Správa majetku.
author: johanhoffmann
ms.date: 02/01/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetMaintenancePlan, EntAssetObjectCalendarListPage, EntAssetObjectCalendarListPagePoolsOpen
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 3982232e5008d6f8c283d6cecfaf2fa6e66150a1
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836727"
---
# <a name="creating-work-orders"></a>Vytvoření pracovních příkazů

[!include [banner](../../includes/banner.md)]

Po naplánování úloh preventivní údržby pro ně můžete v dalším kroku vytvořit pracovní příkazy. Tento krok můžete dokončit pomocí jednoho z plánů údržby. Naplánované práce v rozvrhu údržby mohou mít různé typy odkazů, jak popisuje následující tabulka:

| Typ odkazu | popis |
|---|---|
| Plány údržby | Práce preventivní údržby na základě typů plánu údržby *Čas* nebo *Počítadlo*. |
| Pořadí údržby | Práce preventivní údržby obsahující několik majetků, které vyžadují podobný typ údržby. |
| Požadavek na údržbu | Ručně vytvořený požadavek na údržbu nebo opravu majetku. Tento požadavek lze převést na pracovní příkaz. |

## <a name="create-work-orders-based-on-your-maintenance-schedule"></a>Vytvoření pracovních příkazů na základě plánu údržby

Chcete-li vytvořit pracovní příkazy, které jsou založeny na vašem plánu údržby, postupujte takto.

1. Otevřete jednu z následujících stránek podle toho, jak chcete vybrat položky plánu pro své pracovní příkazy:

    - Všechen rozvrh údržby (**Správa majetku \> Rozvrh údržby \> Všechen rozvrh údržby**)
    - Otevřít řádky rozvrhu údržby (**Správa majetku \> Rozvrh údržby \> Otevřít řádky rozvrhu údržby**)
    - Otevřít fondy rozvrhu údržby (**Správa majetku \> Rozvrh údržby \> Otevřít fondy rozvrhu údržby**)

1. V mřížce zaškrtněte políčko u každé úlohy plánované údržby, pro kterou chcete vytvořit pracovní příkaz. Pak v podokně akcí vyberte možnost **Pracovní příkaz**.

    Otevře se dialogové okno **Vytvořit pracovní příkazy**. V poli **Hodiny prognózy údržby** se zobrazí celkový počet hodin prognózy pro vybrané řádky.

    ![Dialogové okno Vytvořit pracovní příkazy](media/18-preventive-maintenance.png)

1. V části **Parametry** zadejte počet pracovních příkazů, které mají být vytvořeny. Vyberte některou z následujících možností:

    - **Jeden pracovní příkaz na řádek** - Vytvořte jeden pracovní příkaz na řádek plánu údržby.
    - **Jeden pracovní příkaz na** - Vytvářejte pracovní příkazy, které jsou seskupeny podle nastavení ostatních možností, které budou k dispozici, když vyberete tuto možnost.

1. V poli **Typ pracovního příkazu** vyberte typ pracovního příkazu, který se má použít pro všechny pracovní příkazy, které vytvoříte.
1. Vyberte **OK** k vytvoření pracovních příkazů podle vašeho nastavení.

## <a name="group-work-order-lines-that-are-automatically-created-while-a-maintenance-plan-runs"></a>Seskupte řádky pracovních příkazů, které se automaticky vytvářejí, když běží plán údržby

Tato funkce umožňuje definovat pravidla pro seskupování řádků pracovních příkazů do jednoho pracovního příkazu, když je systém nastaven na automatické generování pracovních příkazů na základě plánu údržby. Dříve mohly automaticky generované pracovní příkazy obsahovat pouze jeden řádek. Nyní však můžete pracovní příkazy seskupovat například podle majetku, typu majetku nebo funkčního umístění. (Ručně generované pracovní příkazy již lze tímto způsobem seskupit, jak je popsáno v předchozí části tohoto tématu.)

### <a name="enable-grouping-for-automatically-generated-work-orders"></a>Povolení seskupování pro automaticky generované pracovní příkazy

Než můžete použít tuto funkci, musíte ji zapnout ve svém systému. Správci mohou pomocí nastavení [správa funkcí](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) zkontrolovat stav funkce a zapnout ji. V pracovním prostoru **Správa funkcí** je tato funkce uvedena následovně:

- **Modul:** *Správa majetku*
- **Název funkce:** *Použít pravidla pro seskupování pracovních příkazů při provádění plánu údržby*

### <a name="set-up-grouping-for-automatically-generated-work-orders"></a>Nastavení seskupování pro automaticky generované pracovní příkazy

Při nastavení seskupování pro automaticky generované pracovní příkazy postupujte následovně.

1. Klikněte na **Správa majetku \> Nastavení \> Preventivní údržba \> Plány údržby**.
1. U každého plánu, kde chcete generovat seskupené pracovní příkazy, postupujte takto:

    1. V podokně seznamu vyberte plán.
    1. Na záložce s náhledem **Řádky** se ujistěte, že je na každém řádku zaškrtnuto políčko **Automaticky vytvořit**.

1. Přejděte na **Správa majetku \> Periodické \> Preventivní údržba \> Rozvrhnout plány údržby**.
1. V dialogovém okně **Naplánovat rozvrhy údržby** v části **Období** určete časový horizont plánu (jak daleko se dívat dopředu při hledání úloh plánované údržby, pro které se má generovat práce).
1. Nastavte možnost **Automaticky vytvořit pracovní příkaz podle plánu** na *Ano*.
1. V oddílu **pracovní příkaz** vyberte některou z následujících možností:

    - **Jeden pracovní příkaz na řádek** - Vytvořte jeden pracovní příkaz na řádek plánu údržby. (Tato možnost poskytuje stejnou funkcionalitu, která je k dispozici, když je vypnutá funkce *Použít pravidla pro seskupování pracovních příkazů při provádění plánu údržby*.)
    - **Jeden pracovní příkaz na** - Vytvářejte pracovní příkazy, které jsou seskupeny podle nastavení ostatních možností, které budou k dispozici, když vyberete tuto možnost.

1. Pokud chcete, aby se možnosti uplatnily při spuštění pouze některých vašich plánů údržby, na kartě s náhledem **Záznamy, které mají být zahrnuty**, přidejte filtry podle potřeby, stejně jako to můžete udělat pro jiné dávkové úlohy v Microsoft Dynamics 365 Supply Chain Management.
1. Na kartě s náhledem **Spustit na pozadí** nastavte dávkové a plánovací možnosti, jak požadujete, stejně jako u jiných dávkových úloh v Supply Chain Management.
1. Výběrem **OK** spusťte a/nebo naplánujte vybrané plány údržby.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
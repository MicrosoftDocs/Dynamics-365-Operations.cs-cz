---
title: Rozšiřitelnost optimalizace plánování
description: Tento článek popisuje scénáře rozšiřitelnosti, které jsou podporovány optimalizací plánování.
author: t-benebo
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: benebotg
ms.search.validFrom: 2020-07-07
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 7d649110959e6bcfdaeb32dd53c55dbc446ed1be
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8857537"
---
# <a name="planning-optimization-extensibility"></a>Rozšiřitelnost optimalizace plánování

[!include [banner](../../includes/banner.md)]

Tento článek popisuje scénáře rozšiřitelnosti, které souvisí s hlavním plánováním a jsou podporovány optimalizací plánování. Tyto funkce jsou k dispozici od verze Microsoft Dynamics 365 Supply Chain Management 10.0.13.

## <a name="custom-processing-when-master-planning-is-completed"></a>Vlastní zpracování po dokončení hlavního plánování

V nejběžnějším scénáři rozšiřitelnosti v optimalizaci plánování se vlastní zpracování provádí po aktualizaci plánu. Můžete například přidat sloupec do tabulky plánovaných objednávek (`ReqPO`), nebo můžete chtít odvodit nějaké statistické informace z vygenerovaného plánu. Hlavním bodem rozšiřitelnosti, který umožňuje tyto scénáře, je metoda `jobCompletedSuccessfully` ve třídě `MpsMasterPlanningEvents`.

```X++
public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
```

Zde je příklad rozšíření, které nastavuje vlastní pole `CstmOrderPriority` na plánované zakázce.

```X++
[ExtensionOf(classStr(MpsMasterPlanningEvents))]
public static final class MpsMasterPlanningEvents_Cstm_Extension
{
    public static void jobCompletedSuccessfully(MpsMasterPlanningJobCompletedSuccessfullyEventArgs _args)
    {
        ttsbegin;

        var affectedPlannedOrdersQuery = _args.parmPostProcessingQueryBuilder().buildAffectedPlannedOrdersQuery();
        var affectedPlannedOrdersQueryRun = new QueryRun(affectedPlannedOrdersQuery);

        while (affectedPlannedOrdersQueryRun.next())
        {
            ReqPO reqPO = affectedPlannedOrdersQueryRun.get(tableNum(ReqPO));
            reqPO.selectForUpdate(true);
            reqPO.CstmOrderPriority = reqPO.ReqDate - systemDateGet() < 7 ? CstmPlannedOrderPriority::Urgent : CstmPlannedOrderPriority::Regular;
            reqPO.doUpdate();
        }

        ttscommit;

        next jobCompletedSuccessfully(_args);
    }

}
```

Při přidávání vlastní logiky zvažte následující omezení a doporučené postupy:

- Metoda `jobCompletedSuccessfully` je volána mimo rozsah transakce. Proto je plán již viditelný pro uživatele, když se spustí vlastní logika. Pokud vaše přizpůsobení nastavuje další pole u plánovaných objednávek, je důležité, abyste uživatelům sdělili, že hodnoty těchto polí budou nakonec konzistentní (jinými slovy, mohou být zastaralé ihned po dokončení plánovací úlohy).
- Další hlavní plánovací práce může začít, když je volána metoda `jobCompletedSuccessfully`. Nová úloha může ovlivnit celý plán nebo část plánu. Nová úloha může aktualizovat nebo odstranit stejné plánované objednávky nebo transakce požadavků, které byly vytvořeny nebo aktualizovány jako součást plánovací úlohy, která byla zpracována v `jobCompletedSuccessfully`. Při prodloužení této události musí být zpracovány výjimky z konfliktu aktualizací.
- Při rozšíření této metody se vyvarujte použití jednoho rozsahu transakce. Jediný běh hlavního plánování může vyprodukovat miliony transakcí požadavků a stovky tisíc plánovaných objednávek. Pokud jsou všechny tyto transakce a plánované objednávky zpracovány v rámci jediné transakce, dojde k mnoha zaseknutí SQL a zablokování dalších plánovacích procesů. Navíc, pokud je transakce držena po dlouhou dobu, budou v SQL databázi vytvořeny „falešné záznamy“. Falešné záznamy negativně ovlivní každý proces v systému.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
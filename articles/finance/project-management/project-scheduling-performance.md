---
title: Výkon plánování prostředků projektů
description: Tohle téma poskytuje informace, jak zlepšit výkon plánování prostředků u velkého počtu projektů.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760499"
---
# <a name="project-resource-scheduling-performance"></a>Výkon plánování prostředků projektů

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Problémy s výkonem související s plánováním prostředků mohou nastat, když počet projektů dosáhne tisíců. K vylepšení výkonu plánování prostředků je k dispozici funkce, která uživatelům umožňuje zkrátit čas potřebný ke spuštění formuláře dostupnosti prostředků. Konkrétně odebere proces synchronizace pro shrnutí kapacity prostředků a použije tabulku **ResProjectResource** k urychlení vyhledávání prostředků. Všimněte si, že tabulka **ResRollup** již nebude použita.

> [!IMPORTANT]
> Pokud existuje závislost buď na procesu synchronizace pro shrutí kapacity prostředků, nebo na tabulce **ResProjectResource**, nepoužívejte tuto funkci.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Povolení zvýšení výkonnosti plánování prostředků
Chcete-li povolit vylepšení výkonnosti plánování prostředků, proveďte následující kroky.

1. Přejděte na **Správa funkcí** > **Vše** a v seznamu funkcí vyhledejte **Povolit funkci vylepšení výkonosti plánování prostředků projektu**.
2. Vyberte **Povolit**.

> [!NOTE]
> Pokud nemůžete najít funkci v seznamu, volbou **Zkontrolovat aktualizace** aktualizujte seznam.

3. Aktualizujte prohlížeč a poté přejděte na **Řízení a účetnictví projektu** > **Periodické** > **Prostředky projektu** > **Synchronizovat kapacitu kalendářů prostředků ve všech společnostech**.
4. Nastavením **Odebrat existující záznamy o kapacitě** na **Ano** odstraníte předchozí data. Pokud chcete generovat přírůstková data, nastavte tuto volbu na **Ne**.
5. V poli **Kód období** vyberte období, ve kterém mají být data generována. Pokud vyberete kód období, není nutné definovat počáteční a koncové datum.
6. Pokud ponecháte pole **Kód období** prázdné, vyberte konkrétní počáteční a koncové datum pro generování dat.
7. Vyberte **OK**.

 > [!NOTE]
 > Dojde k distribuci obecných dat do tabulky **ResCalendarCapacity** napříč všemi společnostmi ve vašem prostředí, takže dávkovou úlohu je třeba spustit pouze v jedné právnické osobě. Data v této dávkové úloze jsou potřebná k výpočtu kapacity prostředků prostřednictvím přidruženého kalendáře.

8. Přejděte na **Řízení a účetnictví projektu** > **Periodické** > **Prostředky projektu** > **Naplnit prostředky projektu ve všech společnostech** a poté vyberte **OK**. Toto je skript pro aktualizaci dat pro obecná data v tabulkách **ResProjectResource**, **ResCalendarDateTimeRange** a **ResEffectiveDateTimeRange**. Hodnoty pro pole **PSAPRojSchedRole.RootActivity** se také aktualizují. Pokud to není spuštěno, obdržíte varování, když se pokusíte provést operace plánování prostředků.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Zapnutí zvýšení výkonnosti plánování prostředků

1. Přejděte na **Správa funkcí** > **Vše** a hledejte **Povolit funkci vylepšení výkonosti plánování prostředků projektu**.
2. Vyberte funkci a poté vyberte tlačítko **Zakázat**.
3. Aktualizujte svůj prohlížeč.
4. Přejděte na **Řízení a účetnictví projektů** > **Periodicky** > **Synchronizace kapacity** > **Synchronizace shrnutí kapacity pro prostředek**.
5. Na stránce **Synchronizace shrnutí kapacity** nastavením **Odebrat existující záznamy o kapacitě** na **Ano** odstraníte předchozí data. Pokud chcete generovat přírůstková data, nastavte tuto volbu na **Ne**.
6. V poli **Kód období** vyberte období, ve kterém mají být data generována. Pokud vyberete kód období, není nutné definovat počáteční a koncové datum.
7. Pokud ponecháte pole **Kód období** prázdné, vyberte konkrétní počáteční a koncové datum pro generování dat.
8. Vyberte **OK**.

> [!NOTE]
> Dojde k distribuci obecných dat do tabulky **ResRollup** napříč všemi společnostmi ve vašem prostředí, takže dávkovou úlohu je třeba spustit pouze v jedné právnické osobě. Tato dávková úloha je nutná pro všechn zobrazení **Dostupnost prostředků**. Pokud tato dávková úloha není spuštěna, data **ResRollup** budou generována za chodu, což může chvíli trvat.

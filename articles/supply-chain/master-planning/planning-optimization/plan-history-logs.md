---
title: Zobrazení historie plánu a protokolů plánování
description: Toto téma vysvětluje, jak zobrazit historii úloh plánování, které jsou spouštěny funkcí Optimalizace plánování.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 93e8f933524b34116987c9e0d91d226e21d98f4d
ms.sourcegitcommit: 5c9a5bfef507ed36f0f849ab56fa0aa8abb78d54
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/20/2021
ms.locfileid: "6646480"
---
# <a name="view-plan-history-and-planning-logs"></a>Zobrazení historie plánu a protokolů plánování

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak zobrazit historii úloh plánování, které jsou spouštěny funkcí Optimalizace plánování v aplikaci Microsoft Dynamics 365 Supply Chain Management.

Chcete-li zobrazit historii plánu, otevřete plán tak, že přejdete na **Hlavní plánování** \> **Nastavení** \> **Plány** \> **Hlavní plány** a vyberete **Historie**. V rámci historie jsou uvedeny všechny úlohy pro vybraný plán. Seznam obsahuje dokončené a aktivní úlohy.

Historie úloh pro hlavní plánovací běhy Optimalizace plánování udržuje maximálně 60 záznamů na hlavní plán. Kdykoli spustíte nový výpočet hlavního plánování, bude odstraněn nejstarší záznam historie tohoto plánu.

Kromě toho, že se zobrazuje počáteční čas a stav úloh, můžete zobrazit protokol pro určitou práci. Protokol obsahuje další informace a upozornění. Některé úlohy nemají protokol. Chcete-li zobrazit protokol pro úlohu, vyberte možnost **protokol**. Položky protokolu se ukládají po dobu pouze 30 dní po datu dokončení úlohy, poté se automaticky smažou.

Pokud byla povolena možnost **Dávkové zpracování** na pevné záložce **Spustit na pozadí**, když bylo nastaveno zpracování hlavního plánování, protokol dávkové úlohy zobrazuje více informací o všech varováních a chybách, které byly vygenerovány během běhu hlavního plánování. Například chyby automatického spouštění jsou zachyceny pouze v protokolu dávkové úlohy. Nejsou zobrazeny v protokolech na stránce **Historie**.

Chcete-li zobrazit chyby automatického spouštění a další varování nebo chyby, které se vyskytly během běhu hlavního plánování, postupujte takto.

1. Přejděte na **Správa systému \> Dotazy \> Dávkové úlohy**.
1. Najděte a vyberte záznam, který představuje hlavní plánovací běh, o který se zajímáte. (Například hodnota pole **Popis práce** může začínat *Hlavní plánování*.)
1. Postupujte podle jednoho z těchto kroků podle toho, zda používáte *vylepšený formulář* nebo *starší (nevylepšený) formulář* pro stránku **Dávkové úlohy**:

    - Pokud používáte vylepšený formulář: V podokně akcí vyberte **Historie dávkových úloh**. Pak na stránce **Historie dávkových úloh**, v podokně akcí vyberte **Protokol**.
    - Pokud používáte starší formulář: V podokně akcí na kartě **Dávková úloha** vyberte **Protokol**.

1. Vyberte **Podrobnosti zprávy**, chcete-li otevřít podokno **Podrobnosti zprávy**, kde můžete zobrazit všechna varování a chyby, které byly zachyceny během zpracování.

## <a name="related-resources"></a>Související prostředky

- [Přehled optimalizace plánování](planning-optimization-overview.md)
- [Začínáme s optimalizací plánování](get-started.md)
- [Analýza přizpůsobení pro optimalizaci plánování](planning-optimization-fit-analysis.md)
- [Použití filtrů v plánu](plan-filters.md)
- [Zrušení úlohy plánování](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

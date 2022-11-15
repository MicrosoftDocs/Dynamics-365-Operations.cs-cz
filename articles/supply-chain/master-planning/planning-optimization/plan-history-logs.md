---
title: Zobrazení historie plánu a protokolů plánování
description: Tento článek vysvětluje, jak zobrazit historii plánování úloh.
author: t-benebo
ms.date: 06/01/2020
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
ms.author: benebotg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: ab469686a009364bf53cb963506fd2107075a283
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/03/2022
ms.locfileid: "9740924"
---
# <a name="view-plan-history-and-planning-logs"></a>Zobrazení historie plánu a protokolů plánování

[!include [banner](../../includes/banner.md)]

Tento článek vysvětluje, jak zobrazit historii plánování úloh v Microsoft Dynamics 365 Supply Chain Management.

Chcete-li zobrazit historii plánu, otevřete plán tak, že přejdete na **Hlavní plánování** \> **Nastavení** \> **Plány** \> **Hlavní plány** a vyberete **Historie**. V rámci historie jsou uvedeny všechny úlohy pro vybraný plán. Seznam obsahuje dokončené a aktivní úlohy.

Systém uchovává maximálně 60 záznamů historie na hlavní plán a maže záznamy starší 30 dnů. Pokaždé, když spustíte nový výpočet hlavního plánování, systém přidá nový záznam historie a poté podle potřeby vyčistí nejstarší záznamy.

Kromě toho, že se zobrazuje počáteční čas a stav úloh, můžete zobrazit protokol pro určitou práci. Protokol obsahuje další informace a upozornění. Některé úlohy nemají protokol. Chcete-li zobrazit protokol pro úlohu, vyberte možnost **protokol**. Položky protokolu se ukládají po dobu pouze 30 dní po datu dokončení úlohy, poté se automaticky smažou.

Pokud byla povolena možnost **Dávkové zpracování** na pevné záložce **Spustit na pozadí**, když bylo nastaveno zpracování hlavního plánování, protokol dávkové úlohy zobrazuje více informací o všech varováních a chybách, které byly vygenerovány během běhu hlavního plánování. Například chyby automatického spouštění jsou zachyceny pouze v protokolu dávkové úlohy. Nejsou zobrazeny v protokolech na stránce **Historie**.

Chcete-li zobrazit chyby automatického spouštění a další varování nebo chyby, které se vyskytly během běhu hlavního plánování, postupujte takto.

1. Přejděte na **Správa systému \> Dotazy \> Dávkové úlohy**.
1. Najděte a vyberte záznam, který představuje hlavní plánovací běh, o který se zajímáte. (Například hodnota pole **Popis práce** může začínat *Hlavní plánování*.)
1. Postupujte podle jednoho z těchto kroků podle toho, zda používáte *vylepšený formulář* nebo *starší (nevylepšený) formulář* pro stránku **Dávkové úlohy**:

    - Pokud používáte vylepšený formulář: V podokně akcí vyberte **Historie dávkových úloh**. Pak na stránce **Historie dávkových úloh**, v podokně akcí vyberte **Protokol**.
    - Pokud používáte starší formulář: V podokně akcí na kartě **Dávková úloha** vyberte **Protokol**.

1. Vyberte **Podrobnosti zprávy**, chcete-li otevřít podokno **Podrobnosti zprávy**, kde můžete zobrazit všechna varování a chyby, které byly zachyceny během zpracování.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

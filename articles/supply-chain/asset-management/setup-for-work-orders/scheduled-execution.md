---
title: Plánované provedení
description: Tohle téma popisuje plánované provedení v modulu Správa majetku.
author: johanhoffmann
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f49ae2a65bf590eea13265712621675da87dd621
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/06/2021
ms.locfileid: "6360070"
---
# <a name="scheduled-execution"></a>Plánované provedení

[!include [banner](../../includes/banner.md)]

 

Úrovně služeb pracovního příkazu lze použít k nastavení plánovaného provedení. (Další informace o úrovních služeb pracovního příkazu naleznete v tématu [Úroveň služby a popis](service-level-and-description.md).) Naplánované provádění poskytuje flexibilitu v plánování práce pro pracovníky údržby, protože lze nastavit podrobnější nebo méně podrobné požadavky pro interval, po který má být pracovní příkaz dokončen. Například pracovníka údržby, který dokončuje úlohu rychleji než je očekáváno ve výrobním zařízení, může přejít k jiné blízké úloze, která byla naplánována pro aktuální týden, ale ne nutně pro aktuální den. Tento přístup umožňuje optimalizaci plánování pracovníků a dokončení úlohy.

Plánovaná úloha nastavení, která souvisí s pracovními příkazy, může být obecná nebo specifická. Můžete nastavit obecné řádky, které nejsou omezeny na specifické typy pracovních objednávek, typy majetku a tak dále. Případně můžete vytvořit naplánované řádky provedení, které se vztahují na určitý typ pracovního příkazu, typ majetku, typ úlohy údržby atd.

1. Vyberte **Správa majetku** \> **Nastavení** \> **Pracovní příkazy** \> **Plánované provedení**.
2. Vybere **Nový** k vytvoření řádku plánovaného provedení.
3. V polích **Funkční umístění**, **Typ pracovního příkazu**, **Typ majetku**, **Výrobce**, **Model**, **Kategorie typu úlohy údržby**, **Typ úlohy údržby**, **Varianta typu úlohy údržby** a **Obchod** vyberte hodnoty podle potřeby.
4. V vyberte úroveň služeb pracovního příkazu v poli **Úroveň služeb**. Pokud toto pole ponecháte prázdné, provedete nejobecnější typ řádku plánovaného provedení. Příklad obecného řádku naleznete v prvním záznamu na následujícím obrázku. Tento řádek umožňuje naplánovat všechny pracovní příkazy, které nemají žádnou úroveň služby pracovního příkazu pro určité datum a čas.
5. V poli **Plánované provedení** vyberte časový interval.
6. Zvolte možnost **Uložit**.

![Plánované provedení.](media/20-setup-for-work-orders.png)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
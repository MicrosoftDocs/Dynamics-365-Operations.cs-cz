---
title: Postupné vytváření objednávek pro maloobchodní transakce
description: V tomto tématu je popsáno postupné vytváření objednávek pro transakce obchodu v Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7d5812893edff24a60a0e2eb3607701ac47a8a78
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057137"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions-public-preview"></a>Postupné vytváření objednávek pro maloobchodní transakce (Public preview)

[!include [banner](includes/banner.md)]

V aplikaci Dynamics 365 Retail verze 10.0.4 a starších je zaúčtování výkazů operací na konci dne a všechny transakce jsou zaúčtovány do knih až na konci dne. Rozsáhlé transakce tak musí být zpracovány v omezeném časovém úseku, což má někdy za následek vytížení a uzamčení a selhání zaúčtování výkazů. Maloobchodní prodejci také nemohou uznat výnosy a platby ve svých knihách v průběhu dne.

Ve verzi Public Preview se díky postupnému vytváření objednávek, funkci představené ve verzi 10.0.5 aplikace Retails, transakce zpracovávají po celý den a na konci dne se zpracovávají pouze finanční odsouhlasení úhrad a jiné transakce řízení hotovosti. Tato funkce rozdělí vytížení vytváření prodejních objednávek, faktur a plateb na celý den a poskytuje lepší vnímaný výkon a schopnost uznat výnosy a platby v knihách v téměř reálném čase. 


## <a name="how-to-use-trickle-feed-based-posting"></a>Jak používat postupné účtování
  
1. Chcete-li povolit postupné účtování transakcí, přejděte na **Správa systému > Nastavení > Konfigurace licence** a zakažte klíč **Výkazy**.

2. Na stejné stránce povolte licenční klíč **Výkazy (postupné) – Preview**. Když povolíte tento klíč, ujistěte se, že neexistují žádné nevyřízené výkazy čekající na zaúčtování. 

    > [!Important]
    > Před povolením licenčního klíče **Výkazy (postupné) – Preview** se ujistěte, že neexistují žádné nevyřízené výkazy čekající na zaúčtování.

3. Aktuální dokument výkazu bude rozdělen na dva různé typy. transakční výkaz a finanční výkaz.

      - Transakční výkaz vybere všechny nezaúčtované a ověřené transakce a bude vytvářet prodejní objednávky, prodejní faktury, deníky slev a plateb a transakce příjmů a výdajů ve frekvenci, kterou nakonfigurujete. Tento proces byste měli nakonfigurovat ke spouštění v časté frekvenci, aby dokumenty byly vytvářeny při odesílání transakcí do centrály prostřednictvím úlohy P. U transakčního výkazu, který již vytváří prodejní objednávky a prodejní faktury, není třeba konfigurovat dávkovou úlohu **Zaúčtovat zásoby**. Lze ji však stále použít k uspokojení specifických obchodních požadavků, které můžete mít.  
      
     - Finanční výkaz je určen k tomu, aby byl vytvořen na konci dne, a podporuje pouze metodu uzávěrky **Směna**. Tento výkaz bude omezen na finanční odsouhlasení a bude vytvářet pouze deníky pro rozdílné částky mezi spočtenou částkou a částkou transakce pro různé úhrady, společně s deníky pro ostatní transakce řízení hotovosti.   

4. Chcete-li vypočítat transakční výkaz, klikněte na **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Vypočítat transakční výkazy v dávce**. Chcete-li zaúčtovat transakční výkazy v dávce, klikněte na **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Zaúčtovat transakční výkazy v dávce**.

5. Chcete-li vypočítat finanční výkaz, klikněte na **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Vypočítat finanční výkazy v dávce**. Chcete-li zaúčtovat finanční výkazy v dávce, klikněte na **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Zaúčtovat finanční výkazy v dávce**.

> [!NOTE]
> Položky nabídky **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Vypočítat výkazy v dávce** a **Retail a Commerce > IT pro Retail a Commerce > Zaúčtování POS > Zaúčtovat výkazy v dávce** jsou s touto novou funkcí odebrány.

Typy transakčních a finančních výkazů lze alternativně vytvořit ručně. Přejděte na **Retail a Commerce > Kanály > Obchody** a klikněte na **Výkazy**. Klikněte na **Nový** a pak zvolte typ výkazu, který chcete vytvořit. Pole na stránce **Výkazy** a akce pod položkou **Skupina výkazů** této stránky zobrazí relevantní data a akce založené na vybraném typu výkazu.

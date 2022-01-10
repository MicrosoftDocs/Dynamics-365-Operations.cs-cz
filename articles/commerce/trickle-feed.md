---
title: Postupné vytváření objednávek pro maloobchodní transakce
description: V tomto tématu je popsáno postupné vytváření objednávek pro transakce obchodu v Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 12/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: ''
ms.openlocfilehash: 3a7fd8698d7123403cf9092a4a4bf810595d795b
ms.sourcegitcommit: f82372b1e9bf67d055fd265b68ee6d0d2f10d533
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/14/2021
ms.locfileid: "7921231"
---
# <a name="trickle-feed-based-order-creation-for-retail-store-transactions"></a>Postupné vytváření objednávek pro maloobchodní transakce

[!include [banner](includes/banner.md)]

V Microsoft Dynamics 365 Commerce verzi 10.0.5 a novější doporučujeme, abyste převedli všechny procesy účtování výkazů na procesy postupného účtování výkazů. S používáním funkce postupného účtování jsou spojeny významný výkon a obchodní výhody. Prodejní transakce jsou zpracovávány po celý den. Transakce odvodu úhrad a řízení hotovosti jsou zpracovány ve finančním výkazu na konci dne. Funkce postupného účtování umožňuje nepřetržité zpracování prodejních objednávek, faktur a plateb. Proto lze zásoby, výnosy a platby aktualizovat a rozpoznat téměř v reálném čase.

## <a name="use-trickle-feed-based-posting"></a>Používání postupného účtování

> [!IMPORTANT]
> Než povolíte postupné účtování, musíte se ujistit, že neexistují žádné vypočítané a nezaúčtované výkazy. Před aktivací funkce zaúčtujte všechny výkazy. Otevřené výkazy můžete zkontrolovat v pracovním prostoru **Finance obchodu**.

Chcete-li povolit postupné účtování maloobchodních transakcí, povolte funkci s názvem **Maloobchodní výkazy – Postupné účtování** v pracovním prostoru **Správa funkce**. Výkazy budou rozděleny na dva typy: transakční a finanční.

### <a name="transactional-statements"></a>Transakční výkazy

Zpracování transakčního výkazu by mělo být během dne spouštěno v časté frekvenci, aby dokumenty byly vytvářeny při načítání transakcí do centrály aplikace Commerce. Transakce se načítají z obchodů do centrály Commerce při spuštění **úlohy P**. Musíte také spustit úlohu **Ověřit transakce obchodu** a ověřit transakce, aby je transakční výkaz vyzvedl.

Naplánujte spouštění následujících úloh s vysokou frekvencí:

- Chcete-li vypočítat transakční výkaz, spusťte úlohu **Vypočítat transakční výkazy v dávce** (**Retail a Commerce \> Retail a Commerce IT \> Zaúčtování POS \> Vypočítat transakční výkazy v dávce**). Tato úloha vyzvedne všechny nezaúčtované a ověřené transakce a přidá je do nového transakčního výkazu.
- Chcete-li zaúčtovat transakční výkazy v dávce, spusťte úlohu **Zaúčtovat transakční výkazy v dávce** (**Retail a Commerce \> Retail a Commerce IT \> Zaúčtování POS \> Zaúčtovat transakční výkazy v dávce**). Tato úloha spustí proces účtování a vytvoří prodejní objednávky, prodejní faktury, deníky plateb, deníky slev a transakce příjmů a výdajů pro nezaúčtované výkazy, které neobsahují žádné chyby. 

### <a name="financial-statements"></a>Finanční výkazy

Zpracování finančního výkazu má být konečným procesem. Tento typ zpracování výkazů podporuje pouze způsob Uzavírání **směn** a vyzvedne pouze uzavřené směny. Výkazy jsou omezeny na finanční odsouhlasení. Vytvoří pouze deníky pro rozdílné částky mezi spočtenou částkou a částkou transakce pro různé úhrady, společně s deníky pro ostatní transakce řízení hotovosti.

Naplánujte čas zahájení a ukončení následujících úloh finančního výkazu na základě očekávaného konce dne:

- Chcete-li vypočítat finanční výkaz, spusťte úlohu **Vypočítat finanční výkazy v dávce** (**Retail a Commerce \> Retail a Commerce IT \> Zaúčtování POS \> Vypočítat finanční výkazy v dávce**). Tato úloha shromáždí všechny nezaúčtované finanční transakce a přidá je do nového finančního výkazu.
- Chcete-li zaúčtovat finanční výkazy v dávce, spusťte úlohu **Zaúčtovat finanční výkazy v dávce** (**Retail a Commerce \> Retail a Commerce IT \> Zaúčtování POS \> Zaúčtovat finanční výkazy v dávce**).

### <a name="manually-create-statements"></a>Ruční vytváření výkazů

Typy transakčních a finančních výkazů lze také vytvořit ručně. 

1. Přejděte na **Retail a Commerce \> Kanály \> Obchody**, a vyberte **Výkazy**. 
2. Vyberte **Nový** a poté vyberte typ výkazu, který chcete vytvořit. Pole na stránce **Výkazy** zobrazí data relevantní k vybranému typu výkazu a akce pod položkou **Skupina výkazů** zobrazí relevantní akce.

[!INCLUDE[footer-include](../includes/footer-banner.md)]

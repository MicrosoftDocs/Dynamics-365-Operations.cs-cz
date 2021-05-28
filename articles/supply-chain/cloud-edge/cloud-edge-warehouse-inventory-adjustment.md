---
title: Úprava skladových zásob
description: Toto téma poskytuje informace o deníku úprav skladu a zpracování, když používáte jednotky škálování.
author: perlynne
ms.date: 04/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSInventoryAdjustmentJournal, InventJournalCount
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: SCM
ms.author: perlynne
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a451816078ca2e77f30379828777209dc48bd849
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026126"
---
# <a name="warehouse-inventory-adjustment"></a>Úprava skladových zásob

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Funkce úpravy skladových zásob se používá při spuštění cloudových a hranových jednotek pro [výrobní úlohy](cloud-edge-workload-manufacturing.md) a [úlohy správy skladu](cloud-edge-workload-warehousing.md).

Když pracovník provede úpravu zásob pomocí aplikace skladu proti úloze správy skladu s jednotkou škálování, musí fyzickou aktualizaci skladových zásob zpracovat dávková úloha **Deník úprav skladových zásob**, kterou spustíte a naplánujete přechodem na **Správa skladu > Pravidelné úkoly > Deník úprav skladových zásob**.

Následující pracovní procesy aplikace skladu aktuálně používají **Deník úpravy skladových zásob** na úlohách jednotek škálování:

- Úprava příchozí/odchozí
- Cyklická inventura
- Načtení registrační značky

Několik transakcí inventáře je vytvořeno jako součást každého procesu přizpůsobení inventáře, protože nasazení centra a jednotky škálování sdílejí záznamy inventáře.

## <a name="inventory-adjustment-example"></a>Příklad úprav zásob

V tomto příkladu pracovník skladu použil aplikaci skladu k registraci přidání zásob na skladě.

Nejprve úloha jednotky škálování vytvoří transakci úpravy skladových zásob pro pozitivní fyzickou úpravu, která se poté synchronizuje s centrem a má za následek zvýšení zásob v centru.

| Typ                                    | Jednotka škálování | Směr | Centrum |
|-----------------------------------------|------------|-----------|-----|
| Úprava skladových zásob          | +1         | ->        | +1  |

Centrum poté zpracuje účtování deníku počítání, které je přijímáno prostřednictvím [zprávy procesoru zpráv](cloud-edge-message-processor-messages.md). Tím se aktualizují další dostupné zásoby. Aby se předešlo zdvojení skladových zásob, centrum vytvoří v rámci tohoto procesu transakci offsetu a odstraní dříve zaznamenané zásoby, které souvisí s úpravou skladu.

| Typ                                    | Jednotka škálování | Směr | Centrum |
|-----------------------------------------|------------|-----------|-----|
| Inventura                                | +1         | <-        | +1  |
| Úpravy skladu (offset) | -1         | <-        | -1  |

Po vytvoření jednotky škálování **Deník úpravy skladu** na centru můžete zkontrolovat **Deníku počítání** i **Ofsetový deník**, které jsou vytvářeny centrem jako součást procesu úpravy.

Každou z těchto položek deníku a transakce ve Supply Chain Management můžete zkontrolovat pomocí následujících kroků:

1. Přihlaste se k jednotce škálování.
1. Přejděte na **Správa skladu \> Periodické úkoly \> Deník úprav skladových zásob**.
1. Na stránce **Deník úprav skladových zásob** najděte a otevřete deník, který zaznamenal změnu dostupných zásob. Část **Řádky deníku** část ukazuje každou úpravu zaznamenanou tímto deníkem.
1. Přihlaste se k centru.
1. Přejděte na **Správa skladu \> Periodické úkoly \> Deník úprav skladových zásob**.
1. Na stránce **Deník úpravy skladových zásob**, pokud jste synchronizovali centrum a jednotku měřítka, měli byste vidět stejný deník.
1. Otevřít deník. Pokud byly [zprávy procesoru zprávy](cloud-edge-message-processor-messages.md) zpracovány, uvidíte odkazy na **Deník počítání** a **Ofsetový deník** v záhlaví.
    - **Deník počítání** by měl zobrazovat stejné hodnoty dimenzí jako řádky deníku.
    - **Ofsetový deník** by měl zobrazit offset, který odstraní úpravu zdvojení zásob.
    > [!NOTE]
    > Když jsou veškerá synchronizace a zpracování dokončeny, **Deník počítání** a **Ofsetový deník** jsou synchronizovány zpět do jednotky škálování. Ty lze také zobrazit na příslušné stránce **Deník úpravy skladových zásob**.

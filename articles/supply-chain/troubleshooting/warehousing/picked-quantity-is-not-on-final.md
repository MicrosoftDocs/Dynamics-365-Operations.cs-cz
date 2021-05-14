---
title: Zásilku nemůžete potvrdit, protože položky nebyly vybrány
description: Zásilku nemůžete potvrdit, protože položky nebyly vybrány
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938434"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Zásilku nemůžete potvrdit, protože položky nebyly vybrány

Kód chyby: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Příznaky

Když se pokusíte potvrdit dodávku, systém zobrazí následující chybovou zprávu:

> Některé položky, které jsou nezbytné pro vytížení %1, dosud nebyly vyzvednuty a přesunuty na konečné skladové místo.

Proto nemůžete potvrdit dodání pro zásilku.

## <a name="cause"></a>Příčina

Dodávku nebo zásilku nelze v aktuálním stavu potvrdit, protože může existovat jedna z následujících podmínek:

- Související práce ještě nebyly vybrány a přesunuty na konečné místo dodání.
- Vybrané množství práce neodpovídá vytvořenému množství práce na řádku dodávky.

## <a name="resolution"></a>Rozlišení

Zkontrolujte související prodejní objednávky nebo objednávky přenosu pro dodávku nebo zásilku. Ujistěte se, že všechny související práce byly dokončeny na konečném místě přepravy a že množství odpovídá.

1. Přejděte na **Řízení skladu \> Náklady \> Všechny náklady**.
1. Vyberte dodávku, pro kterou nelze potvrdit odeslání.
1. Na záložce s náhledem **Řádky nákladu** vyberte řádek nákladu.
1. Poznamenejte si hodnotu pole **Množství vytvořených prací**.
1. V podokně akcí na kartě **Náklady** ve skupině **Související informace** vyberte **Práce**.
1. Ověřte, že práce byla dokončena na konečném místě přepravy a že vybrané množství práce odpovídá vytvořenému množství práce na řádku zatížení.
1. Tento postup opakujte pro všechny řádky nákladů, abyste se ujistili, že jsou splněna všechna kritéria.

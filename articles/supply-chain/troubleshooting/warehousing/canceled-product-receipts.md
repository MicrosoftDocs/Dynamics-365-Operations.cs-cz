---
title: Zrušené příjmy produktů neaktualizují stav transakce na Registrovaný
description: Po zrušení příjmu produktu při příchozím načtení systém automaticky aktualizuje stav transakce inventáře z Přijato na Objednané.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: troubleshooting
ms.search.form: WMSPickingRegistration
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: eae703ce0b2c981518b18c4badd4f90031b902ece62f3ca0837427b306d618b1
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6731096"
---
# <a name="canceled-product-receipts-dont-update-transaction-status-to-registered"></a>Zrušené příjmy produktů neaktualizují stav transakce na Registrovaný

## <a name="symptoms"></a>Příznaky

Po spuštění akce **Zrušení příjmu produktu** při příchozím načtení systém automaticky aktualizuje stav transakce inventáře z *Přijato* na *Objednané*.

## <a name="resolution"></a>Řešení

Když jsou dodací listy zrušeny pro odchozí zatížení, stav transakcí zásob zůstane *Vydáno*. Když se však zruší příjmy produktu z příchozího zatížení, stav inventárních transakcí se neobnoví na *Registrováno*. Proto po zrušení příjmu produktu z příchozího nákladu musí pracovník skladu znovu zaregistrovat množství položek pro zatížení.

Další informace viz [Zaregistrujte množství zboží, které dorazí v příchozím nákladu](/dynamics365/supply-chain/warehousing/inbound-load-handling#register-item-quantities-arriving).

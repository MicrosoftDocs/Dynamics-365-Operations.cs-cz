---
title: Převod dílčí hlavní knihy do hlavní knihy
description: Toto téma popisuje funkce Microsoft Dynamics 365 Finance související s procesem převodu dílčí hlavní knihy do hlavní knihy.
author: roschlom
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1ae10f406148e213fd0272d1387f15606233be27
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000440"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Převod dílčí hlavní knihy do hlavní knihy

[!include [banner](../includes/banner.md)]

V tomto tématu jsou popsány funkce Microsoft Dynamics 365 Finance, které se vztahují k pravidlům převodu dávek položek dílčí hlavní knihy.

Ve verzi 8.1 byly provedeny změny za účelem umožnění přenosu pravidel, na jejichž základě je synchronní možnost odepsána. Další informace naleznete v části [Odstraněné nebo zastaralé funkce pro Finance and Operations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/deprecated-features?toc=/dynamics365/finance/toc.json#finance-and-operations-81-with-platform-update-20).

Pro převod dávek dílčí hlavní knihy jsou k dispozici následující možnosti. 

 - Asynchronní – Tato možnost okamžitě naplánuje převod účetních položek dílčí hlavní knihy do hlavní knihy. Doklad hlavní knihy bude zaznamenán, jakmile zdroje budou moci zpracovat tento požadavek na serveru. 

- Plánovaná dávka – Tato možnost přidá do hlavní knihy položky modulu zaúčtování dílčí hlavní knihy, které jsou přeneseny do fronty zpracování, kde budou položky zpracovány v přijatém pořadí. Doklad hlavní knihy bude v naplánovaném čase zaznamenán, jakmile zdroje budou moci zpracovat tuto dávkovou úlohu na serveru. 
 
Ve verzi 10.0.8 byla provedena vylepšení pro zvýšení výkonu asynchrnonní možnosti. Tato funkce je povolena pod názvem funkce **Optimalizace výkonu převodu z dílčí knihy do hlavní knihy**. 
 
Tato funkce zlepšuje přenos dat z dílčí hlavní knihy do hlavní knihy. Umožňuje efektivnější proces a seskupuje sady menších transakcí pro převod. To umožňuje efektivnější využití dávkového serveru. Tato funkce vyžaduje, aby byl dávkový server nastaven, online a funkční, aby bylo možné použít možnost asynchronního převodu. 

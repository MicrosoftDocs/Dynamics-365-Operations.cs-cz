---
title: Převod dílčí hlavní knihy do hlavní knihy
description: Toto téma popisuje funkce Microsoft Dynamics 365 Finance související s procesem převodu dílčí hlavní knihy do hlavní knihy.
author: roschlom
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 1efdf095e379b73d553ca3525abbeee8ca35bcbb
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897497"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Převod dílčí hlavní knihy do hlavní knihy

[!include [banner](../includes/banner.md)]

V tomto tématu jsou popsány funkce Microsoft Dynamics 365 Finance, které se vztahují k pravidlům převodu dávek položek dílčí hlavní knihy.

Ve verzi 8.1 byly provedeny změny za účelem umožnění přenosu pravidel, na jejichž základě je **synchronní** možnost odepsána. Další informace naleznete v části [Odstraněné nebo zastaralé funkce pro Finance and Operations](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Pro převod dávek dílčí hlavní knihy jsou k dispozici následující možnosti. 

 - Asynchronní – Tato možnost okamžitě naplánuje převod účetních položek dílčí hlavní knihy do hlavní knihy. Doklad hlavní knihy bude zaznamenán, jakmile zdroje budou moci zpracovat tento požadavek na serveru. 

- Plánovaná dávka – Tato možnost přidá do hlavní knihy položky modulu zaúčtování dílčí hlavní knihy, které jsou přeneseny do fronty zpracování, kde budou položky zpracovány v přijatém pořadí. Doklad hlavní knihy bude v naplánovaném čase zaznamenán, jakmile zdroje budou moci zpracovat tuto dávkovou úlohu na serveru. 
 
Ve verzi 10.0.8 byla provedena vylepšení pro zvýšení výkonu možnosti Asynchrnonní. Tato funkce je povolena pod názvem funkce **Optimalizace výkonu převodu z dílčí knihy do hlavní knihy**. 
 
Tato funkce zlepšuje přenos dat z dílčí hlavní knihy do hlavní knihy. Umožňuje efektivnější proces a seskupuje sady menších transakcí pro převod. To umožňuje efektivnější využití dávkového serveru. Tato funkce vyžaduje, aby byl dávkový server nastaven, online a funkční, aby bylo možné použít možnost asynchronního převodu. 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
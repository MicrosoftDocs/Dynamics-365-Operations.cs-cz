---
title: Převod dílčí hlavní knihy do hlavní knihy
description: Toto téma popisuje funkce související s procesem převodu dílčí hlavní knihy do hlavní knihy.
author: RyanCCarlson2
ms.date: 12/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalSetup, LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-01-18
ms.dyn365.ops.version: AX 10.0.8
ms.openlocfilehash: 70a34fa1f4ee540d89ec05816e4065fb3e1df9ef
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727307"
---
# <a name="subledger-transfer-to-the-general-ledger"></a>Převod dílčí hlavní knihy do hlavní knihy

[!include [banner](../includes/banner.md)]

V tomto tématu jsou popsány funkce, které se vztahují k pravidlům převodu dávek položek dílčí hlavní knihy.

Ve verzi 8.1 byly provedeny změny za účelem umožnění přenosu pravidel, na jejichž základě je **synchronní** možnost odepsána. Další informace naleznete v tématu [Odebrané nebo zastaralé funkce ve finančních a provozních aplikacích](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=%2fdynamics365%2ffinance%2ftoc.json#finance-and-operations-81-with-platform-update-20).

Pro převod dávek dílčí hlavní knihy jsou k dispozici následující možnosti:

- **Asynchronní** – Převod účetních položek dílčí hlavní knihy do hlavní knihy je naplánován okamžitě. Doklad hlavní knihy bude zaznamenán, jakmile zdroje budou moci zpracovat tento požadavek na serveru.
- **Plánovaná dávka** - Účetní položky podřízené účetní knihy, které je třeba převést, se přidají do fronty zpracování v hlavní knize. Položky ve frontě budou zpracovány v pořadí, v jakém byly přijaty. Každý doklad hlavní knihy aktualizuje účty v naplánovaném čase, jakmile zdroje budou moci zpracovat tuto dávkovou úlohu na serveru.

Ve verzi 10.0.8 byla provedena vylepšení pro zvýšení výkonu možnosti **Asynchrnonní**. Tato funkce je povolena pod názvem funkce **Optimalizace výkonu převodu z dílčí knihy do hlavní knihy**.

Funkce pro asynchronní přenos dávek podřízené knihy pomáhá zlepšit přenos dat z podřízené knihy do hlavní knihy. Díky seskupení sad menších transakcí a přenosu transakcí ve skupinách funkčnost zpracovává transakce efektivněji. Když jsou transakce seskupeny, prostředky dávkového serveru jsou využívány efektivněji.

Asynchronní přenos dávek dílčí knihy vyžaduje, aby byl dávkový server nastaven, online a funkční, protože dávkové úlohy jsou vytvářeny pro okamžité spuštění na dávkovém serveru. Když je povolena funkce **Optimalizace výkonu převodu z dílčí knihy do hlavní knihy**, dávková úloha systému **Automatizace procesů** s názvem **Úloha systému dotazování na automatizaci procesů** musí být také povolena. Další informace naleznete v tématu [Automatizace procesu](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

Změna efektivity na dávkové úrovni používá jednu opakovanou dávkovou úlohu pro všechny právnické osoby v systému. Za běhu je vytvořena nová dávková úloha ke zpracování požadovaných záznamů, které ještě nebyly přeneseny. Další nastavení lze ovládat ze stránky **Automatizace procesů** ve správě systému. Na této stránce můžete upravit proces na pozadí, změnit frekvenci a definovat období spánku.

Další informace o nastavení automatizace procesu najdete v tématu [Proces automatizace](../../fin-ops-core/dev-itpro/sysadmin/process-automation.md).

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

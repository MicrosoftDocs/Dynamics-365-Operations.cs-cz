---
title: " Konfigurace obchodů pro maloobchodní výkazy"
description: Tato procedura vás provede konfiguracemi pro maloobchod, které ovlivní způsob, jakým se vytvářejí a účtují výkazy obchodu.
author: jashanno
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4b73282abd2df92b3f466f7c1c6c210173001fd7
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/01/2020
ms.locfileid: "3021847"
---
# <a name="store-configurations-for-retail-statements"></a> Konfigurace obchodů pro maloobchodní výkazy

[!include[task guide banner](../includes/task-guide-banner.md)]

Tato procedura vás provede konfiguracemi pro maloobchod, které ovlivní způsob, jakým se vytvářejí a účtují výkazy obchodu. Finanční dimenze v obchodech jsou zahrnuty v jiné proceduře. Tato procedura používá ukázkovou společnost USRT.

1. V **Navigačním podokně** přejděte na **Moduly > Retail and Commerce > Kanály > Obchody > Všechny obchody**.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
4. Klikněte na možnost **Upravit**.
5. Nastavení v pevné záložce **Výkaz/uzávěrka** ovlivní vytvoření ověření a zaúčtování výkazu pro obchod. Rozbalte pevnou záložku **Výkaz/uzávěrka**.  
6. V poli **Metoda výkazu** vyberte metodu, podle které chcete seskupit řádky výpisu.  
7. Vyberte „Ano“ v možnosti **Jeden výkaz denně**, pokud má existovat pouze jeden výkaz vytvořený denně při vytváření výpisů z výkazu vytvoření dávkové úlohy.  
8. Pole **Výpočet výkazu úhrad** definuje, zda je třeba společně přidat výkazy úhrad, nebo zda má být použit poslední.  
9. V poli **Zaokrouhlení** vyberte účet hlavní knihy pro zaúčtování haléřových rozdílů.  
10. V poli **Maximální rozdíl zaokrouhlení** můžete zadat maximální povolený rozdíl zaokrouhlení.
11. V poli **Zaúčtování** můžete zadat maximální celkový povolený rozdíl pro zaúčtování pro výkaz.
12. V poli **Směna** můžete zadat maximální celkový rozdíl v rámci směny ve výkazu.  
13. V poli **Transakce** můžete zadat maximální celkový rozdíl v řádku výkazu.  
14. V poli **Metoda uzávěrky** můžete definovat, zda transakce, které budou zahrnuty do výkazu, by měly být součástí uzavřené směny, nebo zda se může jednat o libovolné transakce v rámci definovaného data a času.  
15. V poli **Konec pracovního dne** můžete zadat čas, pokud mají být transakce, ke kterým dojde po půlnoci, zaúčtovány v rámci předchozího dne.  
16. Vyberte „Ano“ v možnosti **Zaúčtovat jako pracovní den**, pokud mají být transakce, ke kterým dojde po půlnoci, zaúčtovány jako součást předchozího dne.  
17. Vyberte možnost „Ano“ v možnosti **Metoda rozdělení podle výpisu**, chcete-li získat výkazy vytvořené pro každou definovanou metodu výkazu. To je užitečné v případě, že výkon při účtování je třeba zlepšit pro obchody s vysokými objemy transakcí, protože vytvoří mnoho menších výkazů, které lze zpracovat současně.  
18. Na pevné záložce **Obecné**, v poli **Výchozí odběratel** můžete vybrat účet odběratele, který se má použít pro prodeje příchozím odběratelům.  


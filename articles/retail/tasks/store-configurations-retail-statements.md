--- 
title: " Konfigurace obchodů pro maloobchodní výkazy"
description: "Tato procedura vás provede konfiguracemi pro maloobchod, které ovlivní způsob, jakým se vytvářejí a účtují výkazy maloobchodu."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailStoreTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: cac676c9c6ebb6769fe7e30ac08a2c8334befc24
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="store-configurations-for-retail-statements"></a> Konfigurace obchodů pro maloobchodní výkazy

[!include[task guide banner](../includes/task-guide-banner.md)]

Tato procedura vás provede konfiguracemi pro maloobchod, které ovlivní způsob, jakým se vytvářejí a účtují výkazy maloobchodu. Finanční dimenze maloobchodu jsou zahrnuty v jiné proceduře. Tato procedura používá ukázkovou společnost USRT.

1. Přejděte do nabídky Maloobchodní a velkoobchodní prodej > Kanály > Maloobchody > Všechny maloobchody.
2. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
3. Klikněte na odkaz na vybraném řádku v seznamu.
    * Nastavení v části Výkaz/uzávěrka ovlivní vytvoření ověření a zaúčtování výkazu pro obchod.  Otevřete oddíl Výkaz/uzávěrka.  
    * Vyberte metodu, podle které chcete seskupit řádky výpisu.  
    * Vyberte „Ano“, pokud má existovat pouze jeden výkaz vytvořený denně při vytváření výpisů z výkazu vytvoření dávkové úlohy.  
    * Pole Výpočet výkazu úhrad definuje, zda je třeba společně přidat výkazy úhrad, nebo zda má být použit poslední.  
    * Vyberte účet hlavní knihy pro zaúčtování haléřových rozdílů.  
    * V poli Maximální rozdíl zaokrouhlení můžete zadat maximální povolený rozdíl zaokrouhlení.  
    * V poli Zaúčtování můžete zadat maximální celkový povolený rozdíl pro zaúčtování pro výkaz.  
    * V poli Směna můžete zadat maximální celkový rozdíl v rámci směny ve výkazu.  
    * V poli Transakce můžete zadat maximální celkový rozdíl v řádku výkazu.  
    * V poli Metoda uzávěrky můžete definovat, zda transakce, které budou zahrnuty do výkazu, by měly být součástí uzavřené směny, nebo zda se může jednat o libovolné transakce v rámci definovaného data a času.  
    * V poli Konec pracovního dne můžete zadat čas, pokud mají být transakce, ke kterým dojde po půlnoci, zaúčtovány v rámci předchozího dne.  
    * Vyberte „Ano“, pokud mají být transakce, ke kterým dojde po půlnoci, zaúčtovány jako součást předchozího dne.  
    * Vyberte možnost „Ano“ chcete-li získat výkazy vytvořené pro každou definovanou metodu výkazu. To je užitečné v případě, že výkon při účtování je třeba zlepšit pro obchody s vysokými objemy transakcí, protože vytvoří mnoho menších výkazů, které lze zpracovat současně.  
    * V poli Výchozí odběratel můžete vybrat účet odběratele, který se má použít pro prodeje příchozím odběratelům.  



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
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: af4321cd9d6e15c82c4eef1f1ca218b8301ebf35
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003646"
---
# <a name="store-configurations-for-retail-statements"></a> Konfigurace obchodů pro maloobchodní výkazy

[!include [banner](../includes/banner.md)]

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
17. Vyberte možnost „Ano“ v možnosti **Metoda rozdělení podle výpisu**, chcete-li získat výkazy vytvořené pro každou definovanou metodu výkazu. Tato akce je užitečná v případě, že výkon při účtování je třeba zlepšit pro obchody s vysokými objemy transakcí, protože vytvoří mnoho menších výkazů, které lze zpracovat současně.  
18. Na pevné záložce **Obecné**, v poli **Výchozí odběratel** můžete vybrat účet odběratele, který se má použít pro prodeje příchozím odběratelům.  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
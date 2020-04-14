---
title: Vytvoření, výpočet a zaúčtování výkazů pro maloobchod
description: Toto téma popisuje ruční postup pro vytvoření, výpočet a zaúčtování výpisu pro obchod.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailStatementTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21f1b0a34205e192957405bc9d298c45c8bb4d25
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141007"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>Vytvoření, výpočet a zaúčtování výkazů pro maloobchod

[!include [banner](../includes/banner.md)]

Toto téma popisuje ruční postup pro vytvoření, výpočet a zaúčtování výpisu pro obchod. Existují také dávkové úlohy, které lze konfigurovat pro stejné úkoly. Postup pro konfiguraci a spuštění dávkových úlohy můžete najít v jiných tématech. Pokud chcete tento postup dokončit, musíte mít transakce, které byly dokončeny v POS a pak odeslány do aplikace Dynamics 365 Commerce. Tento záznam používá v ukázkových datech společnost USRT.

1. Na domovské stránce vyberte **Finance obchodu**.
2. Vyberte **Nový výpis**.
3. V poli **Uložit číslo** vyberte z rozevíracího seznamu požadovanou možnost.
4. Vyberte **OK**.
5. Skupina **Nastavení** obsahuje nastavení, která řídí, které transakce budou zahrnuty do výkazu a způsob jejich seskupení do řádků výkazu. Můžete otevřít skupinu **Nastavení** a tato nastavení změnit, nebo můžete použít výchozí hodnoty.  
    - Pole **Metoda výkazu** definuje způsob, jak budou seskupeny řádky výkazu.  
    - Pokud chcete vypočítat výkaz pouze pro konkrétního zaměstnance nebo registr, v poli **zaměstnanec/registr** vyberte zaměstnance nebo registrační pokladnu.  
6. Vyberte možnost v poli **Metoda uzávěrky**.
7. V podokně akcí vyberte **Vypočítat výkaz**.
8. Vyberte **Ano**.
    - Po výpočtu výkazu, by měly být vytvořený řádky s celkovými částkami pro každý použitý způsob platby a metodu výkazu.  
    - Zadejte do každého řádku spočtenou částka, pokud je nutné ji zadávat nebo aktualizovat. Vypočtená pole budou vyplněna částkami z výkazů úhrad provedených v POS.  
9. V podokně akcí vyberte **Publikovat výkaz**.
10. Vyberte **Zavřít**.
11. Zavřete podokno.
12. Na domovské stránce vyberte **Finance obchodu**.
13. Vyberte kartu **Publikované výkazy**.


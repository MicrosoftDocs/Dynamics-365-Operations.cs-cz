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
ms.openlocfilehash: 4517b9ddeb648b3d789773fc0dcb1ecd3c8be85c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/24/2019
ms.locfileid: "2024791"
---
# <a name="create-calculate-and-post-statements-for-a-retail-store"></a>Vytvoření, výpočet a zaúčtování výkazů pro maloobchod

[!include[task guide banner](../includes/task-guide-banner.md)]

Toto téma popisuje ruční postup pro vytvoření, výpočet a zaúčtování výpisu pro obchod. Existují také dávkové úlohy, které lze konfigurovat pro stejné úkoly. Postup pro konfiguraci a spuštění dávkových úlohy můžete najít v jiných tématech. Pokud chcete tento postup dokončit, musíte mít transakce, které byly dokončeny v POS a pak odeslány do aplikace Dynamics 365 Retail. Tento záznam používá v ukázkových datech společnost USRT.

1. Na domovské stránce vyberte **Maloobchodní finance**.
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
12. Na domovské stránce vyberte **Maloobchodní finance**.
13. Vyberte kartu **Publikované výkazy**.


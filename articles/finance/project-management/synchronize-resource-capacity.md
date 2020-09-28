---
title: Synchronizace kapacity prostředku
description: Toto téma poskytuje informace o tom, jak synchronizovat kapacitu prostředku napříč kalendáři a projekty.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27b6fde91a72e37bb2712daba765032322cbd4e9
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760492"
---
# <a name="synchronize-resource-capacity"></a>Synchronizace kapacity prostředku

[!include [banner](../includes/banner.md)]

Procesy pro synchronizaci prostředků pomáhají zajistit, aby informace pro kalendář a základní kalendář přešly dále do plánování prostředků pro projekt. Pokud dojde ke změně kalendáře, procesy provedou požadované aktualizace v plánování zdrojů pro projekt. Procesy také pomáhají zvýšit výkonnost, protože informace o zdrojích kalendáře jsou synchronizovány v předstihu. Aktualizace informací o plánování zdrojů se děje tudíž rychleji. Doporučujeme naplánovat procesy jako dávku namísto postupného zpracování. V opačném případě je riziko, že někdo zapomene inkluzivní datum, kdy byly informace naposled synchronizovány. Pokud inkluzivní data nejsou použity, mohou vzniknout mezery v synchronizaci dat.

![Synchronizace kalendáře](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a>Synchronizace shrnutí kapacity pro prostředek

Proces synchronizace umožňuje synchronizovat všechny informace v kalendáři prostředku. Tyto informace zahrnují základní informace z kalendáře o všech změnách v tabulce kapacity kalendáře prostředků projektu. Pokud jsou do projektu přidány nové prostředky, synchronizace pomáhá zajistit, že jsou aktualizované informace k dispozici. Tuto synchronizaci lze provádět kdykoliv.

Doporučujeme používat dávky. Možnosti jsou dostupné při synchronizaci rezervací kapacity.

1. Zvolte **Řízení a účetnictví projektů** &gt; **Periodicky** &gt; **Synchronizace kapacity** &gt; **Synchronizace shrnutí kapacity pro prostředek**.
2. Nastavte možnosti v následující tabulce.

    | Parametr      | popis |
    |-------------|-------------|
    | Kód období | Volitelně vyberte kód datového intervalu hlavní knihy k nastavení počátečního a koncového data pro synchronizaci procesu pro shrnutí kapacity zdrojů. |
    | Počáteční datum  | Zadejte počáteční datum pro proces synchronizace pro shrnutí kapacity zdrojů. |
    | Koncové datum    | Zadejte koncové datum pro proces synchronizace pro shrnutí kapacity zdrojů. |

[![Proces synchronizace](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)

---
title: Vytvoření dlouhodobého majetku
description: Toto téma vysvětluje, jak vytvořit nový záznam o dlouhodobém majetku na stránce se seznamem dlouhodobého majetku.
author: moaamer
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ab330c604b2485687544a7d8b3eef3a652fa2069
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985130"
---
# <a name="create-a-fixed-asset"></a>Vytvoření dlouhodobého majetku

[!include [banner](../../includes/banner.md)]

Toto téma vysvětluje, jak vytvořit nový záznam o dlouhodobém majetku na stránce se seznamem **dlouhodobého majetku**.

Systém přiřadí číslo aktiva na základě číselné řady, která je přiřazena skupině dlouhodobého majetku. Pokud používáte šablonu dlouhodobého majetku k importu majetku prostřednictvím doplňku Microsoft Excel, nebo pokud použijete jinou úlohu importu, systém automaticky vytvoří záznamy dlouhodobého majetku a zvýší číslo aktiva.

Chcete-li ručně vytvořit záznam o majetku, postupujte takto.

1. Přejděte na **Podokno navigace \> Moduly \> Dlouhodobý majetek \> Dlouhodobý majetek \> Dlouhodobý majetek**.
2. V **podokně akcí** zvolte **Nový**.
3. Zadejte nebo vyberte hodnotu v poli **Skupina dlouhodobého majetku**. Pole **Číslo** bude výchozí, pokud je povolena funkce **Automaticky číslovat dlouhodobý majetek** v možnostech **Parametry dlouhodobého majetku** a **Skupina dlouhodobého majetku**. Pokud ne, je třeba zadat jednoznačné číslo k identifikaci dlouhodobého majetku.
4. Zadejte hodnotu do pole **Název**. Zadejte další informace, které vaše firma potřebuje pro tento majetek.
5. V **podokně akcí** vyberte **Knihy**.
6. Zadejte datum do pole **Datum pořízení**.
7. Zadejte číslo do pole **Pořizovací cena**.

    - Zadejte další informace, které vaše firma potřebuje pro tuto knihu.
    - Zadejte další informace, které vaše firma potřebuje pro zbývající knihy.

8. Zavřete stránku.

Dlouhodobý majetek můžete také importovat pomocí doplňku Excel nebo spuštěním úlohy importu z pracovního prostoru **Správa dat**. Před spuštěním importu zadejte do šablony hodnoty pro požadovaná pole.

Pokud jste nedefinovali číslo dlouhodobého majetku v šabloně doplňku aplikace Excel nebo ve správě dat, systém vytvoří číslo dlouhodobého majetku pro každé importované aktivum a automaticky zvýší číselnou sekvenci pro každý. Pokud však importujete majetek a v šabloně definujete čísla majetku, systém to automaticky **nezvýší** číselnou sekvenci. V takovém případě bude muset správce ručně aktualizovat číselnou posloupnost. Pokud jste definovali číslo dlouhodobého majetku v šabloně doplňku Excel, systém použije definované číslo dlouhodobého majetku a zvýší číselnou sekvenci.

> [!NOTE]                                                                                                         
> Po zaúčtování odpisů budou pole **Uvedeno do užívání** a **Datum zahájení odpisu** uzamčena na stránce **Kniha**. Ani jedno pole nebude aktualizováno z datové entity.

> [!WARNING]
> Záznam dlouhodobého majetku nebude odstraněn, pokud byly transakce zaúčtovány do přidružené knihy nebo pokud je nově vytvořený dlouhodobý majetek zadán na řádku deníku, ale nebyl zaúčtován. 

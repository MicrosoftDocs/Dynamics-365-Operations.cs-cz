---
title: "Přehled rozšířeného odsouhlasení banky"
description: "Tento článek popisuje průběhu procesu rozšířeného odsouhlasení banky. Funkci rozšířeného odsouhlasení banky umožňuje importovat bankovní výpisy, které mohou být automaticky odsouhlaseny z bankovních transakcí."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 22104
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 00f022da597b1de2454e93123de31731c6a65962
ms.openlocfilehash: 20363ef1917f7d0796cb0d5cd8e623c598b5ee01
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Přehled rozšířeného odsouhlasení banky

[!include[banner](../includes/banner.md)]


Tento článek popisuje průběhu procesu rozšířeného odsouhlasení banky. Funkci rozšířeného odsouhlasení banky umožňuje importovat bankovní výpisy, které mohou být automaticky odsouhlaseny z bankovních transakcí.

Funkce rozšířeného odsouhlasení banky umožňuje importovat bankovní výpisy. Importované bankovní výpisy lze poté automaticky odsouhlasit v rámci bankovních transakcí. Zde je postup pro tok rozšířeného odsouhlasení banky.

1.  Nastavte import bankovních výpisů.
    -   Importujte bankovní výpisy prostřednictvím rozhraní datové entity.
    -   Součástí aplikace jsou tři obvyklé formáty bankovních výpisů: ISO20022, BAI2 a MT940.
    -   Tuto funkci lze rozšířit o jakýkoli formát.

2.  Nastavte číselnou řadu pro použití rozšířeného odsouhlasení banky a definujte pravidla párování pro odsouhlasení banky.
    -   Odpovídající pravidla vyrovnání je sada kritérií, která slouží k filtrování řádků bankovního výpisu a Microsoft Dynamics 365 pro bankovní operace řádky transakce během odsouhlasení. V závislosti na obchodních postupů můžete nastavit více než jedno pravidlo pro porovnávání k automatizaci a optimalizaci procesu odsouhlasení.

3.  Odsouhlaste bankovní výpisy s Dynamics 365 pro bankovní operace transakce.
    -   Proveďte automatické párování a vytvoření deníků odsouhlasení.
    -   Zobrazení bankovních výpisů a 365 Dynamics pro bankovní operace transakce vedle sebe.
    -   Pokud se objeví na bankovním výpisu, ale nejsou zobrazeny v 365 Dynamics pro operace automaticky účtovat Dynamics 365 pro bankovní operace transakce.
    -   Generujte výkaz odsouhlasení.







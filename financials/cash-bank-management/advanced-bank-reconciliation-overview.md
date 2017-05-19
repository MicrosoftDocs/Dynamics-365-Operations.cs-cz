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
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 6977cb3b315a90b504fc6748d2a4d02854a9d5ef
ms.contentlocale: cs-cz
ms.lasthandoff: 04/25/2017


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
    -   Odpovídající pravidlo odsouhlasení představuje sadu kritérií, které se používají k filtru řádků bankovního výpisu a řádků bankovních transakcí aplikace Microsoft Dynamics 365 for Operations během odsouhlasení. V závislosti na vašich obchodních praktikách můžete nastavit více než jedno pravidlo párování k automatizaci a optimalizaci vašeho procesu odsouhlasení.

3.  Odsouhlaste bankovní výpisy s bankovními transakcemi aplikace Dynamics 365 for Operations.
    -   Proveďte automatické párování a vytvoření deníků odsouhlasení.
    -   Prohlédněte si bankovní výpisy a bankovní transakce aplikace Dynamics 365 for Operations vedle sebe.
    -   Automaticky zaúčtujte bankovní transakce aplikace Dynamics 365 for Operations, pokud se zobrazí na bankovním výpisu, ale nezobrazí v aplikaci Dynamics 365 for Operations.
    -   Generujte výkaz odsouhlasení.







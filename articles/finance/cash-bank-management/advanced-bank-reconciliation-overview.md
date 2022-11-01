---
title: Přehled rozšířeného odsouhlasení banky
description: Tento článek popisuje průběhu procesu rozšířeného odsouhlasení banky. Funkci rozšířeného odsouhlasení banky umožňuje importovat bankovní výpisy, které mohou být automaticky odsouhlaseny z bankovních transakcí.
author: angelad116
ms.date: 10/24/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: kfend
ms.custom:
- "22104"
- intro-internal
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 677a032ce77fbe57393c85235a1c64dba3958f2d
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715142"
---
# <a name="advanced-bank-reconciliation-overview"></a>Přehled rozšířeného odsouhlasení banky

[!include [banner](../includes/banner.md)]

Tento článek popisuje průběhu procesu rozšířeného odsouhlasení banky. Funkci rozšířeného odsouhlasení banky umožňuje importovat bankovní výpisy, které mohou být automaticky odsouhlaseny z bankovních transakcí.

Funkce rozšířeného odsouhlasení banky umožňuje importovat bankovní výpisy. Importované bankovní výpisy lze poté automaticky odsouhlasit v rámci bankovních transakcí. Zde je postup pro tok rozšířeného odsouhlasení banky.

1.  Nastavte import bankovních výpisů.
    -   Importujte bankovní výpisy prostřednictvím rozhraní datové entity.
    -   Součástí aplikace jsou tři obvyklé formáty bankovních výpisů: ISO20022, BAI2 a MT940.
    -   Tuto funkci lze rozšířit o jakýkoli formát.

2.  Nastavte číselnou řadu pro použití rozšířeného odsouhlasení banky a definujte pravidla párování pro odsouhlasení banky.
    -   Odpovídající pravidlo odsouhlasení představují sadu kritérií, která se používají k filtrování řádků bankovních výpisů a řádků bankovních transakcí aplikace Microsoft Dynamics 365 Finance během procesu sesouhlasení. V závislosti na vašich obchodních praktikách můžete nastavit více než jedno pravidlo párování k automatizaci a optimalizaci vašeho procesu odsouhlasení.

3.  Odsouhlaste bankovní výpisy s bankovními transakcemi aplikace Finance.
    -   Proveďte automatické párování a vytvoření deníků odsouhlasení.
    -   Zobrazte bankovní výpisy a bankovní transakce aplikace Finance vedle sebe.
    -   Automaticky zaúčtujte bankovní transakce aplikace Finance, pokud se zobrazí na bankovním výpisu, ale nezobrazí v aplikaci Finance.
    -   Generujte výkaz odsouhlasení.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]

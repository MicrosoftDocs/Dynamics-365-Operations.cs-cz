---
title: Přehled rozšířeného odsouhlasení banky
description: Tento článek popisuje průběhu procesu rozšířeného odsouhlasení banky. Funkci rozšířeného odsouhlasení banky umožňuje importovat bankovní výpisy, které mohou být automaticky odsouhlaseny z bankovních transakcí.
author: panolte
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "22104"
- intro-internal
ms.assetid: b0705653-1fa6-4d94-9728-bcf9fb387ad1
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 93ba7c8dc29a50de4b4cec342a5a83efe03e6419
ms.sourcegitcommit: 92ff867a06ed977268ffaa6cc5e58b9dc95306bd
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 07/03/2021
ms.locfileid: "6336134"
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
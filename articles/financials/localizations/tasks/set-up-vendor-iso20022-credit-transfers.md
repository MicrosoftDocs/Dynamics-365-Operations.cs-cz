--- 
title: "Nastavení dodavatelů a bankovních účtů dodavatelů pro převody kreditu ve formátu ISO20022"
description: "Tento postup popisuje způsob nastavení informací o dodavateli a konkrétním bankovním účtu dodavatele požadovaných pro převedení kreditu SEPA nebo jakéhokoli jiného generování souboru pro platbu dodavatele podle normy ISO20022."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f01947840553a65af4aba1309d89f9b3e9ced872
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-vendors-and-vendor-bank-accounts-for-iso20022-credit-transfers"></a>Nastavení dodavatelů a bankovních účtů dodavatelů pro převody kreditu ve formátu ISO20022

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tento postup popisuje způsob nastavení informací o dodavateli a konkrétním bankovním účtu dodavatele požadovaných pro převedení kreditu SEPA nebo jakéhokoli jiného generování souboru pro platbu dodavatele podle normy ISO20022. 

K vytvoření tohoto postupu jsou použita ukázková data společnosti DEMF.
Toto je čtvrtý z pěti úkolů, které společně popisují proces platby dodavatele pomocí konfigurací elektronického výkaznictví. Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.


## <a name="set-up-bank-details"></a>Nastavení podrobností o bance
1. Přejděte do části Závazky > Dodavatelé > Všichni dodavatelé.
2. Použijte rychlý filtr pro hledání záznamů. V poli Účet dodavatele můžete například filtrovat pomocí hodnoty „DE-001“.
3. Klepnutím na položku DE-001 zobrazíte podrobnosti o dodavateli.
4. V podokně akcí klikněte na možnost Dodavatel.
5. Klikněte na možnost Bankovní účty.
6. Klikněte na položku Upravit.
    * Pokud není k dispozici žádný bankovní účet, musíte vytvořit nový.  
7. V poli Kód SWIFT zadejte hodnotu COBADEFFXXX".
8. Zadejte do pole IBAN hodnotu „DE36200400000628808808“.
9. Zavřete stránku.

## <a name="set-up-a-method-of-payment-for-the-vendor"></a>Nastavení metody platby pro dodavatele
1. Klikněte na položku Upravit.
2. Rozbalte nebo sbalte oddíl Platba.
3. V poli Způsob platby kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Klikněte na odkaz na řádku SEPA CT v seznamu.
5. Klikněte na položku Uložit.



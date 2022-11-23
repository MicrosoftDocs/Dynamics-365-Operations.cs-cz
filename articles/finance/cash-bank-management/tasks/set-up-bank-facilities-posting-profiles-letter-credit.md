---
title: Nastavení zařízení banky a zaúčtování profilů pro akreditiv
description: Tento postup vás provede vytvořením bankovního zařízení a účetního profilu potřebného pro zpracování akreditivu.
author: kweekley
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7fe5b2ba43c4fcb4855c742bdb6f8209ebd92d68
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779455"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Nastavení zařízení banky a zaúčtování profilů pro akreditiv

[!include [banner](../../includes/banner.md)]

Tento postup vás provede vytvořením bankovního zařízení a účetního profilu potřebného pro zpracování akreditivu. 

Tento úkol využívá ukázkovou společnost USMF.


## <a name="general-ledger-parameter"></a>Parametr hlavní knihy
1. Přejděte do nabídky **Pokladna a banka > Nastavení > Parametry pokladny a banky**.
2. Rozbalte oddíl **Bankovní dokument**.
3. Vyberte možnost **Povolit import akreditivu**.
4. Vyberte možnost **Povolit export akreditivu**.
5. Klikněte na tlačítko **Uložit**.
6. Zavřete stránku.

## <a name="create-bank-facility"></a>Vytvoření bankovního zařízení
1. Přejděte do nabídky **Pokladna a banka > Nastavení > Bankovní zařízení**.
2. Klepněte na možnost **Nový**.
3. V poli **Skupina zařízení** zadejte název skupiny bankovních zařízení.
4. V poli **Popis** zadejte popis skupiny bankovních zařízení.
5. Klikněte na tlačítko **Uložit**.
6. Klikněte na kartu **Typy zařízení**.
7. Klepněte na možnost **Nový**.
8. Do pole **Typ zařízení** zadejte jedinečný kód.
9. Zadejte hodnotu do pole **Popis**.
10. V poli **Skupina zařízení** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
11. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
12. Klikněte na odkaz na vybraném řádku v seznamu.
13. V poli **Druh zařízení** vyberte povahu bankovního zařízení.
14. Klikněte na tlačítko **Uložit**.
15. Zavřete stránku.

## <a name="bank-posting-profile"></a>Účetní profil banky
1. Přejděte do nabídky **Pokladna a banka > Nastavení > Profil účtování bankovních dokumentů**.
2. Klepněte na možnost **Nový**.
3. V poli **Číslo účtu/skupiny** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Vyberte hlavní účet pro vyrovnání.
    * Tento účet se používá při výpočtu prognózy pro cashflow.  
7. V poli **Poplatkový účet** vyberte účet pro výdajové transakce.
8. V poli **Maržový účet** vyberte účet pro transakce marže.
    * Tento účet je debetován, pokud je počáteční marže zaúčtována a kreditován po zaúčtování platby.  
9. Klikněte na tlačítko **Uložit**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

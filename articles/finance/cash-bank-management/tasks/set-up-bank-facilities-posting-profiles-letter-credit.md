---
title: Nastavení zařízení banky a zaúčtování profilů pro akreditiv
description: Tento postup vás provede vytvořením bankovního zařízení a účetního profilu potřebného pro zpracování akreditivu.
author: kweekley
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BankParameters, DefaultDashboard, BankDocumentSetup, BankDocumentPosting
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 15a7a4798c4c743c9171fd2258a5573f456c92e5
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8726343"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letter-of-credit"></a>Nastavení zařízení banky a zaúčtování profilů pro akreditiv

[!include [banner](../../includes/banner.md)]

Tento postup vás provede vytvořením bankovního zařízení a účetního profilu potřebného pro zpracování akreditivu. 

Tento úkol využívá ukázkovou společnost USMF.






## <a name="general-ledger-parameter"></a>Parametr hlavní knihy
1. Přejděte do nabídky Pokladna a banka > Nastavení > Parametry pokladny a banky.
2. Rozbalte oddíl Bankovní dokument.
3. Vyberte možnost Povolit import akreditivu.
4. Vyberte možnost Povolit export akreditivu.
5. Klikněte na položku Uložit.
6. Zavřete stránku.

## <a name="create-bank-facility"></a>Vytvoření bankovního zařízení
1. Přejděte do nabídky Pokladna a banka > Nastavení > Bankovní zařízení.
2. Klikněte na položku Nová.
3. V poli Skupina zařízení zadejte název skupiny bankovních zařízení.
4. V poli Popis zadejte popis skupiny bankovních zařízení.
5. Klikněte na položku Uložit.
6. Klikněte na kartu Typy zařízení.
7. Klikněte na položku Nová.
8. Do pole Typ zařízení zadejte jedinečný kód.
9. Zadejte nějakou hodnotu do pole Popis.
10. V poli Skupina zařízení kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
11. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
12. Klikněte na odkaz na vybraném řádku v seznamu.
13. V poli Druh zařízení vyberte povahu bankovního zařízení.
14. Klikněte na položku Uložit.
15. Zavřete stránku.

## <a name="bank-posting-profile"></a>Účetní profil banky
1. Přejděte do nabídky Pokladna a banka > Nastavení > Profil účtování bankovních dokumentů.
2. Klikněte na položku Nová.
3. V poli Číslo účtu/skupiny kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. Vyberte hlavní účet pro vyrovnání.
    * Tento účet se používá při výpočtu prognózy pro cashflow.  
7. V poli Poplatkový účet vyberte účet pro výdajové transakce.
8. V poli Maržový účet vyberte účet pro transakce marže.
    * Tento účet je debetován, pokud je počáteční marže zaúčtována a kreditován po zaúčtování platby.  
9. Klikněte na položku Uložit.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

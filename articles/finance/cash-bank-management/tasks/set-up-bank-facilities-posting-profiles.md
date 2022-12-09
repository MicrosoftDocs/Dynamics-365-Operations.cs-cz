---
title: Nastavení zařízení banky a zaúčtování profilů pro záruční listiny
description: Tato úloha vytvoří bankovní zařízení a účetní profil potřebný pro zpracování záruční listiny.
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
ms.openlocfilehash: 0987ae1e9cfbb1e2d2a957a5fd1ad82257292c0a
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/23/2022
ms.locfileid: "9804094"
---
# <a name="set-up-bank-facilities-and-posting-profiles-for-letters-of-guarantee"></a>Nastavení zařízení banky a zaúčtování profilů pro záruční listiny

[!include [banner](../../includes/banner.md)]

Tato úloha vytvoří bankovní zařízení a účetní profil potřebný pro zpracování záruční listiny.



Tento úkol používá ukázkovou společnost USMF. 




## <a name="general-ledger-parameter"></a>Parametr hlavní knihy
1. Přejděte do nabídky **Pokladna a banka > Nastavení > Parametry pokladny a banky**.
2. Rozbalte oddíl **Bankovní dokument**.
3. Vyberte možnost **Povolit záruční listinu**.
4. V poli **Deník transakce** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
5. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
6. Klikněte na odkaz na vybraném řádku v seznamu.
7. Klikněte na kartu **Číselné řady**.
    * Definování kódu číselné řady pro číslo záruční listiny záruční a odkazy na transakce záruční listiny  
8. Klikněte na tlačítko **Uložit**.
9. Zavřete stránku.

## <a name="create-bank-facility"></a>Vytvoření bankovního zařízení
1. Přejděte do nabídky **Pokladna a banka > Nastavení > Bankovní zařízení**.
2. Klepněte na možnost **Nový**.
3. V poli **Skupina zařízení** zadejte název skupiny bankovních zařízení pro transakci záruční listiny.
4. Zadejte hodnotu do pole **Popis**.
5. Klikněte na tlačítko **Uložit**.
6. Klikněte na kartu **Typy zařízení**.
7. Klepněte na možnost **Nový**.
8. V poli **Typ zařízení** zadejte název typu bankovního zařízení, který se vztahuje se k zařízení smlouvy bankovního zařízení.
9. Zadejte hodnotu do pole **Popis**.
10. V poli **Skupina zařízení** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
11. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
12. Klikněte na odkaz na vybraném řádku v seznamu.
13. Vyberte možnost v poli **Druh zařízení**.
14. Klikněte na možnost **Uložit**.
15. Zavřete stránku.

## <a name="bank-posting-profile"></a>Účetní profil banky
1. Přejděte do nabídky **Pokladna a banka > Nastavení > Profil účtování bankovních dokumentů**.
2. Klepněte na možnost **Nový**.
3. V poli **Číslo účtu/skupiny** kliknutím na tlačítko rozevíracího seznamu otevřete vyhledávání.
4. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
5. Klikněte na odkaz na vybraném řádku v seznamu.
6. V poli **Účet vyrovnání** vyberte hlavní účet pro vyrovnání.
7. V poli **Poplatkový účet** vyberte účet pro výdajové transakce.
8. V poli **Maržový účet** vyberte účet pro transakci marže.
9. V poli **Účet likvidace** vyberte účet likvidace pro transakci záruční listiny. 
10. Klikněte na tlačítko **Uložit**.
11. Zavřete stránku.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

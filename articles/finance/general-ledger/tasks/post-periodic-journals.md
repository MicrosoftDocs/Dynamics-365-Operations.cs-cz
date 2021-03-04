---
title: Účtování periodických deníků
description: Periodické deníky se někdy nazývají opakované deníky, protože částka, text a ostatní informace se opakují při každém získání periodického deníku.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7f721a05c8b74f1cfcf43177b73129751483650e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441183"
---
# <a name="post-periodic-journals"></a>Účtování periodických deníků

[!include [banner](../../includes/banner.md)]

Periodické deníky se někdy nazývají opakované deníky, protože částka, text a ostatní informace se opakují při každém získání periodického deníku. Při vytváření periodického deníku zadáte interval pro opakování, například dny nebo měsíce. Tento průvodce úkolem vytvoří periodický deník s měsíčním opakováním.

1. Přejděte na **Navigační podokno >Moduly > Hlavní kniha > Periodické úlohy**.
2. Klepněte na možnost **Nový**.
3. V poli **Název** zadejte nebo vyberte hodnotu.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Zadejte hodnotu do pole **Popis**. Popis bude představovat název periodického deníku při jeho pozdějším použití, takže nezapomeňte použít vhodný název.
6. V **Podokně akcí** klikněte na **Řádky**. Periodický deník obvykle zahrnuje několik řádků deníku. Tento průvodce úkolem však přidá pouze jeden řádek.
7. Do pole **Datum** zadejte datum. Pole **Datum** obsahuje datum zaúčtování pro následující přenos do denního deníku. Pro deníky, které budou načteny každý měsíc, je doporučeno použít datum v měsíci odpovídající jeho zaúčtování - typicky první nebo poslední den daného období. Je možné ponechat pole Datum prázdné a datum doplnit, až je deník načten (pomocí pole Prázdné datum). Pole je automaticky aktualizováno na další opakující se datum, kdy jsou načteny transakce. 
8. Zadejte požadované hodnoty do pole **Účet**.
9. V poli **Popis** zadejte nebo vyberte hodnotu.
10. Zavřete stránku.
11. Do pole **Má dáti** zadejte číslo.
12. Zadejte požadované hodnoty do pole **Protiúčet**.
13. V poli **Jednotka** pak vyberte možnost Měsíce.
14. Do pole **Počet jednotek zadejte** „1“.
15. V poli **Poslední datum** zadejte datum. Zadání koncového data do předchozího období zabrání nechtěnému vytvoření periodického deníku v nesprávném počátečním období. Poslední datum bude později aktualizováno pokaždé, když je načten periodický deník. 
16. Klikněte na možnost **Uložit**.
17. Přejděte na **Navigační podokno > Moduly > Hlavní kniha > Položky deníku > Hlavní deníky**.
18. Klepněte na možnost **Nový**.
19. V poli **Název** zadejte nebo vyberte hodnotu.
20. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
21. Klikněte na odkaz na vybraném řádku v seznamu.
22. Zadejte hodnotu do pole **Popis**.
23. V **Podokně akcí** klikněte na **Řádky**.
24. V **Podokně akcí** klikněte na možnost **Deník období**.
25. Klikněte na **Načíst deník.**
26. Do pole **Do data** zadejte datum. **Koncové datum** slouží jako datum přerušení pro periodické řádky dokladu. Na základě nastavení opakování může stejný řádek Koncové datum a Do data být zahrnut vícekrát ve výsledném deníku. Do data je automaticky aktualizováno na základě data relace – poslední datum, kdy byl řádek přenesen do deníku. 
27. V poli **Číslo periodického deníku** zadejte nebo vyberte hodnotu.
28. Klikněte na odkaz na vybraném řádku v seznamu.
29. Klikněte na tlačítko **OK**. Periodický deník lze nyní zkontrolovat, schválit nebo zaúčtovat v závislosti na požadavcích a nastavení.   


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
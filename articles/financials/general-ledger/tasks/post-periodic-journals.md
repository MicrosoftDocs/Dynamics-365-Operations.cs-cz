--- 
title: "Účtování periodických deníků"
description: "Periodické deníky se někdy nazývají opakované deníky, protože částka, text a ostatní informace se opakují při každém získání periodického deníku."
author: aprilolson
manager: AnnBe
ms.date: 02/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8eae11e0501db78e467e517b29a2bc19f5765e75
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="post-periodic-journals"></a>Účtování periodických deníků

[!include [task guide banner](../../includes/task-guide-banner.md)]

Periodické deníky se někdy nazývají opakované deníky, protože částka, text a ostatní informace se opakují při každém získání periodického deníku. Při vytváření periodického deníku zadáte interval pro opakování, například dny nebo měsíce. Tento průvodce úkolem vytvoří periodický deník s měsíčním opakováním.



1. Přejděte do hlavní knihy > Periodické úkoly > Periodické deníky.
2. Klikněte na položku Nová.
3. V poli Název zadejte nebo vyberte hodnotu.
4. Klikněte na odkaz na vybraném řádku v seznamu.
5. Zadejte nějakou hodnotu do pole Popis.
    * Popis bude představovat název periodického deníku při jeho pozdějším použití, takže nezapomeňte použít vhodný název.  
6. Klikněte na položku Řádky.
    * Periodický deník obvykle zahrnuje několik řádků deníku. Tento průvodce úkolem však přidá pouze jeden řádek.  
7. Do pole Datum zadejte datum.
    * Pole Datum obsahuje datum zaúčtování pro následující přenos do denního deníku. Pro deníky, které budou načteny každý měsíc, je doporučeno použít datum v měsíci odpovídající jeho zaúčtování - typicky první nebo poslední den daného období. Je možné ponechat pole Datum prázdné a datum doplnit, až je deník načten (pomocí pole Prázdné datum).    Pole je automaticky aktualizováno na další opakující se datum, kdy jsou načteny transakce.  
8. Zadejte požadované hodnoty do pole Účet.
9. Zadejte nějakou hodnotu do pole Popis.
10. Zavřete stránku.
11. Do pole Má dáti zadejte čísl.
12. Zadejte požadované hodnoty do pole Protiúčet.
13. V poli Jednotka pak vyberte možnost Měsíce.
14. Do pole Počet jednotek zadejte „1“.
15. V poli Poslední datum zadejte datum.
    * Zadání koncového data do předchozího období zabrání nechtěnému vytvoření periodického deníku v nesprávném počátečním období. Poslední datum bude později aktualizováno pokaždé, když je načten periodický deník.  
16. Klikněte na položku Uložit.
17. Přejděte na výchozí řídicí panel.
18. Přejděte do nabídky Hlavní kniha > Položky deníku > Hlavní deníky.
19. Klikněte na položku Nová.
20. V poli Název zadejte nebo vyberte hodnotu.
21. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
22. Klikněte na odkaz na vybraném řádku v seznamu.
23. Zadejte nějakou hodnotu do pole Popis.
24. Klikněte na položku Řádky.
25. Klikněte na Periodický deník.
26. Klikněte na Načíst deník.
27. Do pole Do data zadejte datum.
    * Koncové datum slouží jako datum přerušení pro periodické řádky dokladu. Na základě nastavení opakování může stejný řádek Koncové datum a Do data být zahrnut vícekrát ve výsledném deníku. Do data je automaticky aktualizováno na základě data relace – poslední datum, kdy byl řádek přenesen do deníku.  
28. V poli Číslo periodického deníku zadejte nebo vyberte hodnotu.
29. Klikněte na odkaz na vybraném řádku v seznamu.
30. Klikněte na tlačítko OK.
    * Periodický deník lze nyní zkontrolovat, schválit nebo zaúčtovat v závislosti na požadavcích a nastavení.  



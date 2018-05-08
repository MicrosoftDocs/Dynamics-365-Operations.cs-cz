--- 
title: "Nastavení DIČ"
description: "Tato procedura vás provede předpoklady registrace DIČ, jako je nastavení typu registrace a jeho přiřazení kategorii registrace."
author: v-oloski
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 20f64385b988ff48d865d2d521a9e580dc04c4a2
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-vat-id"></a>Nastavení DIČ

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura vás provede předpoklady registrace DIČ, jako je nastavení typu registrace a jeho přiřazení kategorii registrace. Další informace o ID registrace a zpracování ID registrace, včetně povinných požadavků, najdete v tématu nápovědy věnovaném ID registrace a zpracování ID registrace. 

Informace zde uvedené se vztahují na všechny evropské země/oblasti. Tento úkol byl vytvořen za použití ukázkových dat společnosti DEMF s primární adresou právnické osoby v Německu. Tento úkol je určen pro správce systému. Tato procedura je určena pro funkci, která byla přidána do aplikace Dynamics 365 for Operations verze 1611.

1. Přejděte na položky Správa organizace > Globální adresář > Typy registrace > Typy registrace.
2. Kliknutím na možnost Nový otevřete dialogové okno.
3. Do pole Název zadejte DIČ.
4. Do pole Popis zadejte Číslo DPH.
5. V poli Země/oblast zadejte nebo vyberte hodnotu DEU.
6. Vyberte Ano v poli Jedinečný.
    * Zaškrtněte toto políčko, chcete-li ověřit, zda je DPH jedinečná.  
7. Vyberte možnost Primární v poli Země.
    * Toto políčko zaškrtněte, pokud bude DIČ platit pro všechny adresy patřící do určené země nebo regionu.  
8. Klikněte na položku Vytvořit.
9. Klepněte na možnost Přidat.
10. V poli Země/oblast zadejte nebo vyberte hodnotu ITA.
11. Do pole formát napište '###########'.
    * Při zadání ID registrace tohoto typu pro vybranou zemi nebo oblast bude ID registrace ověřeno na základě tohoto formátu.  
12. Zaškrtněte políčko Jedinečné.
    * Zaškrtněte toto políčko, chcete-li ověřit, zda je DPH jedinečná.  
13. Zaškrtněte políčko Primární pro zemi.
    * Toto políčko zaškrtněte, pokud bude DIČ platit pro všechny adresy patřící do určené země nebo regionu.  
14. Klikněte na položku Uložit.
15. Přejděte na položky Správa organizace > Globální adresář > Typy registrace > Kategorie registrace.
16. Klikněte na položku Nová.
17. V poli Země/oblast zadejte nebo vyberte hodnotu DIČ, DEU.
18. V poli kategorie registrace vyberte DIČ.
    * Přiřaďte typ registrace, který jste vytvořili dříve, k předdefinované kategorii registrace.  
19. Klikněte na položku Nová.
20. V poli Země/oblast zadejte nebo vyberte hodnotu DIČ, ITA.
21. V poli kategorie registrace vyberte DIČ.
    * Přiřaďte typ registrace, který jste vytvořili, k předdefinované kategorii registrace.  
22. Klikněte na položku Uložit.



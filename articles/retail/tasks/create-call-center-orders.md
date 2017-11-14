--- 
title: " Vytváření objednávek v kontaktním středisku"
description: "Tato procedura vás provede vyhledáním odběratele vytvořením nové objednávky, vyhledáváním produktu a inkasováním platby od odběratele."
author: josaw1
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: f702690f72b3e299f6c2744da326a23d5753eb5d
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="create-call-center-orders"></a> Vytváření objednávek v kontaktním středisku

[!include[task guide banner](../includes/task-guide-banner.md)]

Tato procedura vás provede vyhledáním odběratele vytvořením nové objednávky, vyhledáváním produktu a inkasováním platby od odběratele. Tato procedura používá ukázková data USRT společnosti a je určena pro úředníka prodejní objednávky. Předpoklady: Uživatelé provádějící proceduru jsou nastaveni jako uživatelé kontaktního střediska a pololetní katalog společnosti Fabrikam je publikovaném s alespoň jedním zdrojovým kódem.

1. Přejděte na Maloobchodní a velkoobchodní prodej > Odběratelé > Služby odběratele.
2. V poli SearchText zadejte kritéria vyhledávání pro vyhledávání odběratele.
    * Pro tuto vzorovou proceduru zadejte text „karen“ a stiskněte tabulátor.  
3. Klikněte na Hledat.
    * Jelikož v ukázkových datech existuje pouze jeden odběratel se jménem Karen, bude výběr proveden automaticky.  
4. Klepněte na položky Nová prodejní objednávka.
5. Rozbalte nebo sbalte oddíl Záhlaví prodejní objednávky.
6. Vyberte typ zdrojového kódu pro katalog.
    * Pokud neexistují žádné aktivní zdrojové kódy, můžete zavřít pole Zdroj a tento krok vynechat.  
7. Klikněte na položku Přidat řádek.
8. Do pole Číslo položky zadejte hledaný výraz položky.
    * U této vzorové procedury zadejte číslo dílčí položky „8111“ a stiskněte tabulátor. Objeví se místní okno hledání položky.  
9. Vyberte produkt, který chcete přidat do prodejní objednávky
10. Zadejte prodejní množství.
11. Klepněte na volbu Nový.
12. Kliknutím na tlačítko Dokončit zachytíte platbu odběratele.
13. Klepněte na možnost Přidat.
    * Odkaz Přidat se nachází na kartě Platby. Pokud je sbalena karta Platby, rozbalte ji.  
14. Vyberte způsob platby.
    * V této proceduře vyberte hotovostní způsob platby.  
15. Zavřete stránku.
16. Zadejte částku.
    * V této proceduře zadejte částku odpovídající výši zůstatku objednávky, který lze zobrazit na stránce Souhrn prodejní objednávky vlevo od pole Částka. Díky tomu budete moci ukončit objednávku jako plně zaplacenou.  
17. Klikněte na tlačítko OK.
18. Klepněte na tlačítko Odeslat.


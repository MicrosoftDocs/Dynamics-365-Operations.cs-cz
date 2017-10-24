--- 
title: "Zpracování upomínek"
description: "Tato procedura popisuje způsob tvorby, tisku a zaúčtování upomínek."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: dc837ea6513992a5f94e48baa366e279df297866
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="process-collection-letters"></a>Zpracování upomínek

[!include[task guide banner](../../includes/task-guide-banner.md)]

Tato procedura popisuje způsob tvorby, tisku a zaúčtování upomínek. Tento úkol používá ukázkovou společnost USMF.


## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Nastavení posloupnosti upomínek v účetním profilu
1. Přejděte do nabídky na Kredit a inkasa > Nastavení > Účetní profily odběratele.
2. Klikněte na položku Upravit.
    * Z rozevíracího seznamu vyberte posloupnost upomínek. Pokud nechcete generovat upomínky pro transakce pomocí tohoto účetního profilu, ponechejte toto pole prázdné.  
    * Karta omezení tabulky vám umožní změnit způsob, jakým se zpracovávají upomínky. Je-li toto pole nastaveno na hodnotu Ano, budou u tohoto účetního profilu vytvářeny upomínky.  
3. Zavřete stránku.

## <a name="create-collection-letters"></a>Vytvořit upomínky
1. Přejděte na Úvěry a inkasa > Upomínka > Vytvořit upomínky.
    * Musíte vybrat typy transakcí, pro které budete shromažďovat upomínky. Všechny otevřené transakce pro tyto typy budou zahrnuty do výpočtu.  
2. V poli Upomínka vyberte možnost.
3. Zadejte datum upomínky.
    * Existují dvě možnosti účetního profilu:  Účet – Použít účetní profil, který je přiřazený k účtu odběratele pro jednotlivá oznámení úroků.   Vybrat – Použije se účetní profil vybraný v poli Účetní profil.  
    * Vyberte účetní profil, pokud jste změnili nastavení „Použít účetní profil z“ na možnost „Vybrat“.  
4. Rozbalte oddíl Záznamy k zahrnutí.
5. Klepněte na tlačítko Filtr.
6. Do pole Kritéria v poli Kritéria, zadejte ID zákazníka. Například zadejte 'US-001'..
7. Klikněte na tlačítko OK.
8. Klikněte na tlačítko OK.

## <a name="print-collection-letters"></a>Tisk upomínek
1. Přejděte na Úvěry a inkasa > Upomínka > Zkontrolovat a zpracovat upomínky.
2. V poli Stav vyberte možnost „Vytvořeno“.
3. Vyberte volbu Nevytištěno v poli Vytištěno.
4. Klepněte na položku Tisk.
5. Klikněte na možnost Upomínka.
6. Rozbalte oddíl Záznamy k zahrnutí.
7. Vložení data přerušení pro zaúčtování
8. Kliknutím na OK vytiskněte upomínku.

## <a name="post-the-collection-letter"></a>Zaúčtování upomínky
1. Klikněte na položku Zaúčtovat.
2. Zadejte datum zaúčtování pro upomínku.
3. Rozbalte oddíl Záznamy k zahrnutí.
4. Klikněte na tlačítko OK.
5. V poli Stav vyberte možnost „Zaúčtováno“.
6. Vyberte volbu v poli Vytištěno.



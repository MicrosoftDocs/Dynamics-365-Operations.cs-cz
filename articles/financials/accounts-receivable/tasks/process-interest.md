---
title: Zpracování úroků
description: Tato procedura popisuje způsob tvorby, tisku a zaúčtování oznámení úroků.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5652a38684061914f895d7f8b82999c9840fd63
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1549599"
---
# <a name="process-interest"></a>Zpracování úroků

[!include [task guide banner](../../includes/task-guide-banner.md)]

Tato procedura popisuje způsob tvorby, tisku a zaúčtování oznámení úroků. Tento úkol používá ukázkovou společnost USMF.


## <a name="set-up-interest-on-the-posting-profile"></a>Nastavte úrok v účetním profilu.
1. Přejděte do nabídky na Kredit a inkasa > Nastavení > Účetní profily odběratele.
2. Klikněte na položku Upravit.
    * Vyberte kód úroku z rozevíracího seznamu. Pokud nechcete vypočítat úrok pro transakce pomocí tohoto účetního profilu, ponechejte toto pole prázdné.  
    * Karta Omezení tabulky vám umožní změnit způsob, jakým se zpracovává úrok. Je-li toto pole nastaveno na hodnotu Ano, budou u tohoto účetního profilu vypočteny úroky.  

## <a name="calculate-interest"></a>Vypočítat úroky
1. Přejděte do nabídky Úvěry a inkasa > Úrok > Vytvořit oznámení úroků.
    * Musíte vybrat typy transakcí, pro které budete vypočítávat úrok. Všechny otevřené transakce pro tyto typy budou zahrnuty do výpočtu.  
    * Pokud vyberete Úrok, budete počítat úrok z úroku. Je vhodné zkontrolovat zákony upravující výpočet úroku z úroku před jeho zahrnutím do těchto transakcí.  
    * Úrok se vypočítá od tohoto data do data "Do data". Pokud neurčíte pole „Od data“, pak všechna nezaúčtovaná oznámení úroků budou zrušena a úroky budou přepočítány od data transakce.  
2. Zadejte datum oznámení úroků.
    * Existují tři možnosti účetního profilu:  Účet – Použít účetní profil, který je přiřazený k účtu odběratele pro jednotlivá oznámení úroků.   Vybrat – Použije se účetní profil vybraný v poli Účetní profil.   Transakce – Pomocí individuálního účetního profilu z transakcí, na nichž se počítá úrok pro jednotlivá oznámení úroku. Transakce, které nemají přiřazený účetní profil použijí účetní profil, který je uveden v oblasti Hlavní kniha a DPH formuláře Parametry pohledávek.  
    * Zde vyberte účetní profil, pokud jste změnili nastavení „Použít účetní profil z“ na možnost „Vybrat“.  
3. Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.
4. Klepněte na tlačítko Filtr.
5. Do pole Kritéria zadejte ID zákazníka. Například zadejte 'US-001'..
6. Klikněte na tlačítko OK.
7. Klikněte na tlačítko OK.

## <a name="print-interest-notes"></a>Tisk oznámení úroků
1. Přejděte do nabídky Úvěry a inkasa > Úrok > Zkontrolovat a zpracovat oznámení úroků.
2. V poli Stav vyberte možnost „Vytvořeno“.
3. Vyberte volbu Nevytištěno v poli Vytištěno.
4. Klepněte na položku Tisk.
5. Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.
6. Klikněte na tlačítko OK.
7. Zavřete stránku.

## <a name="post-the-interest-note"></a>Zaúčtování oznámení úroků
1. Vyberte oznámení úroků, které je připraveno k zaúčtování (stav je vytvořen).
2. Klikněte na položku Zaúčtovat.
3. Zadejte datum účtování pro oznámení úroků.
    * Chcete-li pro oznámení úroků vytvořit jednu transakci hlavní knihy, vyberte Ano.     Pokud políčko Ano nevyberete, bude úrok všech oznámení úroků odběrateli kumulován a zaúčtován do hlavní knihy jako jedna transakce.  
4. Rozbalte nebo sbalte oddíl Záznamy k zahrnutí.
5. Klikněte na tlačítko OK.
6. V poli Stav vyberte možnost „Zaúčtováno“.


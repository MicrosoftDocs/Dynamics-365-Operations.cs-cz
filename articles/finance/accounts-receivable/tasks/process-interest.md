---
title: Zpracování úroků
description: Tato procedura popisuje způsob tvorby, tisku a zaúčtování oznámení úroků.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustPosting, SysQueryForm, CustInterestNote, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 093fbd23f9fcaf62db9988a98a94b8cebf582768
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441178"
---
# <a name="process-interest"></a>Zpracování úroků

[!include [banner](../../includes/banner.md)]

Tato procedura popisuje způsob tvorby, tisku a zaúčtování oznámení úroků. Tento úkol využívá ukázkovou společnost USMF.


## <a name="set-up-interest-on-the-posting-profile"></a>Nastavte úrok v účetním profilu.
1. V **Navigačním podokně** přejděte na **Moduly > Kredit a inkasa > Nastavení > Účetní profily odběratele**.
2. Klikněte na možnost **Upravit**.
3. Na pevné záložce **Nastavení** v poli **Kód úroku** vyberte kód úroku z rozevíracího seznamu. Pokud nechcete vypočítat úrok pro transakce pomocí tohoto účetního profilu, ponechejte toto pole prázdné. Pevná záložka **Omezení tabulky** vám umožní změnit způsob, jakým se zpracovává úrok. Je-li toto pole nastaveno na hodnotu Ano, budou u tohoto účetního profilu vypočteny úroky.  

## <a name="calculate-interest"></a>Vypočítat úroky
1. V **Navigačním podokně** přejděte na **Moduly > Kredit a inkasa > Úrok > Vytvořit oznámení úroků**.
2. Musíte vybrat typy transakcí, pro které budete vypočítávat úrok. Všechny otevřené transakce pro tyto typy budou zahrnuty do výpočtu.  
3. Pokud nastavíte **Úrok** na ‚Ano‘, budete počítat úrok z úroku. Je vhodné zkontrolovat zákony upravující výpočet úroku z úroku před jeho zahrnutím do těchto transakcí.  
4. V poli **Od data** zadejte datum, od kterého se bude úrok počítat. Pokud neurčíte pole **Od data**, pak všechna nezaúčtovaná oznámení úroků budou zrušena a úroky budou přepočítány od data transakce.
5. V poli **Do data** zadejte datum, do kterého se bude úrok počítat.
6. V poli **Použít účetní profil od** je nutné vybrat nějakou možnost. Existují tři možnosti účetního profilu:
    - Účet – Pro každé oznámení úroku použije účetní profil přiřazený účtu odběratele. 
    - Vybrat – Použije se účetní profil vybraný v poli Účetní profil.
    - Transakce – Pomocí individuálního účetního profilu z transakcí, na nichž se počítá úrok pro jednotlivá oznámení úroku. Transakce, které nemají přiřazený účetní profil použijí účetní profil, který je uveden v oblasti Hlavní kniha a DPH formuláře Parametry pohledávek.  
7. Rozbalte pevnou záložku **Záznamy k zahrnutí**.
8. Klikněte na tlačítko **Filtr**.
9. Do pole **Kritéria** zadejte ID zákazníka. Například zadejte 'US-001'.
6. Klikněte na tlačítko **OK**.
7. Klikněte na tlačítko **OK**.

## <a name="print-interest-notes"></a>Tisk oznámení úroků
1. V **Navigačním podokně** přejděte na **Moduly > Kredit a inkasa > Úrok > Zkontrolovat a zpracovat oznámení úroků**.
2. V poli **Stav** vyberte možnost „Vytvořeno“.
3. V poli **Vytištěno** vyberte volbu ‚Nevytištěno‘.
4. Klepněte na položku **Tisk**.
5. Rozbalte pevnou záložku **Záznamy k zahrnutí**.
6. Klikněte na tlačítko **OK**.
7. Zavřete stránku.

## <a name="post-the-interest-note"></a>Zaúčtování oznámení úroků
1. Vyberte oznámení úroků, které je připraveno k zaúčtování (stav je vytvořen).
2. Klikněte na možnost **Zaúčtovat**.
3. Zadejte datum účtování pro oznámení úroků. Chcete-li pro oznámení úroků vytvořit jednu transakci hlavní knihy, vyberte Ano. Pokud políčko Ano nevyberete, bude úrok všech oznámení úroků odběrateli kumulován a zaúčtován do hlavní knihy jako jedna transakce.  
4. Rozbalte pevnou záložku **Záznamy k zahrnutí**.
5. Klikněte na tlačítko **OK**.
6. V poli **Stav** vyberte možnost „Zaúčtováno“.


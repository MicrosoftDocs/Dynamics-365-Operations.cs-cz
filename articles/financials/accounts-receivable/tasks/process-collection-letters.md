--- 
title: "Zpracování upomínek"
description: "Tato procedura popisuje způsob tvorby, tisku a zaúčtování upomínek."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 12/04/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.translationtype: HT
ms.sourcegitcommit: 075d0f5dc0c9dc4e46dc92a2da75da9f7a207472
ms.openlocfilehash: 33d9fd62a780ab109474eefa9e322a9c529f9e72
ms.contentlocale: cs-cz
ms.lasthandoff: 12/06/2018

---
# <a name="process-collection-letters"></a>Zpracování upomínek

[!include [banner](../../includes/banner.md)]

Tato procedura popisuje způsob tvorby, tisku a zaúčtování upomínek. Tento úkol používá ukázkovou společnost USMF.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Nastavení posloupnosti upomínek v účetním profilu
1. Přejděte na **Kredit a inkasa > Nastavení > Účetní profily odběratele**.
2. Klikněte na možnost **Upravit**.
3. Z rozevíracího seznamu vyberte posloupnost upomínek. Pokud nechcete generovat upomínky pro transakce pomocí tohoto účetního profilu, ponechejte toto pole prázdné.  
4. Rozbalte kartu omezení tabulky, což umožní změnit způsob, jakým se zpracovávají upomínky. Je-li toto pole nastaveno na hodnotu **Ano**, budou u tohoto účetního profilu vytvářeny upomínky.  

## <a name="create-collection-letters"></a>Vytvořit upomínky
1. Přejděte na **Úvěry a inkasa > Upomínka > Vytvořit upomínky**.
2. Vyberte typy transakcí, pro které budete shromažďovat upomínky. Všechny otevřené transakce pro tyto typy budou zahrnuty do výpočtu.  
2. V poli **Upomínka** vyberte možnost.
3. Zadejte datum upomínky.
4. Vyberte účetní profil, pokud jste změnili nastavení **Použít účetní profil z** na možnost **Vybrat**. Existují dvě možnosti účetního profilu:   
   - **Účet** – Pro každé oznámení úroku použije účetní profil přiřazený účtu odběratele.   
   - **Vybrat** – Použije se účetní profil vybraný v poli **Účetní profil**.  
5. Rozbalte oddíl **Záznamy k zahrnutí**.
6. Klikněte na tlačítko **Filtr**.
7. Do pole **Kritéria** zadejte ID zákazníka. Například zadejte 'US-001'.
8. Klikněte na tlačítko **OK**.
9. Klikněte na tlačítko **OK**.

## <a name="print-collection-letters"></a>Tisk upomínek
1. Přejděte na **Úvěry a inkasa > Upomínka > Zkontrolovat a zpracovat upomínky**.
2. V poli **Stav** vyberte možnost **Vytvořeno**.
3. Vyberte volbu **Nevytištěno** v poli **Vytištěno**.
4. Klepněte na položku **Tisk**.
5. Klikněte na možnost **Upomínka**.
6. Rozbalte oddíl **Záznamy k zahrnutí**.
7. Vložení data přerušení pro zaúčtování.
8. Kliknutím na **OK** vytiskněte upomínku.
9. Zaúčtování upomínky.
   1. Klikněte na možnost **Zaúčtovat**.
   2. Zadejte datum zaúčtování pro upomínku.
   3. Rozbalte oddíl **Záznamy k zahrnutí**.
   4. Klikněte na tlačítko **OK**.
   5. V poli **Stav** vyberte možnost **Zaúčtováno**.
   6. Vyberte volbu v poli **Vytištěno**.

## <a name="control-collection-letters-at-the-customer-level"></a>Ovládací prvek upomínky na úrovni odběratelů
Upomínky lze také nastavit na úrovni odběratele, tak aby byl sledován kód upomínky pro každou transakci, ale zpracování upomínky bylo založeno na jedné úrovni upomínky, která je pro odběratele uložena. Jedna upomínka bude obsahovat všechny transakce, které jsou pro odběratele po splatnosti. Vzhledem k tomu, že se dny odkladu nyní sledují na úrovni odběratele, nebude další upomínka odeslána, dokud neuplyne počet dní odkladu pro další upomínku v pořadí, a to i přesto, že budou transakce po odeslání poslední upomínky po splatnosti. Tato možnost sníží počet upomínek odeslaných pro každého zákazníka. 

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Nastavení odběratele na kontrolu upomínek na úrovni odběratelů
1.  Přejděte na **Kredit a inkasa > Nastavení > Parametry závazků** a klikněte na kartu **Inkasa**. 
2.  Změňte hodnotu **vytvořit upomínku pro** na **Odběratel**. 
3.  Přejděte na **Úvěry a inkasa > Upomínka > Zkontrolovat a zpracovat upomínky**. Vygeneruje se pouze jedna upomínka pro odběratele se všemi transakcemi po splatnosti.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Ignorovat platby a dobropisy pro výpočet kódu upomínky
Pokud zahrnete transakce a upomínky do transakcí, které budou zahrnuty v upomínkách, můžete mít platby nebo dobropisy, které vyvolají upomínku. Můžete určovat, jak platby a dobropisy určují kód upomínky, změnou hodnoty parametru **Ignorovat platby a dobropisy při výpočtu kódu upomínky**. 

Pokud chcete ignorovat platby a dobropisy pro výpočet kódu upomínky, postupujte následovně:
1. Přejděte na **Kredit a inkasa > Nastavení > Parametry závazků** a klikněte na kartu **Inkasa**. 
2. Změňte hodnotu možnosti **ignorovat platby a dobropisy pro výpočet kódu upomínky na** **Ano**.


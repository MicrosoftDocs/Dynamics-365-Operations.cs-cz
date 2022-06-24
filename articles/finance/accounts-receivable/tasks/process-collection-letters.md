---
title: Zpracování upomínek
description: Tento článek popisuje způsob tvorby, tisku a zaúčtování upomínek.
author: ShivamPandey-msft
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, CustCollectionLetterNote
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-12-01
ms.dyn365.ops.version: 8.1.3
ms.openlocfilehash: fbca4acf30e2c58d8bb615d659b883b574a12aa7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909120"
---
# <a name="process-collection-letters"></a>Zpracování upomínek

[!include [banner](../../includes/banner.md)]

Tento článek popisuje způsob tvorby, tisku a zaúčtování upomínek. Tento úkol využívá ukázkovou společnost USMF.

## <a name="set-up-a-collection-letter-sequence-on-the-posting-profile"></a>Nastavení posloupnosti upomínek v účetním profilu
1. Přejděte na **Navigační podokno > Moduly > Kredit a inkasa > Nastavení > Účetní profily odběratele**.
2. Klikněte na možnost **Upravit**.
3. Z rozevíracího seznamu vyberte posloupnost upomínek. Pokud nechcete generovat upomínky pro transakce pomocí tohoto účetního profilu, ponechejte toto pole prázdné.  
4. Rozbalte kartu **Omezení tabulky**, což umožní změnit způsob, jakým se zpracovávají upomínky. Je-li toto pole nastaveno na hodnotu **Ano**, budou u tohoto účetního profilu vytvářeny upomínky.  

## <a name="create-collection-letters"></a>Vytvořit upomínky
1. Přejděte na **Navigační podokno > Moduly > Kredit a inkasa > Upomínka > Vytvořit upomínky**.
2. Vyberte typy transakcí, pro které budete shromažďovat upomínky. Všechny otevřené transakce pro tyto typy budou zahrnuty do výpočtu.  
3. V poli **Upomínka** vyberte možnost.
4. Do pole **Datum upomínky** zadejte datum upomínky.
5. Vyberte účetní profil, pokud jste změnili nastavení **Použít účetní profil z** na možnost **Vybrat**. Existují dvě možnosti účetního profilu:   

   - **Účet** – Pro každé oznámení úroku použije účetní profil přiřazený účtu odběratele.   
   - **Vybrat** – Použije se účetní profil vybraný v poli **Účetní profil**.  

6. Rozbalte oddíl **Záznamy k zahrnutí**.
7. Vyberte **Filtr**.
8. Do pole **Kritéria** zadejte ID zákazníka. Například zadejte 'US-001'.
9. Vyberte **OK**.
10. Vyberte **OK**.

## <a name="print-collection-letters"></a>Tisk upomínek
1. Přejděte na **Navigační podokno > Moduly > Kredit a inkasa > Upomínka > Zkontrolovat a zpracovat upomínky**.
2. V poli **Stav** vyberte možnost **Vytvořeno**.
3. Vyberte volbu **Nevytištěno** v poli **Vytištěno**.
4. Vyberte **Tisk**.
5. Vyberte možnost **Upomínka**.
6. V oddílu **Parametry** zadejte datum přerušení pro zaúčtování.
7. Rozbalte část **Záznamy k zahrnutí** a zadejte podrobnosti o upomínce.
8. Výběrem **OK** vytiskněte upomínku.
9. Zaúčtování upomínky.

    1. Zvolte **Zaúčtovat**.
    1. Zadejte datum zaúčtování pro upomínku.
    1. Rozbalte oddíl **Záznamy k zahrnutí**.
    1. Vyberte **OK**.
    1. V poli **Stav** vyberte možnost **Zaúčtováno**.
    1. Vyberte volbu v poli **Vytištěno**.

## <a name="control-collection-letters-at-the-customer-level"></a>Ovládací prvek upomínky na úrovni odběratelů
Pokud jsou upomínky nastaveny na úrovni transakce, může být pro odběratele generováno více upomínek na základě splatnosti transakce. Pokud se transakce zobrazují v jiných posloupnostech upomínek, budou pro každou skupinu zpožděných transakcí pro odběratele generovány samostatné upomínky. Z toho vyplývá, že jednotlivý odběratel může například obdržet jednu upomínku pro transakce, které jsou 60 dnů po splatnosti, a další upomínku pro transakce, které jsou 90 dnů po splatnosti. 

Každá upomínka je také přidružena ke kódu upomínky. Kód upomínky je přidružen k jednotlivým transakcím a používá se k určení, kdy by měla být pro každou transakci vygenerována následující upomínka. Pokud je například transakce zpožděna o více než 30 dní, kód upomínky určí, že následující upomínka bude odeslána, když bude transakce zpožděna o 60 dní, pokud není uhrazena dříve. 

Upomínky lze také nastavit na úrovni odběratele. V tomto případě je sledován kód upomínky pro každou transakci, ale zpracování upomínky bylo založeno na jedné úrovni upomínky, která je pro odběratele uložena. Jedna upomínka bude obsahovat všechny transakce, které jsou pro odběratele po splatnosti. Vzhledem k tomu, že se dny odkladu nyní sledují na úrovni odběratele, nebude další upomínka odeslána, dokud neuplyne počet dní odkladu pro další upomínku v pořadí, a to i přesto, že budou transakce po odeslání poslední upomínky po splatnosti. Tato možnost pomáhá snížit počet upomínek, které musíte odeslat každému zákazníkovi.

### <a name="set-up-the-customer-to-control-collection-letters-at-the-customer-level"></a>Nastavení odběratele na kontrolu upomínek na úrovni odběratelů
1.  Přejděte na **Navigační podokno > Moduly > Kredit a inkasa > Nastavení > Parametry závazků** a vyberte kartu **Inkasa**. 
2.  Změňte hodnotu **vytvořit upomínku pro** na **Odběratel**. 
3.  Přejděte na **Navigační podokno > Moduly > Kredit a inkasa > Upomínka > Zkontrolovat a zpracovat upomínky**. Vygeneruje se pouze jedna upomínka pro odběratele se všemi transakcemi po splatnosti.

## <a name="ignore-payments-and-credit-memos-when-calculating-the-collection-letter-code"></a>Ignorovat platby a dobropisy pro výpočet kódu upomínky
Pokud zahrnete transakce a upomínky do transakcí, které budou zahrnuty v upomínkách, můžete mít platby nebo dobropisy, které vyvolají upomínku. Můžete určovat, jak platby a dobropisy určují kód upomínky, změnou hodnoty parametru **Ignorovat platby a dobropisy při výpočtu kódu upomínky**. 

Pokud chcete ignorovat platby a dobropisy pro výpočet kódu upomínky, postupujte následovně:

1. Přejděte na **Navigační podokno > Moduly > Kredit a inkasa > Nastavení > Parametry závazků** a klikněte na kartu **Inkasa**. 
2. Změňte hodnotu možnosti **ignorovat platby a dobropisy pro výpočet kódu upomínky na** **Ano**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

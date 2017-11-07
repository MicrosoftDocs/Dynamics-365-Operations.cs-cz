---
title: "Vrácení platby dodavatele"
description: "Tento článek popisuje rozdíly mezi stornováním, odstraněním, anulováním a odmítnutím platby. Dále popisuje dva způsoby stornování kontroly dodavatele."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankChequeTable, LedgerJournalTransBankChequeReversal, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14361
ms.assetid: 9f0a1883-cbe0-4cc7-b9f3-dd12fb85ebe8
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 736432a7e128f6b7b0d7ed5e0156c0769407bbaa
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---

# <a name="reverse-a-vendor-payment"></a>Vrácení platby dodavatele

[!include[banner](../includes/banner.md)]


Tento článek popisuje rozdíly mezi stornováním, odstraněním, anulováním a odmítnutím platby. Dále popisuje dva způsoby stornování kontroly dodavatele. 

V některých případech po zaúčtování platby dodavatele se platba musí vrátit. Vrácení se liší od odstranění, anulování nebo zamítnutí platby. Platbu můžete odstranit pouze v případě, že je ve stavu **Vytvořeno**. Tento stav označuje, že platba byla vytvořena, ale ještě nebyla vygenerována. Toto omezení platí vždy, bez ohledu na způsob platby. Můžete zrušit neodeslané šeky poté, co byly vygenerovány, ale předtím, než budou odeslány. Pokud se vygenerovaná platba provádí jako elektronický převod prostředků (EFT), platbu můžete odmítnout ještě před odesláním. Pokud chcete odmítnout platbu, změnte hodnotu **Stavu platby**. Platba, která byla zrušena nebo odmítnuta, může být obnovena nastavením **Stavu platby** na hodnotu **Žádná**. 

Po odeslání platby se použijí reverzace. Platby, které jsou provedeny elektronicky nelze již po odeslání vrátit zpět. Namísto toho musí být vytvořena nová transakce na danou částku, aby se závazek vrátil zpět na účet dodavatele. Pro stornování zaúčtovaných šeků jsou k dispozici dvě metody. V jedné metodě jsou storna účtována okamžitě po klepnutí na tlačítko **Storno platby** na stránce **Zkontrolovat**. Ve druhé metodě bude po klepnutí na tlačítko **Storno plateb** na stránce **Zkontrolovat** stornovaná transakce odeslána do deníku stornování šeků v modulu Správa hotovosti a banky, kde poté může posuzující uživatel tuto stornovanou transakci zaúčtovat nebo zrušit. 

Informace o metodě, kterou vaše organizace používá, naleznete na stránce **Parametry pokladny a banky**. Pokud je možnost **Použít proces kontroly pro storna plateb** nastavena na **Ano**, jsou storna odesílána ke kontrole deníku stornování šeků. Následující tabulka popisuje, jak se metody stornování šeků liší.

| Pokud vaše organizace nekontroluje stornování šeků před zaúčtováním                                                                                                                                  | Pokud vaše organizace kontroluje stornování šeků před zaúčtováním                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Šek je stornován ihned po klepnutí na tlačítko **OK** na stránce **Zkontrolovat**.                                                                                                                      | Šek není okamžitě stornován. Je vytvořen deník stornování šeků ke kontrole. Pokud dojde k odstranění deníku stornování šeků, šek lze znovu stornovat.                                                                                                                                                                                                                                                                |
| Účetní položky pro původní šek budou stornovány.                                                                                                                                         | Účet hlavní knihy z původního účetního zápisu šek nemusí být zaúčtován. Finanční dimenze z původního deníku šeku jsou výchozí finanční dimenze v deníku stornování šeků. Tyto výchozí hodnoty lze změnit. Při zaúčtování deníku stornování šeků, jsou hlavních účty pro modul Závazky zadány automaticky z účetních profilů, které mohly být změněny. |
| Účetní struktury používané při zaúčtování původního šek jsou využity ke stornování šeku, i v případě, že byla účetní struktura změněna. Kombinace účtů není ověřena. | Pokud došlo ke změně účetní struktury po zaúčtování původního šeku, může být vyžadována pro stornování šeku nová finanční dimenze. Tato finanční dimenze nemusí být zadána automaticky z deníku pro původní platbu. Kombinace účtu je ověřena při zaúčtování storna šeku.                                                                                                        |
| Pevné dimenze se nepoužívají pro stornování k zajištění toho, že budou stornovány stejné účty hlavní knihy.                                                                                      | Pevné dimenze jsou použity při zaúčtování do deníku stornování šeků. Hodnota finanční dimenze nemusí existovat v účetním záznamu pro původní šek v závislosti na tom, kdy byla pevná dimenze definována.                                                                                                                                                                                                     |

## <a name="reverse-posted-checks-without-reviewing-them"></a>Stornování zaúčtovaných šeků bez prohlížení
Pokud vaše organizace chce zaúčtovat stornování šeků ihned po klepnutí na tlačítko **Storno plateb** na stránce **Šeky**. Na stránce **Parametry řízení hotovosti a banky** nastavte možnost **Použít proces kontroly pro storna plateb** na **Ne**. Na stránce **Šeky** lze vybrat šek, který chcete stornovat, a vybrat **Storno platby**. Můžete zadat datum a vybrat důvod stornování.

## <a name="reverse-posted-checks-after-they-are-reviewed-in-the-check-reversal-journal"></a>Stornování zaúčtovaných šeků po jejich zkontrolování v deníku stornování šeků
Pokud vaše organizace chce zkontrolovat stornování šeků před jejich zaúčtováním, vytvořte deník stornování šeků ke kontrole a na stránce **Parametry řízení hotovosti a banky** nastavte možnost **Použít proces kontroly pro storna plateb** na **Ano**. Na stránce **Šeky** lze vybrat šek, který chcete stornovat, a vybrat **Storno platby**. Můžete zadat datum a vybrat důvod stornování. Musíte vybrat také název deníku pro vytvoření deníku v deníku stornování šeku.

### <a name="review-a-reversal"></a>Kontrola storna

Jste-li uživatelem, který kontroluje storna, můžete buď schválit a zaúčtovat deník, nebo zamítnout storno odstraněním deníku. Na stránce **Deník stornování šeků** můžete vybrat deník stornování ke kontrole a kliknout na tlačítko **Řádky**. Můžete zkontrolovat stornované deníky a vybrat jednu z následujících možností schválení:

-   Chcete-li schválit a zaúčtovat deník stornování, klepněte na položku **Zaúčtovat** nebo na položku **Zaúčtovat a převést**.
-   Chcete-li storno odmítnout, odstraňte deník storna šeku.

> [!NOTE]
> Pokud odstraníte deník, storno se odstraní ze systému, ovšem původní šek zůstane na stránce **Šek**. Šek již poté nebude ve stavu **Čekající zrušení**.

## <a name="results-of-posting-a-reversal"></a>Výsledky zaúčtování storna
Při zaúčtování storna dojde k následujícím akcím:

-   Stav šeku bude aktualizován na stav **Zrušení**.
-   Pokud je vybrána možnost **Odsouhlasení** v průběhu stornování na stránce Storno, dojde k odsouhlasení šeku (vybrána možnost **Odsouhlaseno**) a nebude zobrazen na stránce **Odsouhlasení účtu**.
-   Doklad stornování je zaúčtován oproti bankovnímu účtu, ze kterého byl šek vydán, a zvýší tak zůstatek na bankovním účtu.
-   Doklad je zaúčtován do hlavní knihy.
-   Podrobnosti úprav jsou aktualizovány ve skupině polí **Historie** na stránce **Šek**.

> [!NOTE] 
> Při stornování šeku vydaného pro mezipodnikovou obchodní transakci vycházejí souvztažné položky z nastavení účetnictví a ne z původní transakce. Pokud byl stornovaný šek vydán pro platbu dodavateli, může dojít také k následujícím akcím:

-   Původní platbu na faktuře, oproti které byla platba vyrovnána, nelze použít (vyrovnání je stornováno).
-   Transakce je zaúčtována oproti účtu dodavatele jako storno platby a storno platby je vyrovnáno oproti původní platbě. Pole **Poslední doklad vyrovnání** na stránce **Transakce dodavatele** původní úhrady dodavateli je aktualizováno, aby reflektovalo číslo dokladu stornované transakce.

Pokud byl stornovaný šek vydán pro refundaci odběratele, může dojít také k následujícím akcím:

-   Transakce je zaúčtována oproti účtu odběratele jako storno platby a vyrovnání mezi původní platbou a dokumentem, oproti kterému byla platba původně vyrovnána, je stornováno (je vytvořena záporná platba).
-   Na původní platbu je použito storno platby. Pole **Poslední doklad vyrovnání** na stránce **Transakce odběratele** původní platby odběrateli je aktualizováno, aby reflektovalo číslo dokladu stornované transakce.






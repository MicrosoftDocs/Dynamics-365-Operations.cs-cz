---
title: Přecenění měny pro závazky a pohledávky
description: Toto téma poskytuje informace o procesu přecenění cizí měny, kterého lze využít pro aktualizaci hodnoty otevřených transakcí v modulu Závazky a pohledávky.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustExchRateAdjustment, VendExchRateAdjustment
audience: Application User
ms.reviewer: kfend
ms.custom: 14211
ms.assetid: defb1ea5-1f3e-4859-87d8-3f9954d3f388
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cf32a31df1d56740d803b97d65829b1b1d31eb17
ms.sourcegitcommit: d1683d033fc74adbc4465dd26f7b0055e7639753
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/05/2022
ms.locfileid: "8713917"
---
# <a name="currency-revaluation-for-accounts-payable-and-accounts-receivable"></a>Přecenění měny pro závazky a pohledávky

[!include [banner](../includes/banner.md)]

Teoretická hodnota (účetní hodnota) otevřených transakcí v zahraničních měnách se průběžně liší z důvodu fluktuací směnných kurzů. Toto téma poskytuje informace o procesu přecenění cizí měny, kterého lze využít pro aktualizaci hodnoty otevřených transakcí v modulu Závazky a pohledávky. 

Teoretická hodnota nebo účetní hodnota otevřených transakcí v zahraničních měnách se průběžně liší z důvodu fluktuací směnných kurzů. Chcete-li aktualizovat hodnotu otevřených transakcí v modulu Závazky a pohledávky, spusťte proces přecenění cizí měny. Přecenění cizí měny lze spustit pro závazky a pohledávky. Proces používá nový směnný kurz pro přecenění otevřených částek nebo nevyrovnaných částek k určitému datu. Rozdíly mezi původními zaúčtovanými částkami a přehodnocenými částkami způsobí nerealizovaný zisk nebo ztrátu každé otevřené transakce. Dílčí knihy pro závazky a pohledávky účty jsou pak aktualizovány, aby odrážely nerealizovaný zisk nebo ztrátu a účetní položka je zaúčtována do hlavní knihy.

## <a name="simulate-a-foreign-currency-revaluation"></a>Simulovat přecenění cizí měny
Dříve, než přeceníte částky v cizí měně pro otevřené transakce, můžete použít sestavu pro simulaci přecenění cizí měny pro stejné datum a způsob. Spustit sestavu simulace můžete na stránce **přecenění cizí měny** kliknutím na tlačítko **Simulace**. Tato sestava poskytuje náhled na částku nerealizovaného zisku nebo ztráty na základě parametrů, které jsou definovány pro simulaci.

## <a name="process-a-foreign-currency-revaluation"></a>Zpracování přecenění cizí měny
Na stránce **Přecenění cizí měny** v části **Pravidelné úlohy** proveďte přecenění otevřených transakcí. Proces můžete spustit v reálném čase nebo naplánovat jeho spuštění použitím dávky. Při definování nastavení pro proces přecenění nezapomeňte ověřit, zda chcete vytisknout sestavu výsledků. Po dokončení procesu nemůže být sestava přecenění znovu vytištěna. Pokud generujete sestavu přecenění cizí měny, zobrazí se v ní různé zůstatky na úrovni odběratele/dodavatele a úrovni měny:

-   Zůstatky odběratelů nebo dodavatelů, kteří mají transakce v cizí měně, které mají být přehodnoceny. Následující zůstatky jsou určeny:
    -   Celkový původní zůstatek v cizí měně.
    -   Celková částka přecenění cizí měny v zúčtovací měně, stejné jako u předchozího přecenění.
    -   Celková částka přecenění cizí měny v zúčtovací měně, stejné jako u stávajícího přecenění.
    -   Rozdíl mezi předchozím a stávajícím přeceněním. Tato odchylka je další nerealizovaný zisk nebo ztráta.
-   Celkový nerealizovaný zisk nebo ztráta pro každou měnu.

Při každém spuštění přecenění cizí měny je vytvořen záznam. Ze záznamu na stránce **Zhodnocení cizí měny** vyberte **Transakce** pro zobrazení podrobného seznamu transakcí, které byly vytvořeny z důvodu přecenění. Každý doklad o transakci představuje otevřenou transakci, která byla přehodnocena. Pokud byla otevřená transakce přeceněna více než jednou, zobrazí se dva záznamy, které používají stejný doklad. Jeden záznam bude pro storno předchozího nerealizovaného zisku nebo ztráty a ostatní záznamy budou pro nový nerealizovaný zisk nebo ztrátu. Spusťte proces přecenění klepnutím na tlačítko **Přecenění cizí měny**. Definujte vhodné nastavení pro následující parametry:

-   **Metoda** – Metoda použitá u vybrané úlohy přecenění cizí měny:
    -   **Standardní** – úlohy přecenění cizí měny jsou zaúčtovány bez ohledu na to, zda je výsledkem zisk nebo ztráta.
    -   **Minimální** – úlohy přecenění cizí měny budou jsou zaúčtovány pouze tehdy, pokud je výsledkem ztráta.
    -   **Datum faktury** – úlohy přecenění cizí měny využívají původní směnný kurz transakcí, které jsou přehodnoceny na původní hodnotu v zúčtovací měně. Platnost všech předchozích přecenění cizí měny byla zrušena.
-   **Rozhodné datum** – Datum, kdy byly nalezeny všechny transakce, které mají otevřené (nevyrovnané) částky pro toto datum. Částky v cizí měně jsou přehodnoceny pomocí směnných kurzů, které jsou zadány na stránce **Směnné kurzy měn** pro zvažované datum. Když jsou částky v cizí měně přehodnoceny ke zvažovanému datu, toto datum se stane datem posledního přecenění cizí měny pro transakce, které byly upraveny. Pokud se rozhodnete spustit přecenění cizí měny pro zvažované datum dřívější, než je datum posledního přecenění cizí měny v již upravených transakcích, transakce otevřené v dřívějším zvažovaném datu, které však mají pozdější poslední data přecenění cizí měny, nejsou upraveny periodickou úlohou.
-   **Datum kurzu** – Datum, které určuje směnný kurz použitý u přecenění cizí měny.
-   **Použít účetní profil z** – účetní profil, který se používá k zadání výchozího hlavního účtu pro pohledávky a závazky pro účetní položky u transakcí přecenění cizí měny:
    -   **Zaúčtování** – Použije se účetní profil transakce odběratele.
    -   **Vybrat** - Zadejte účetní profil v poli **Účetní profil**.
-   **Účetní profil** – Je-li v poli **Použít účetní profil z** vybrána možnost **Vybrat**, zadaný účetní profil v tomto poli určuje účetní profil u transakcí zaměřených na přecenění cizí měny.
-   **Finanční dimenze** – finanční dimenze, které jsou zaúčtovány u účetních záznamů v transakcích zaměřených na přecenění cizí měny. Finanční dimenze nejsou ověřeny podle pravidel pro strukturu účtu. Struktura účtu, která byla zavedena v době zaúčtování faktur, nemusí být stejná jako pravidla, která platila po dokončení přeceňování. V procesu přecenění není možné vybrat konkrétní finanční dimenze, proto se ověření struktury účtu přeskočí.  
    -   **Žádná** – nejsou zaúčtovány žádné finanční dimenze. Používáte-li požadovanou finanční dimenzi ve vaší účetní struktuře, proces přecenění stále probíhá a vytvoří účetní položky, které nemají žádné finanční dimenze. Nejprve se zobrazí zpráva s upozorněním, po které můžete zrušit přecenění.
    -   **Tabulka** – finanční dimenze účtu odběratele nebo dodavatele jsou zaúčtovány v transakcích zaměřených na přecenění cizí měny.
    -   **Zaúčtování** – finanční dimenze transakce, která je právě přehodnocena, je zaúčtována v transakcích zaměřených na přecenění cizí měny. Ve výchozím nastavení budou finanční dimenze z účtu hlavní knihy původní transakce pohledávek a závazků použity pro transakce přecenění hlavního účtu pohledávek/závazků a finanční dimenze z účtu hlavní knihy majetku/výdajů/příjmů původní transakce se použijí pro transakce přecenění hlavního účtu nerealizovaného zisku/ztráty.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]

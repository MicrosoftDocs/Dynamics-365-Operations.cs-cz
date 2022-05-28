---
title: Odsouhlasení bankovního výpisu pomocí rozšířeného odsouhlasení banky
description: Funkce Rozšířené odsouhlasení banky umožňuje importovat elektronické bankovní výpisy a automaticky je odsouhlasit z bankovních transakcí v aplikaci Microsoft Dynamics 365 Finance. Toto téma popisuje proces odsouhlasení.
author: moaamer
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationWorksheet
audience: Application User
ms.reviewer: kfend
ms.custom: 98243
ms.assetid: 9df13adf-aa9d-4f6b-bde6-25a214611692
ms.search.region: global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 27956cbc4d51c1b907138b49947b57a570d98da1
ms.sourcegitcommit: 631d2cea52590af15f208e9af584446e85540fcf
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/07/2022
ms.locfileid: "8727559"
---
# <a name="reconcile-bank-statements-by-using-advanced-bank-reconciliation"></a>Odsouhlasení bankovního výpisu pomocí rozšířeného odsouhlasení banky

[!include [banner](../includes/banner.md)]

Funkce Rozšířené odsouhlasení banky umožňuje importovat elektronické bankovní výpisy a automaticky je odsouhlasit z bankovních transakcí v aplikaci Dynamics 365 Finance. Toto téma popisuje proces odsouhlasení.  

## <a name="import-an-electronic-bank-statement"></a>Import elektronického bankovního výpisu

Import bankovních výpisů je možný pomocí akce **Import výpisu** na stránce **Bankovní výpisy**. V bankovním výpisu je bankovní účet identifikován skrze kombinaci hodnot, které jsou nastaveny v údajích o bankovním účtu. Mezi tyto hodnoty patří název banky, číslo bankovního účtu, směrovací číslo, kód SWIFT (Society for Worldwide Interbank Financial Telecommunication) a číslo IBAN (International Bank Account Number). 

Můžete odeslat bankovní výpis, který obsahuje informace pro jeden účet nebo více účtů. Pokud existuje více účtů, účty mohou náležet k různým právnickým osobám.

-   Chcete-li importovat jeden soubor bankovního příkazu pro jeden účet, nastavte možnost **Importovat výpis pro více bankovních účtů se všemi právnickými osobami** na **Ne** a vyberte bankovní účet, který je spojen s výpisem. Kliknutím na tlačítko **Procházet** vyberte přiřazený soubor bankovního výpisu a klepněte na tlačítko **Odeslat**.
-   Chcete-li importovat jeden soubor bankovního výpisu pro více účtů, nastavte možnost **Importovat výpis pro více bankovních účtů se všemi právnickými osobami** na **Ano**. Kliknutím na tlačítko **Procházet** vyberte přiřazený soubor bankovního výpisu a klepněte na tlačítko **Odeslat**.

Pokud některý výpis v elektronickém souboru nelze přiřadit k bankovnímu účtu nebo pokud je přiřazen více bankovním účtům pomocí identifikačních polí, nebude importován. Lze však stále importovat jiné výpisy v souboru. Uživatel obdrží zprávu, že se import bankovních výpisů pro konkrétní bankovní účty nezdařil. Mějte prosím na paměti, že uživatel, který importuje soubor s bankovním výpisem, musí mít přístup k právnické osobě, aby mohl importovat výpisy z bankovních účtů této právnické osoby. 

Více souborů výpisu lze také uložit do aplikace Finance v jediném procesu, a to pomocí souboru zip. Chcete-li importovat více souborů bankovního výpisu pro více účtů, zkombinujte všechny soubory bankovních výpisů do jednoho souboru zip. V dialogovém okně **Importovat bankovní výpisy** nastavte **Importovat výpis pro více bankovních účtů ve všech právnických osobách** na **Ano**. Kliknutím na tlačítko **Procházet** vyberte soubor zip obsahující soubory bankovního výpisu a klepněte na tlačítko **Odeslat**. Proces importu rozpozná soubor .zip a nahraje každý zahrnutý výpis, bez ohledu na bankovní účet právnické osoby.

Je k dispozici možnost **Po importu odsouhlasit**. Pokud tuto možnost nastavíte na **Ano**, systém automaticky ověří bankovní výpis, vytvoří nové odsouhlasení bankovního účtu a list a spustí po odeslání bankovního výpisu Výchozí sadu pravidel párování. Tato funkce automatizuje proces až do okamžiku, kdy musíte odpovídající transakce ručně spárovat.

## <a name="validate-the-bank-statement"></a>Ověření bankovního výpisu
K ověření příkazu klepněte na stránce **Bankovní výpisy** na tlačítko **Ověřit**. Bankovní výpisy musí být ověřeny dříve, než mohou být odsouhlaseny. Tento krok je dokončen automaticky, pokud nastavíte možnost **Po importu odsouhlasit** na **Ano** v době importu. 

Ověření bankovního výpisu ověří následující podrobnosti:

-   Bankovní výpis odpovídá vybranému bankovnímu účtu.
-   Měna bankovního výpisu odpovídá měně bankovního účtu.
-   Počáteční zůstatek výpisu se rovná konečnému zůstatku předchozího výpisu pro bankovní účet.
-   Datum nepřekrývá datum pro další bankovní výpis ze stejného bankovního účtu.
-   Nejsou žádné mezery v datech pro výpisy bankovního účtu.
-   Data na řádcích výpisu jsou v rozsahu „od data“ a „do data“ z bankovního výpisu.
-   Počáteční zůstatek a souhrnné částky na řádku se rovnají konečnému zůstatku.

Po dokončení ověření se stav bankovního výpisu aktualizuje na **Ověřeno**. Bankovní výpis musí být ověřen dříve, než může být odsouhlasen.

## <a name="reconcile-the-bank-statement"></a>Odsouhlasení bankovního výpisu
Po importu elektronického bankovního výpisu a ověření výpisu na stránce **Bankovní výpisy** je možné odsouhlasit bankovní výpis s použitím stránky **Odsouhlasení banky** a **List odsouhlasení banky**. 

Na stránce **Odsouhlasení banky** klepněte na tlačítko **Nové** a vytvořte tak nové odsouhlasení, a potom vyberte bankovní účet výpisu, který byl importován. Bankovní účet může mít pouze jedno otevřené bankovní odsouhlasení. Datum přerušení určí transakce bankovního výpisu a bankovní transakce Operations, které jsou součástí listu odsouhlasení. Standardně se používá aktuální systémové datum jako datum přerušení, ale můžete datum odsouhlasení změnit. Zbývající informace v záhlaví jsou automaticky převzaty z příkazu. Tento krok je dokončen automaticky, pokud nastavíte možnost **Po importu odsouhlasit** na **Ano** v době importu. 

Na stránce **Odsouhlasení banky** klepněte na tlačítko **List** a otevřete tak stránku **List odsouhlasení banky**. Pokud možnost **Po importu odsouhlasit** nastavíte na **Ano**, bude pro odsouhlasení automaticky spuštěna Výchozí sada pravidel párování. Pro ruční spuštění pravidel párování kliknutím na tlačítko **Spustit pravidla párování** vyberte odpovídající sady pravidel nebo pravidel párování, které chcete spustit pro bankovních transakce. Pokud máte mnoho transakcí ke zpracování, můžete provést tento krok jako dávkový proces. 

Stránka **List odsouhlasení banky** obsahuje čtyři mřížky, které obsahují transakce. Dvě horní mřížky zobrazují transakce z bankovního výpisu a aplikace Operations, které nebyly dosud spárovány. Dva dolní mřížky zobrazují odpovídající transakce. Karta **Podrobnosti transakce bankovního výpisu** popisuje podrobnosti o nespárované transakci bankovního výpisu, která je vybrána v horní mřížce. 

Existují tři způsoby spárování nebo odsouhlasení transakcí bankovního výpisu:

-   Spárování transakcí s bankovními transakcemi Operations.
-   Spárování transakcí s transakcemi storna bankovního výpisu.
-   Označte transakce jako **Nové**, aby je bylo možné zaúčtovat později jako bankovní transakce v aplikaci Finance.

Pokud chcete transakce spárovat ručně, vyberte je v mřížce **Transakce bankovního výpisu**, vyberte příslušené transakce v mřížce **Bankovní transakce v aplikaci Operations** a klikněte na **Spárovat**. Vybrané transakce jsou přesunuty z horních mřížek pro nespárované transakce do dolních mřížek pro spárované transakce. Kromě toho jsou aktualizovány celkové počty spárovaných a nespárovaných transakcí. Párování transakcí umožňuje stav 1:1, n:1 a n:n. Shody musí dodržovat pravidla pro povolené rozdíly dat a mapování typu transakce. Tato pravidla jsou nastavena na stránce **Parametry pokladny a banky**.

V odsouhlasení se mohou objevit haléřové rozdíly. Můžete spárovat jednu transakci bankovního výpisu a jednu bankovní transakce Operations s haléřovými rozdíly za předpokladu, že jsou haléřové rozdíly v rámci částky tolerance, která je definována v poli **Povolený haléřový rozdíl** u bankovního účtu. Částka je uvedena v poli **Částka opravy** ve spárované bankovní transakci v aplikaci Operations. Když je odsouhlasení banky označena jako odsouhlaseno, jsou opravy automaticky zaúčtovány s použitím hlavního účtu, který je definován v přidruženém typu bankovní transakce. Opravy nejsou podporovány pro typy dokumentů **Šek** a **Vklad**. 

Stornování transakcí bankovního výpisu je párováno pomocí listu odsouhlasení. Dva řádky z výpisu lze spárovat, pokud jsou částky opačné, a pokud je jedna transakce označena jako Storno. Můžete také nastavit pravidlo párování pro akci **Vymazat řádky výpisu s položkou storno**.

Stornované bankovní transakce Operations musí být odsouhlaseny pomocí stránky **Bankovní transakce Operations**. Dvě bankovní transakce Operations je možné odsouhlasit společně, pokud mají dokumenty stejný bankovní účet, typ dokumentu a platební reference, a pokud mají opačné částky. Také je možné odsouhlasit jeden zrušený šek s cílem zabránit, aby se tyto transakce zobrazily v listě odsouhlasení. 

Pokud existují nové bankou zahájené transakce, jako jsou úroky, poplatky nebo náklady, které dosud nejsou uvedeny v aplikaci Finance, můžete je přidat do deníku, který je přidružen k vybranému odsouhlasení bankovního výpisu. Vyberte transakci bankovního výpisu v mřížce **Transakce bankovního výpisu** pro nespárované transakce a potom klepněte na tlačítko **Označit jako nové**. Stav transakce je nastaven na **Nový** a transakce je přesunuta do mřížky **Transakce bankovního výpisu** pro spárované transakce. Transakce, které jsou označeny jako **Nové**, se účtují později na stránce **Bankovní výpis**. 

Můžete zrušit párování transakcí, které byly spárovány nesprávně. Vyberte spárovanou transakci bankovního výpisu a potom klepněte na tlačítko **Zrušit párování**. Všechny přidružené transakce jsou přesunuty zpět do horní mřížky pro nespárované transakce a aktualizuje se celkový počet spárovaných a nespárovaných transakcí. 

Po dokončení procesu odsouhlasení je vhodné označit list odsouhlasení banky jako odsouhlasený.  Tento proces automaticky zaúčtuje opravné částky pomocí účtů nastavených na stránce **Typ bankovní transakce**.  Odsouhlasení banky pro výkaz může být označeno jako odsouhlasená kdykoli, i v případě, že existují řádky bankovního výpisu, které nebyly dosud spárovány.  Nespárované transakce automaticky přejdou na další list odsouhlasení jako nespárované transakce bankovního výpisu transakcí k odsouhlasení.  Všimněte si, že jakmile jednou označíte odsouhlasení bankovního výpisu jako odsouhlasené, nelze tuto akci vrátit zpět.  Odsouhlasení nebude nadále upravitelné a vy nebudete mít možnost provádět aktualizace tohoto odsouhlasení.

## <a name="post-new-transactions-that-are-associated-with-the-reconciliation"></a>Zaúčtování nových transakcí, které jsou přidruženy k odsouhlasení
Transakce bankovního výpisu, které jste označili jako **Nový** v listě odsouhlasení, jsou zaúčtovány na stránce **Bankovní výpis**. Na stránce **Bankovní výpis** výběrem ID výpisu zobrazte podrobnosti výkazu. V nabídce **Účetnictví** můžete pomocí možnosti **Zobrazit rozdělení** a **Zobrazit účetnictví** zobrazit podrobnosti za novými transakcemi a souvisejícími položkami v hlavní knize. Výběrem možnosti **Zaúčtovat** zaúčtujete řádky bankovního výpisu, které jsou označeny jako **Nové**, do hlavní knihy. Mějte na paměti, že zaúčtování může být provedeno pouze jednou pro každý bankovní výpis.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

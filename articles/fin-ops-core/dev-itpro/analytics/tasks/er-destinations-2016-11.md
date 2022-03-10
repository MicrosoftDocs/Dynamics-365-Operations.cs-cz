---
title: Konfigurace cílů ER
description: Tento postup ukazuje, jak nastavit a používat různé cíle pro výstupní součásti elektronického vykazování (ER), jako například složku nebo soubor.
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERFormatDestinationTable, SysLookupPicklist, ERFormatDestinationSettings, ERFormatDestinationEmailSettings, ERExpressionDesignerFormula, SRSPrintDestinationTokens
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f1e679b52b28ff1ca117c5224fc7e2825feb26e5e5aea1c8b5bc3a88d1eaf235
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6743256"
---
# <a name="er-configure-destinations"></a>Konfigurace cílů ER

[!include [banner](../../includes/banner.md)]

Tento postup ukazuje, jak nastavit a používat různé cíle pro výstupní součásti elektronického vykazování (ER), jako například složku nebo soubor. K vytvoření tohoto postupu jsou použita ukázková data společnosti DEMF. Německo je země\oblast s primární adresou právnické osoby, ale pro tuto proceduru můžete použít jakoukoli právnickou osobu. 

Formát použitý v tomto případě je „platební převod ISO 20022 (DE)“, ale můžete vybrat jakýkoli formát, který již byl importován. Všimněte si, že tato procedura je příkladem nastavení jednoho souboru a cíle. Další informace o správě cílů pro elektronické sestavy naleznete v nápovědě pro Dynamics 365 Finance.

1. Přejděte do nabídky Správa organizace > Elektronická sestava > Místo určení elektronického výkaznictví.
2. Klepnutím na tlačítko Nový vytvoříte novou sadu míst určení pro daný formát.
3. V poli Odkaz vyberte formát, pro který chcete konfigurovat místa určení.
    * Pokud nemáte hodnotu, kterou by bylo možné vybrat, znamená to, že nebyly importovány žádné konfigurace pro Formát elektronického výkaznictví. Před nastavením cíle je nutné importovat formát konfigurace.  
4. Kliknutím na Nový vytvořte nový cíl souboru.
    * Všimněte si, že můžete vytvořit jeden cíl souboru pro každou komponentu výstupu ve stejném formátu, jako je složka nebo soubor. Bude možné povolit nebo zakázat cíle samostatně skrze nastavení.  
5. V poli Název zadejte popisný název komponenty výstupu.
    * Doporučujeme používat smysluplné názvy, jako je "Soubor platby" nebo "Kontrolní sestava". Tyto názvy pak budou prezentovány uživatelům v rámci konfigurace spolu s nastavením cíle.  
6. V nabídce Název souboru vyberte soubor nebo složku specifickou pro daný formát.
7. Klepněte na Nastavení.
8. Vyberte možnost Ano v poli Povoleno.
    * Políčko Povoleno na každé kartě umožňuje povolit nebo zakázat jednotlivé místa určení samostatně. V tomto příkladu povolíte odesílání výstupního souboru příjemci pošty při vygenerování souboru.  
9. Klepněte na Upravit pro nastavení příjemců e-mailu.
10. Klepněte na možnost Přidat.
11. Klikněte na Správa tisku – e-mail.
12. Vyberte volbu v poli Typ zdroje e-mailu.
    * Můžete vybrat jiné typy zdrojů e-mailu, jako je například typ zákazníka nebo dodavatele. To definuje typ argumentu, který bude vrácen vzorcem účtu zdroje e-mailu. Vzorec účtu zdroje e-mailu je popsán v následujícím kroku a značí místo, skrze které provážete zdroj e-mailu. Pokud váš vzorec vrátí účet dodavatele, vyberte Dodavatel. Pokud používáte příklad konfigurace „platební převod ISO 20022“, vyberte Dodavatel.  
13. Klikněte na tlačítko Vazba pro zdroj e-mailu.
14. V části Vzorec zadejte odkaz specifický pro dokument pro typ strany, který jste vybrali předtím.
    * Namísto zadávání můžete najít uzel zdroje dat, který reprezentuje účet strany, a kliknutím na tlačítko Přidat zdroj dat aktualizovat vzorec. Příklad: Pokud používáte konfiguraci platební převod ISO 20022, uzel představující účet dodavatele má tvar $PaymentsForCoveringLetter'.Creditor.Identification.SourceID. V opačném případě uložte řetězec zadáním libovolné hodnoty řetězce, jako například DE-001.  
15. Klikněte na položku Uložit.
16. Zavřete stránku.
17. Klepněte na tlačítko Upravit, chcete-li konfigurovat podrobnosti o straně.
18. Vyberte možnost Ano v poli Primární kontakt.
    * Můžete použít různé možnosti k označení, jaký typ kontaktu by měla strana používat jako e-mailovou adresu pro tento cíl. V tomto příkladu používáme primární kontakt.  
19. Klikněte na tlačítko OK.
20. Klikněte na tlačítko OK.
21. Zadejte hodnotu do pole Předmět.
22. Klikněte na tlačítko OK.



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
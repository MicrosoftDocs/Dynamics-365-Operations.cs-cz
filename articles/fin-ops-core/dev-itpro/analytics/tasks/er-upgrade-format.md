---
title: Elektronické výkaznictví - Upgrade formátu přijetím nové základní verze tohoto formátu
description: Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může spravovat konfiguraci formátu pro elektronické výkaznictví.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERVendorPart, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 648b750b311f902555eba4536767788b64a1ea1e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184639"
---
# <a name="er-upgrade-your-format-by-adopting-a-new-base-version-of-that-format"></a>Elektronické výkaznictví - Upgrade formátu přijetím nové základní verze tohoto formátu

[!include [task guide banner](../../includes/task-guide-banner.md)]

Následující postup popisuje, jak uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví může spravovat konfiguraci formátu pro elektronické výkaznictví. Tento odstavec vysvětluje, jakým způsobem lze vytvořit vlastní verzi formátu na základě formátu přijatého od poskytovatele konfigurace. Také popisuje, jak přejmout novou základní verzi tohoto formátu.



K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky v postupech "Vytvoření poskytovatele konfigurace a jeho označení jako aktivního" a "Použití vytvořeného formát pro generování elektronických dokumentů pro platby". Tyto kroky lze provést v rámci společnosti GBSI.


## <a name="select-format-configuration-for-customization"></a>Výběr konfigurace formátu pro přizpůsobení
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
    * V tomto příkladu bude vzorová společnost Litware, Inc. (https://www.litware.com) bude sloužit jako poskytovatel konfigurace, který podporuje konfiguraci formátu pro elektronické platby pro určitou zemi.    Vzorová společnost Proseware, Inc. (http://www.proseware.com) bude jednat jako příjemce konfigurace formátu, který Litware, Inc. poskytl. Proseware, Inc. používá formáty v určitých oblastech v zemi.  
2. Klikněte na Konfigurace výkaznictví.
3. Klepněte na tlačítko Zobrazit filtry.
4. Použijte následující filtry: Do pole „Název" zadejte hodnotu filtru BACS (Velká Británie – fiktivní) a použijte operátor filtru „začíná na"
    * BACS (Velká Británie – fiktivní)  
    * Vybraná konfigurace formátu BACS (Velká Británie – fiktivní) je ve vlastnictví poskytovatele Litware, Inc.  
5. Klepněte na tlačítko Zobrazit filtry.
6. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Verze formátu se stavem Dokončeno bude použita společností Proseware, Inc. pro přizpůsobení.  

## <a name="create-a-new-configuration-for-your-custom-format-of-electronic-document"></a>Vytvoření nové konfigurace pro vlastní formát elektronického dokumentu
    * Proseware, Inc. přijala verzi 1.1 konfigurace BACS (Velká Británie – fiktivní), která obsahuje původní formát pro generování dokumentů elektronických plateb od společnosti Litware, Inc. v souladu se svým předplatným služby. Proseware, Inc. chce začít používat tuto konfiguraci jako standard pro svou zemi, ale pro splnění zvláštních místních požadavků jsou požadována některá přizpůsobení. Proseware, Inc. chce také udržovat možnost upgradu vlastního formátu ihned, jakmile je k dispozici její nová verze (se změnami pro soulad s novými požadavky specifickými pro zemi) od společnosti Litware, Inc. a chtějí provést tento upgrade s co nejnižší cenou.  Aby to bylo možné, Proseware, Inc., potřebuje vytvořit konfiguraci pomocí konfigurace Litware, Inc. BACS (Velká Británie – fiktivní) jako její základ.  
1. Zavřete stránku.
2. Vyberte Proseware, Inc. a nastavte ji jako aktivního zprostředkovatele.
3. Klikněte na možnost Nastavit jako aktivní.
4. Klikněte na Konfigurace výkaznictví.
5. Ve stromovém zobrazení rozbalte možnost „Platby (zjednodušený model)“.
6. Ve stromovém zobrazení vyberte možnost „Platby (zjednodušený model)\BACS (Velká Británie – fiktivní)“.
    * VVyberte konfiguraci BACS (Velká Británie – fiktivní) od Litware, Inc.     Proseware, Inc. použije verzi 1.1 jako základ pro vlastní verzi.  
7. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
    * To vám umožňuje vytvořit novou konfiguraci pro vlastní formát platby.  
8. Do pole Nový zadejte hodnotu „Odvodit z názvu: BACS (Velká Británie – fiktivní), Litware, Inc.“.
    * Výběrem možnosti Odvodit můžete potvrdit použití formátu BACS (Velká Británie – fiktivní) jako základ pro vytváření vlastní verze.  
9. Do pole Název zadejte „BACS (Velká Británie – fiktivní vlastní)“.
    * BACS (Velká Británie – fiktivní vlastní)  
10. Do pole Popis zadejte Platba dodavatele BACS (Velká Británie – fiktivní vlastní).
    * Platba dodavatele BACS (Velká Británie – fiktivní vlastní)  
    * Aktivní poskytovatel konfigurace (Proseware, Inc.) se zadá automaticky v tomto poli. Tento zprostředkovatel bude moci udržovat tuto konfiguraci. Jiní poskytovatelé mohou použít tuto konfiguraci, ale nebudou moci ji spravovat.  
11. Klepněte na možnost Vytvořit konfiguraci.

## <a name="customize-your-format-for-the-electronic-document"></a>Přizpůsobení formátu elektronického dokumentu
1. Klikněte na možnost Návrhář.
2. Klikněte na Rozbalit/sbalit.
3. Klikněte na Rozbalit/sbalit.
4. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka'.
5. Klepnutím na možnost Přidat otevřete dialogové okno.
6. Ve stromovém zobrazení vyberte „XML\Prvek“.
7. Do pole Název zadejte IBAN.
    * KÓD IBAN  
8. Klikněte na tlačítko OK.
9. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka\IBAN'.
10. Klepnutím na možnost Přidat otevřete dialogové okno.
11. Ve stromovém zobrazení vyberte „Text\Řetězec“.
12. Klepněte na tlačítko OK.
13. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Název\Řetězec'.
14. Zadejte 60 do pole Maximální délka.
15. Klikněte na kartu Mapování.
16. Ve stromovém zobrazení rozbalte „model“.
17. Ve stromovém zobrazení rozbalte „model\Platby“.
18. Ve stromovém zobrazení rozbalte „model\Platby\Věřitel“.
19. Ve stromovém zobrazení rozbalte „model\Platby\Věřitel\Účet“.
20. Ve stromové struktuře vyberte 'model\Platby\Věřitel\Účet\IBAN'.
21. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka =  model.Platby\Dodavatel\Banka\IBAN\Řetězec'.
22. Klikněte na možnost Vazba.
23. Klikněte na položku Uložit.

## <a name="validate-the-customized-format"></a>Ověření přizpůsobeného formátu
1. Klikněte na tlačítko Ověřit.
    * Ověřte změny v přizpůsobeném rozvržení formátu a změnách v mapování dat a ujistěte se tak, že jsou všechny vazby v pořádku.  
2. Zavřete stránku.

## <a name="change-the-status-of-the-current-version-of-the-custom-format-configuration"></a>Změna stavu aktuální verze vlastní konfigurace formátu
    * Změňte stav navržené konfigurace formátu z Návrh na Dokončeno, aby byla konfigurace dostupná pro generování platebního dokumentu.  
1. Klikněte na položku Změnit stav.
    * Všimněte si, že je aktuální verze vybrané konfigurace ve stavu Koncept.  
2. Klikněte na tlačítko Dokončit.
3. Zadejte nějakou hodnotu do pole Popis.
4. Klikněte na tlačítko OK.
5. Vyhledejte na seznamu požadovaný záznam a vyberte ho.
    * Všimněte si, že je vytvořená konfigurace uložena jako dokončená verze 1.1.1. To znamená, že se jedná o 1. verzi vlastního formátu BACS (Velká Británie – fiktivní vlastní), která je založena na 1. verzi formátu BACS (Velká Británie – fiktivní), která je založena na 1. verzi datového modelu Platby (zjednodušený model).  

## <a name="test-the-customized-format-to-generate-payment-files"></a>Test vlastního formátu pro generování souborů plateb
    * Postupujte podle kroků v postupu „Použití vytvořeného formátu pro generování elektronických dokumentů pro platby“ v rámci paralelní relace Finance and Operations. Vyberte formát BACS (Velká Británie – fiktivní vlastní) v parametrech metody elektronické platby. Zkontrolujte, že vytvořený soubor platby obsahuje nedávno uvedený uzel XML představující kód IBAN v souladu s místními požadavky.  

## <a name="update-the-existing-country-specific-configuration"></a>Aktualizace existující konfigurace specifické pro zemi
    * Litware, Inc. musí aktualizovat konfiguraci BACS (Velká Británie – fiktivní) a přijmout nové požadavky země, aby mohla spravovat formát elektronického dokumentu. Později se toto stane součástí nové verze této konfigurace, která bude nabízena odběratelům služby, včetně společnosti Proseware, Inc.  
    * Ve skutečném procesu poskytování služeb lze každou novou verzi BACS (Velká Británie – fiktivní) importovat společností Proseware, Inc. z úložiště souborů LCS poskytovatele Litware, Inc. V tomto procesu budeme simulovat tento krok aktualizováním BACS (Velká Británie – fiktivní) jménem poskytovatele služby.  
1. Zavřete stránku.
2. Vyberte poskytovatele Litware, Inc.
3. Klikněte na možnost Nastavit jako aktivní.
4. Klikněte na Konfigurace výkaznictví.
5. Ve stromovém zobrazení rozbalte možnost „Platby (zjednodušený model)“.
6. Ve stromovém zobrazení vyberte možnost „Platby (zjednodušený model)\BACS (Velká Británie – fiktivní)“.
    * Verze návrhu vlastněná poskytovatelem Litware, Inc. BACS (Velká Británie – fiktivní) bude zvolena pro zavedení změn podporujících nové požadavky specifické pro zemi.  

## <a name="localize-the-base-format-of-the-electronic-document"></a>Lokalizace základního formátu elektronického dokumentu
    * Předpokládejme, že existují nové požadavky specifické pro zemi, pro které musí Litware, Inc. zajistit soulad: - Hodnota kódu SWIFT banky příjemce platby v každé platební transakci.  - Limit 100 znaků pro délku textu s názvem dodavatele při generování souboru.  
    * Nové požadavky specifické pro zemi  
    * Vyberte pracovní verzi požadované konfigurace pro zavedení požadovaných změn.  
1. Klikněte na možnost Návrhář.
2. Klikněte na Rozbalit/sbalit.
3. Klikněte na Rozbalit/sbalit.
4. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka'.
5. Klepnutím na možnost Přidat otevřete dialogové okno.
6. Ve stromovém zobrazení vyberte „XML\Prvek“.
7. Do pole Název zadejte SWIFT.
    * SWIFT  
8. Klikněte na tlačítko OK.
9. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Banka\SWIFT'.
10. Klepnutím na možnost Přidat otevřete dialogové okno.
11. Ve stromovém zobrazení vyberte „Text\Řetězec“.
12. Klepněte na tlačítko OK.
13. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka\Dodavatel\Název\Řetězec'.
14. Zadejte 100 do pole Maximální délka.
15. Klikněte na kartu Mapování.
16. Ve stromovém zobrazení rozbalte „model“.
17. Ve stromovém zobrazení rozbalte „model\Platby“.
18. Ve stromovém zobrazení rozbalte „model\Platby\Věřitel“.
19. Ve stromovém zobrazení rozbalte „model\Platby\Věřitel\Zástupce“.
20. Ve stromové struktuře vyberte 'model\Platby\Věřitel\Agent\SWIFT'.
21. Ve stromové struktuře vyberte 'Xml\Zpráva\Platby\Položka =  model.Platby\Dodavatel\Banka\SWIFT\String'.
22. Klikněte na možnost Vazba.
23. Klikněte na položku Uložit.

## <a name="validate-the-localized-format"></a>Ověření lokalizovaného formátu
1. Klikněte na tlačítko Ověřit.
2. Zavřete stránku.

## <a name="change-the-status-of-the-current-version-of-the-base-format-configuration"></a>Změna stavu aktuální verze konfigurace základního formátu
    * Změňte stav aktualizované konfigurace základní formátu z Návrh na Dokončeno, aby byla k dispozici pro generování platebních dokladů a aktualizace konfigurace formátu, které jsou od ní odvozeny.  
1. Klikněte na položku Změnit stav.
    * Všimněte si, že je aktuální verze vybrané konfigurace ve stavu Koncept.  
2. Klikněte na tlačítko Dokončit.
3. Zadejte nějakou hodnotu do pole Popis.
4. Klikněte na tlačítko OK.
5. Vyhledejte na seznamu požadovaný záznam a vyberte ho.

## <a name="change-the-base-version-for-the-custom-format-configuration"></a>Změna základní verze konfigurace vlastního formátu
    * Proseware, Inc. je informován, že je k dispozici nová verze 1.2 konfigurace BACS (Velká Británie – fiktivní) pro generování dokumentů elektronických plateb podle naposledy ohlášených požadavků specifických pro zemi. Proseware, Inc. chce začít ji používat jako standard pro danou zemi.  Aby to bylo možné, Proseware, Inc. musí změnit základní verzi konfigurace pro vlastní konfiguraci BACS (Velká Británie – fiktivní vlastní). Namísto verze 1.1 BACS (Velká Británie – fiktivní) použije novou verzi 1.2.  
1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
2. Vyberte Proseware, Inc. jako zprostředkovatele a označte ho jako aktivního.
3. Klikněte na možnost Nastavit jako aktivní.
4. Klikněte na Konfigurace výkaznictví.
5. Ve stromovém zobrazení rozbalte možnost „Platby (zjednodušený model)“.
6. Ve stromovém zobrazení rozbalte možnost „Platby (zjednodušený model)\BACS (Velká Británie – fiktivní)“.
7. Ve stromovém zobrazení vyberte možnost „Platby (zjednodušený model)\BACS (Velká Británie – fiktivní)\BACS (Velká Británie – fiktivní vlastní)“.
    * Vyberte konfiguraci BACS (Velká Británie – fiktivní vlastní), která je ve vlastnictví Proseware, Inc.  
    * Použijte pracovní verzi vybrané konfigurace pro zavedení požadovaných změn.  
8. Klepněte na Přeskládání.
    * Vyberte novou verzi 1.2 základní konfigurace, která bude použita jako nový základ pro aktualizaci konfigurace.  
9. Klikněte na tlačítko OK.
    * Všimněte si, že byly zjištěny některé konflikty během slučování vlastní verze a nové základní verze, jako jsou změny formátu, které nelze sloučit automaticky.  

## <a name="resolve-rebase-conflicts"></a>Řešení konfliktů přeskládání
1. Klikněte na možnost Návrhář.
    * Povšimněte si změn v limitu délky textu s názvem dodavatele, které nelze provést automaticky. Tyto informace jsou uvedeny v seznamu konfliktů. Pro každý konflikt typu Aktualizace existují tyto možnosti: - Použít předchozí základní hodnotu (tlačítko v horní části mřížky) a vyvolat předchozí hodnotu základní verze (0 v tomto případě).  - Použít základní hodnotu (tlačítko v horní části mřížky) a vyvolat novou hodnotu základní verze (100 v tomto případě).  - Udržujte vlastní hodnotu (vlastní) (60 v tomto případě).  Kliknutím na tlačítko Použít použijte pro délku s textovým názvem dodavatele limit 100 znaků (pro konkrétní zemi).  
    * Všimněte si, že Proseware, Inc. and Litware, Inc mají vlastní a místní verze formátu využívající kódy IBAN a SWIFT se souvisejícími součástmi, které jsou automaticky sloučeny v rámci správy formátu.  
2. Klikněte na Použít základní hodnotu.
    * Kliknutím na tlačítko Použít použijte pro názvy dodavatele limit 100 znaků (pro konkrétní zemi).  
3. Klikněte na položku Uložit.
    * Uložením formátu dojde k odstranění vyřešených konfliktů ze seznamu konfliktů.  
4. Zavřete stránku.

## <a name="change-the-status-of-the-new-version-of-the-custom-format-configuration"></a>Změna stavu nové verze vlastní konfigurace formátu
1. Klikněte na položku Změnit stav.
    * Změňte stav aktualizované vlastní konfigurace formátu z Koncept na Dokončeno. To zpřístupní konfiguraci formátu pro generování platebních dokumentů. Všimněte si, že je aktuální verze vybrané konfigurace ve stavu Koncept.  
2. Klikněte na tlačítko Dokončit.
3. Zadejte nějakou hodnotu do pole Popis.
4. Klikněte na tlačítko OK.
    * Všimněte si, že vytvořená konfigurace je uložena jako dokončená verze 1.2.2: 2. verze základního formátu BACS (Velká Británie – fiktivní vlastní), který je založen na 2. verzi základního formátu BACS (Velká Británie – fiktivní), která je založena na modelu dat 1. verze plateb (zjednodušený model).  

## <a name="test-the-customized-format-for-payment-files-generation"></a>Test vlastního formátu pro generování souborů plateb
    * Postupujte podle kroků v postupu „Použití vytvořeného formátu pro generování elektronických dokumentů pro platby“ v rámci paralelní relace Finance and Operations. Vyberte vytvořený formát BACS (Velká Británie – fiktivní vlastní) v parametrech metody elektronické platby. Zkontrolujte, že vytvořený soubor platby obsahuje nedávno uvedený uzel XML společností by Proseware, Inc. představující kód účtu IBAN v souladu s místními požadavky. Soubor by rovněž měl obsahovat nedávno uvedených uzel XML uvedený společností Litware, Inc. představující bankovní kód SWIFT podle požadavků země.  


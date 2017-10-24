--- 
title: "Definování závislosti konfigurací z jiných komponent pro elektronické výkaznictví (ER)"
description: "K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky průvodce záznamem úloh, ER Správa konfigurací mapování modelů, a mít přístup k aplikaci Microsoft Dynamics Lifecycle Services (LCS)."
author: NickSelin
manager: AnnBe
ms.date: 06/23/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 1a627e2261c4c9c854b68262d7ce316ab6d40dd4
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="define-the-dependency-of-configurations-from-othcomponents-for-electronic-reporting-er"></a>Definování závislosti konfigurací z jiných komponent pro elektronické výkaznictví (ER)

[!include[task guide banner](../../includes/task-guide-banner.md)]

K provedení těchto kroků musíte nejprve dokončit jednotlivé kroky průvodce záznamem úloh, ER Správa konfigurací mapování modelů, a mít přístup k aplikaci Microsoft Dynamics Lifecycle Services (LCS).

Tento postup popisuje postup návrhu konfigurace elektronických sestav (ER) a zadání závislosti z dalších softwarových komponent, abyste tak mohli zajistit správné stažení konfigurace pro specifickou verzi aplikace Microsoft Dynamics 365 for Finance and Operations, edice Enterprise. V tomto příkladu vytvoříte požadované ER konfigurace pro vzorovou společnost Litware, Inc. 

Tento postup je navržen pro uživatele s přiřazenou rolí správce systému nebo vývojáře elektronického vykazování. Kroky lze provést v každé společnosti, protože konfigurace ER jsou sdíleny společnostmi. 

1. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
    * Zkontrolujte, že strom konfigurace obsahuje konfiguraci Ukázkový datový model a podřízené položky. V opačném případě dokončete jednotlivé kroky průvodce záznamem, ER Správa konfigurací mapování modelů, a znovu spusťte tohoto průvodce.   

## <a name="define-the-dependency-of-er-configurations-from-other-components"></a>Definování závislosti konfigurace ER z jiných komponent
1. Ve stromovém zobrazení rozbalte Ukázkový datový model.
2. Ve stromovém zobrazení vyberte Sample data model\Sample mapping.
    * Vybrali jsme pracovní verzi konfigurace mapování modelu Ukázkové mapování. Nyní určíme závislosti z dalších softwarových komponent. Tento krok je považován za předpoklad pro řízení stažení této verze konfigurace z úložiště ER a další používání této verze.   
3. Rozbalte oddíl Předpoklady.
    * Mějte na paměti, že skupina předpokladů implementace již byla během tohoto kroku automaticky přidána. Tato skupina obsahuje součást předpokladů, která se vztahuje ke konfiguraci datového modelu a je označena jako Implementace. Označení znamená, že konfigurace mapování modelu pro vzorový model mapování je považována za implementaci datového modelu – Vzorový datový model. Tato součást vynutí u ER stahování konfigurace mapování modelu – Vzorové mapování, z úložiště ER po stažení konfigurace modelu – Vzorový datový model.   
4. Klikněte na položku Upravit.
    * Jednu závislost aktuální konfigurace ze softwarové komponenty lze určit pomocí definice typu komponenty a buď verze komponenty nebo rozsahu verzí součástí.  
    * Požadované závislostí mohou být seskupeny. Je-li vybrán typ seskupení 'Všechny', podmínka závislosti této skupiny bude považována za splněnou, pokud bude splněna podmínka každé závislosti z této skupiny a podřízené skupiny. Je-li vybrán typ seskupení 'Jeden', podmínka závislosti této skupiny bude považována za splněnou, pokud bude splněna podmínka alespoň jedné závislosti z této skupiny a podřízené skupiny.   
5. Klikněte na položku Nová.
6. Vyberte Požadovaná součást produktu.
7. Zvolte Microsoft Dynamics 365 for Operations (1611).
8. V poli Verze zadejte [7.1.1541.3036,8).
    * [7.1.1541.3036,8)  
    * Zadané závislosti budou vyhodnoceny po stažení této konfigurace z některého úložiště ER. Tato verze konfigurace bude stažena z úložiště ER, pokud je verze 1 konfigurace Vzorový model dat již k dispozici nebo stažena předem. Pokud dojde ke stažení předem, musí být proces dokončen v části Finance a operace a verze musí být 7.1.1541.3036 nebo novější, ale nesmí přesáhnout hlavní verzi 8.   
9. Klikněte na položku Uložit.
10. Zavřete stránku.
11. Klikněte na položku Změnit stav.
12. Klikněte na tlačítko Dokončit.
13. Klikněte na tlačítko OK.
14. Ve stromovém zobrazení vyberte Sample data model\Sample mapping (alternative).
15. Klikněte na položku Upravit.
16. Klikněte na položku Nová.
17. Vyberte Požadovaná součást produktu.
18. Vyberte Microsoft Dynamics AX 7.0 RTW.
19. V poli Verze zadejte [7.0.1265.3015,7.1).
    * [7.0.1265.3015,7.1)  
    * Závislosti budou vyhodnoceny po stažení této konfigurace z některého úložiště ER. Tato verze konfigurace bude stažena z úložiště ER, pokud je verze 1 konfigurace Vzorový model dat již k dispozici nebo stažena předem. Pokud dojde ke stažení předem, musí být proces dokončen v aplikaci Microsoft Dynamics 365 for Finance and Operations, edice Enterprise, a verze musí být 7.0.1265.3015 nebo novější, ale nesmí přesáhnout menší verzi 1.   
20. Klikněte na položku Uložit.
21. Zavřete stránku.
22. Klikněte na položku Změnit stav.
23. Klikněte na tlačítko Dokončit.
24. Klikněte na tlačítko OK.

## <a name="configure-the-er-repository"></a>Konfigurace úložiště ER
1. Zavřete stránku.
2. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
    * Otevřete seznam úložišť ER pro stávajícího poskytovatele ER, Litware, Inc.  
3. Označte v seznamu vybraný řádek.
4. Klikněte na možnost Úložiště.
5. Klepněte na tlačítko Zobrazit filtry.
6. Zadejte hodnotu filtru „LCS“ v poli „Název typu“ za použití operátoru filtru „obsahuje“.
    * Pokud je již úložiště LCS registrováno pro aktuálního zprostředkovatele ER, můžete přeskočit zbývající kroky tohoto podúkolu. Pokud úložiště LCS není zatím zaregistrováno, postupujte podle pokynů.   
7. Klepnutím na možnost Přidat otevřete dialogové okno.
8. V poli Typ úložiště konfigurace zadejte LCS.
9. Klikněte na Vytvořit úložiště.
10. V poli Projekt zadejte nebo vyberte hodnotu.
    * Vyberte požadovaný projekt LCS z vyhledávacího pole Projekt.  
11. Klikněte na tlačítko OK.
12. Zavřete stránku.

## <a name="upload-configurations-to-lcs"></a>Odeslání konfigurací do LCS
1. Klikněte na Konfigurace výkaznictví.
2. Ve stromovém zobrazení vyberte Ukázkový datový model.
3. Vyberte dokončenou verzi této konfigurace.
4. Klikněte na položku Změnit stav.
5. Klepněte na Sdílet.
6. Klikněte na tlačítko OK.
    * Verze 1 této konfigurace modelu byla odeslána do LCS za pomoci projektu LCS pro úložiště ER, v souladu s předchozí konfigurací.   
7. Ve stromovém zobrazení rozbalte Ukázkový datový model.
8. Ve stromovém zobrazení vyberte Sample data model\Sample mapping.
9. Vyberte dokončenou verzi této konfigurace.
10. Klikněte na položku Změnit stav.
11. Klepněte na Sdílet.
12. Klikněte na tlačítko OK.
    * Verze 1.1 této konfigurace mapování modelu byla odeslána do LCS za pomoci projektu LCS pro úložiště ER, v souladu s předchozí konfigurací.   
13. Ve stromovém zobrazení vyberte Sample data model\Sample mapping (alternative).
14. Vyberte dokončenou verzi této konfigurace.
15. Klikněte na položku Změnit stav.
16. Klepněte na Sdílet.
17. Klikněte na tlačítko OK.
    * Verze 1.1 této konfigurace mapování modelu byla odeslána do LCS za pomoci projektu LCS pro úložiště ER, v souladu s předchozí konfigurací.   

## <a name="evaluate-er-configuration-dependencies"></a>Vyhodnocení závislostí konfigurace ER
    * Odstraníme ze systému vytvořené konfigurace a stáhneme je zpět z úložiště LCS.  
1. Ve stromovém zobrazení vyberte Sample data model\Sample mapping.
2. Klepněte na tlačítko Odstranit.
3. Klepněte na tlačítko Ano.
4. Ve stromovém zobrazení vyberte Sample data model\Sample mapping (alternative).
5. Klepněte na tlačítko Odstranit.
6. Klepněte na tlačítko Ano.
7. Ve stromovém zobrazení vyberte Sample data model\Sample format
8. Klepněte na tlačítko Odstranit.
9. Klepněte na tlačítko Ano.
10. Ve stromovém zobrazení vyberte Ukázkový datový model.
11. Klepněte na tlačítko Odstranit.
12. Klepněte na tlačítko Ano.
13. Zavřete stránku.
    * Otevřete seznam úložišť ER pro stávajícího poskytovatele ER, Litware, Inc.  
14. Klikněte na možnost Úložiště.
15. Klepněte na tlačítko Zobrazit filtry.
16. Zadejte hodnotu filtru „LCS“ v poli „Název typu“ za použití operátoru filtru „obsahuje“.
17. Klikněte na možnost Otevřít.
18. Ve stromovém zobrazení vyberte Ukázkový datový model.
    * Všimněte si, že se můžete podívat na vyhodnocení toho, zda byly splněny požadované podmínky pro jednotlivé verze konfigurace ER u aktuálního úložiště. K zobrazení tohoto hodnocení klepněte na tlačítko Zkontrolovat požadavky.   
19. Klikněte na Zkontrolovat požadavky.
20. Klepněte na tlačítko Importovat.
21. Klepněte na tlačítko Ano.
22. Zavřete stránku.
23. Zavřete stránku.
24. Zavřete stránku.
25. Přejděte do části Správa organizace > Elektronické výkaznictví > Konfigurace.
26. Ve stromovém zobrazení rozbalte Ukázkový datový model.
    * Všimněte si, že konfigurace modelu mapování Vzorové mapování bylo staženo spolu s vybranou konfigurací modelu dat. Dva soubory jsou staženy společně vzhledem k tomu, že 'Ukázkové mapování' bylo definováno jako implementace vybraného datového modelu a vzhledem k tomu, že je použitelné pro Finance a Operace. Konfigurace Vzorové mapování (alternativní) nebylo staženo, protože podmínky pro požadovanou aplikační verzi nebyly splněny.   
    * Pokud jste přihlášeni k Dynamics 365 for Finance and Operations, Enterprise edition, zaregistrujte si stejného poskytovatele, přejděte na projekt LCS a stáhněte stejnou konfiguraci datového modelu, stáhne se konfigurace Ukázkové mapování (alternativní) a konfigurace "Ukázkové mapování" bude přeskočena.  



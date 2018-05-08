--- 
title: "Správa konfigurací mapování modelu pro elektronické výkaznictví (ER)"
description: "Následující procedura vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může spravovat mapování modelu pro elektronické výkaznictví (ER) v samostatné konfiguraci ER."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
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
ms.openlocfilehash: 35fdc1e98897d449ce18fe38cc6b7896ca5c5278
ms.contentlocale: cs-cz
ms.lasthandoff: 09/29/2017

---
# <a name="manage-model-mapping-configurations-for-electronic-reporting-er"></a>Správa konfigurací mapování modelu pro elektronické výkaznictví (ER)

[!include [task guide banner](../../includes/task-guide-banner.md)]

Následující procedura vysvětluje, jak uživatel přiřazený k roli Správce systému nebo Návrhář elektronického výkaznictví může spravovat mapování modelu pro elektronické výkaznictví (ER) v samostatné konfiguraci ER. V tomto průvodci záznamem úloh vytvoříte požadované ER konfigurace pro vzorovou společnost Litware, Inc. K provedení kroků v tomto průvodci záznamem úloh musíte nejprve dokončit postup z průvodce záznamem úloh ER Vytvoření poskytovatele konfigurace a jeho označení jako aktivního. 

Vzhledem k tomu, že konfigurace ER se sdílí mezi společnostmi, můžete dokončit tohoto průvodce záznamem úloh za použití sady firemních dat podle vašeho výběru. Funkce pro tohoto průvodce záznamem úloh naleznete po instalaci některé z následujících oprav hotfix: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 pro verzi Dynamics AX 7.0 nebo https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 pro verzi Dynamics 365 for Operations.

1. Přejděte do části Správa organizace > Pracovní prostory > Elektronické výkaznictví.
    * Ověřte, zda poskytovatel konfigurace pro vzorovou společnost ‘Litware, Inc.’ je k dispozici a je označen jako aktivní. Pokud tohoto zprostředkovatele konfigurace nevidíte, musíte nejprve dokončit jednotlivé kroky v průvodci záznamem úloh Vytvoření poskytovatele konfigurace a jeho označení jako aktivního.   

## <a name="add-a-new-er-model-configuration"></a>Přidání nové konfigurace ER modelu
1. Klikněte na Konfigurace výkaznictví.
    * Přidejte novou konfiguraci modelu. Název musí být jedinečný ve stromu konfigurace.  
2. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
3. V poli Název zadejte Vzorový datový model.
    * Vzorový datový model  
4. Klepněte na možnost Vytvořit konfiguraci.
5. Klikněte na možnost Návrhář.
6. Kliknutím na možnost Nový otevřete dialogové okno.
7. Do pole Název zadejte Kořen.
    * Kořen  
8. Klepněte na možnost Přidat.
9. Kliknutím na možnost Nový otevřete dialogové okno.
10. Do pole Název zadejte text „Společnost“.
    * Společnost  
11. Klepněte na možnost Přidat.
12. V poli Popis zadejte text popisu právnické osoby nebo společnosti, ve které je uživatel přihlášen při spuštění. 
    * Popis právnické osoby nebo společnosti, ve které se uživatel po spuštění přihlásil.  
13. Klikněte na Kořenový odkaz.
14. Klikněte na tlačítko OK.
15. Klikněte na položku Uložit.
16. Zavřete stránku.
17. Klikněte na položku Změnit stav.
18. Klikněte na tlačítko Dokončit.
19. Klikněte na tlačítko OK.

## <a name="add-a-new-er-model-mapping-configuration"></a>Přidání nové konfigurace mapování modelu ER
1. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
2. V poli Nový zadejte Mapování modelu založené na datovém modelu Vzorový datový model.
3. Do pole Název zadejte Vzorové mapování.
    * Vzorové mapování  
4. Klepněte na možnost Vytvořit konfiguraci.
5. Rozbalte oddíl Předpoklady.
    * Mějte na paměti, že skupina předpokladů implementace již byla automaticky přidána. Skupina obsahuje součást předpokladů, která se vztahuje k nadřazené konfiguraci datového modelu a je označena jako Implementace. To znamená, že tato konfigurace mapování modelu pro vzorový model mapování je považována za implementaci datového modelu – Vzorový datový model. Tato součást tedy vynutí u ER stahování konfigurace mapování modelu – Vzorové mapování, z úložiště ER po stažení konfigurace modelu – Vzorový datový model.   
6. Klikněte na možnost Návrhář.
    * Všimněte si, že vytvořená konfigurace mapování modelu obsahuje nové prázdné mapování se stejným názvem, jako vytvořená konfigurace. Mějte na paměti, že pokud konfigurace vybraného nadřazeného modelu obsahuje mapování modelu, dojde ke zkopírování do nové konfigurace mapování modelu.   
7. Klikněte na možnost Návrhář.
8. Ve stromové struktuře vyberte Dynamics 365 for Operations\Table.
9. Klikněte na možnost Přidat kořen.
10. Do pole Název zadejte text „Společnost“.
    * Společnost  
11. Do pole Tabulka zadejte hodnotu „CompanyInfo“.
    * CompanyInfo  
12. Klikněte na tlačítko OK.
13. Ve stromovém zobrazení rozbalte Společnost.
14. Ve stromovém zobrazení rozbalte Company\find().
15. Ve stromovém zobrazení vyberte Company\find()\Name.
16. Klikněte na možnost Vazba.
17. Klikněte na položku Uložit.
18. Zavřete stránku.
19. Zavřete stránku.
20. V podokně akcí klikněte na možnost Konfigurace.
21. Klikněte na Parametry uživatelů.
22. Vyberte možnost Ano v poli Nastavení běhu.
23. Klikněte na tlačítko OK.
24. Klikněte na položku Upravit.
25. Vyberte možnost Ano v poli Koncept běhu.

## <a name="add-a-new-er-format-configuration"></a>Přidání nové konfigurace formátu ER
1. Ve stromovém zobrazení vyberte Ukázkový datový model.
2. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
3. V poli Nový zadejte Formát založený na datovém modelu Vzorový datový model.
4. Do pole Název zadejte Ukázkový formát.
    * Ukázkový formát  
5. Klepněte na možnost Vytvořit konfiguraci.
6. Klikněte na možnost Návrhář.
7. Klepnutím na možnost Přidat kořen otevřete dialogové okno.
8. Ve stromovém zobrazení vyberte „Text\Řetězec“.
9. Klikněte na tlačítko OK.
10. Klikněte na kartu Mapování.
11. Ve stromovém zobrazení rozbalte „model“.
12. Ve stromu vyberte model\Company.
13. Klikněte na možnost Vazba.
14. Klikněte na položku Uložit.
15. Zavřete stránku.
    * Pro účely testování spusťte pracovní verzi vytvořeného formátu.  
16. Klikněte na položku Spustit.
    * Na pevné záložce Verze klepněte na tlačítko Spustit.  
17. Klikněte na tlačítko OK.
    * Zkontrolujte výstup, zda obsahuje název společnosti, ve které je přihlášen uživatel, který spouští tuto konfiguraci formátu. Poznámka: vytvářená konfigurace mapování modelu je použita v této konfiguraci formátu, protože je k dispozici pouze jedna konfigurace, která obsahuje požadované mapování modelu.   

## <a name="add-alternative-er-model-mapping-configuration"></a>Přidání alternativní konfigurace mapování modelu ER
1. Ve stromovém zobrazení vyberte Ukázkový datový model.
2. Kliknutím na možnost Vytvořit konfiguraci otevřete dialogové okno.
3. V poli Nový zadejte Mapování modelu založené na datovém modelu Vzorový datový model.
4. V poli Název zadejte Vzorové mapování (alternativní).
    * Vzorové mapování (alternativní)  
5. Klepněte na možnost Vytvořit konfiguraci.
6. Klikněte na možnost Návrhář.
7. Klikněte na možnost Návrhář.
8. Ve stromové struktuře vyberte Dynamics 365 for Operations\Table.
9. Klikněte na možnost Přidat kořen.
10. Do pole Název zadejte text „Společnost“.
    * Společnost  
11. Do pole Tabulka zadejte hodnotu „CompanyInfo“.
    * CompanyInfo  
12. Klikněte na tlačítko OK.
13. Klikněte na položku Upravit.
14. Ve stromovém zobrazení vyberte možnost „Řetězec\SLOUČIT“.
15. Klikněte na možnost Přidat funkci.
16. Ve stromovém zobrazení rozbalte Společnost.
17. Ve stromovém zobrazení rozbalte Company\find().
18. Ve stromovém zobrazení vyberte Company\find()\Name.
19. Klikněte na možnost Přidat datový zdroj.
20. Zadejte hodnotu do pole Receptura.
    * CONCATENATE(Company.'find()'.Name, ";",  
21. Ve stromovém zobrazení vyberte Company\find()\Company(DataArea).
22. Klikněte na možnost Přidat datový zdroj.
23. Zadejte hodnotu do pole Receptura.
    * CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)  
24. Klikněte na položku Uložit.
25. Zavřete stránku.
26. Klikněte na položku Uložit.
27. Zavřete stránku.
28. Zavřete stránku.
29. Vyberte možnost Ano v poli Koncept běhu.

## <a name="use-an-existing-er-model-mapping-configuration"></a>Použití existující konfigurace mapování modelu ER
1. Ve stromovém zobrazení vyberte Sample data model\Sample format
2. Klikněte na položku Spustit.
    * Všimněte si, že vybranou pracovní verzi konfigurace formátu ER nelze spustit, protože je k dispozici více než jedna konfigurace mapování modelu pro nedefinovaný datový model, který byl vybrán jako zdroj dat používaného formátu ER.   
    * Dále definujete konfiguraci alternativního mapování modelu jako tu, ze které se použije mapování modelu pro zdroj dat používaného formátu ER.   
3. Ve stromovém zobrazení vyberte Sample data model\Sample mapping (alternative).
4. Vyberte možnost Ano v položce Výchozí pro pole mapování modelu.
5. Ve stromovém zobrazení vyberte Sample data model\Sample format
6. Klikněte na položku Spustit.
7. Klikněte na tlačítko OK.
    * Všimněte si, že výchozí konfigurace mapování modelu se používá v této konfiguraci formátu pro generování elektronických dokumentů (vytvořený výstup obsahuje kód společnosti).  



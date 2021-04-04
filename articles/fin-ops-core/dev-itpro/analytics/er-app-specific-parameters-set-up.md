---
title: Nastavení parametrů formátu ER podle právnické osoby
description: V tomto tématu je vysvětleno, jak nastavit parametry formátu elektronického výkaznictví (ER) podle právnické osoby.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: eebca6575a0b23f75baabbb91727f498de44d9cb
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570703"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a>Nastavení parametrů formátu ER podle právnické osoby

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a>Předpoklady

Chcete-li provést tento postup, musíte nejprve dokončit kroky v [Nastavení formátů ER, které budou používat parametry specifikované podle právnické osoby](er-app-specific-parameters-configure-format.md).

K dokončení příkladů v tomto tématu musíte mít přístup k aplikaci Microsoft Dynamics 365 Finance (Finance) pro některou z následujících rolí:

- Návrhář elektronického výkaznictví
- Funkční konzultant elektronického výkaznictví
- Správce systému

## <a name="import-er-configurations"></a>Import konfigurací ER

1.  Přihlaste se k prostředí.
2.  Na výchozím řídicím panelu vyberte **Elektronické vykazování**.
3.  Vyberte **Konfigurace vykazování**.
4.  Importujte do aktuální instance aplikace Finance konfigurace, které jste exportovali ze služby Regulatory Configuration Services (RCS) při dokončování kroků v tématu [Konfigurace formátů ER pro použití parametrů zadaných pro právnickou osobu](er-app-specific-parameters-configure-format.md). Tyto kroky proveďte pro každou konfiguraci elektronického výkaznictví (ER) v následujícím pořadí: datový model, mapování modelu a formáty.

    1. Vyberte **Exchange \> Načíst ze souboru XML**.
    2. Zvolte **Procházet** a vyberte soubor pro požadovanou konfiguraci elektronického výkaznictví ve formátu XML.
    3. Vyberte **OK**.
    
    Následující ilustrace znázorňuje konfigurace, které je nutné mít po dokončení.

    ![Stránka konfigurací elektronického výkaznictví](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a>Nastavení parametrů pro společnost DEMF

Pomocí systému ER můžete nastavit specifické parametry aplikace pro formát ER.

1.  Vyberte právnickou osobu **DEMF**.
2.  Ve stromu konfigurace vyberte formát **Formát pro ověření, jak vyhledat data LE**.
3.  V podokně akcí na kartě **Konfigurace** ve skupině **Parametry specifické pro aplikaci** vyberte **Nastavení**.

    ![Stránka specifické parametry aplikace ER](./media/GER-AppSpecParms-LookupForm.PNG)
    
    Na stránce **Parametry specifické pro aplikaci** můžete konfigurovat pravidla pro zdroj dat **Selektor** formátu **Formát pro učení se, jak vyhledávat data ER**.
    
    Pokud základní formát ER bude obsahovat několik zdrojů dat typu **vyhledávání**, musíte vybrat požadovaný zdroj dat na pevné záložce **Vyhledávání** před zahájením konfigurace sady pravidel pro zdroj dat.
    
    Pro každý zdroj dat lze nakonfigurovat samostatná pravidla pro každou verzi vybraného formátu ER.
    
    Celá sada pravidel pro všechny vyhledávací zdroje dat, které jsou k dispozici ve vybrané verzi základního formátu ER, tvoří parametry specifické pro aplikaci ve formátu ER.

4.  Vyberte verzi **1.1.1** formátu ER.
5.  Na pevné záložce **Podmínky** vyberte **Přidat**.
6.  V poli **Kód** nového záznamu výběrem šipky rozevíracího seznamu otevřete vyhledávání.

    Vyhledávání představuje seznam kódů daní pro výběr. Tento seznam je vrácen zdrojem dat **Model.Data.Tax**, který byl nakonfigurován v základním formátu ER. Vzhledem k tomu, že tento zdroj dat obsahuje pole **Název**, zobrazí se názvy jednotlivých kódů daní ve vyhledávání.

    ![Stránka specifické parametry aplikace ER](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  Vyberte kód daně **VAT19**.
8.  V poli **Výsledek vyhledávání** nového záznamu výběrem šipky rozevíracího seznamu otevřete vyhledávání. Vyhledávání představuje seznam hodnot pro formát výčtu TaxationLevel pro výběr.

    Všimněte si, že pokud je jako preferovaný jazyk uživatele, jako který jste přihlášeni, vybrána němčina, budou popisky hodnot ve vyhledávání v němčině, pokud byly přeloženy do formátu Base ER. Kromě toho, pokud byl přeložen popisek vyhledávacího zdroje dat, bude tento popisek zobrazen na kartě **vyhledávání** v preferovaném jazyce uživatele.

    ![Stránka specifické parametry aplikace ER](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  Vyberte hodnotu **Běžné zdanění**.

    Přidáte-li tento záznam, definujete následující pravidlo: vždy, když je požadován zdroj dat vyhledávání **Selektor**, je požadován datový zdroj výběru, a kód DPH **VAT19** je předán jako argument, bude vrácena hodnota **Běžné zdanění** jako požadovaná úroveň zdanění.

10. Vyberte **přidat** a postupujte podle následujících kroků:

    1. V poli **Kód** vyberte kód daně **InVAT19**.
    2. V poli **výsledek vyhledávání** vyberte hodnotu **normální zdanění**.
    
11. Znovu vyberte **přidat** a postupujte podle následujících kroků:

    1. V poli **Kód** vyberte kód daně **VAT7**.
    2. V poli **výsledek vyhledávání** vyberte hodnotu **redukované zdanění**.
    
12. Znovu vyberte **přidat** a postupujte podle následujících kroků:

    1. V poli **Kód** vyberte kód daně **InVAT7**.
    2. V poli **výsledek vyhledávání** vyberte hodnotu **redukované zdanění**.
    
13. Znovu vyberte **přidat** a postupujte podle následujících kroků:

    1. V poli **Kód** vyberte kód daně **THIRD**.
    2. V poli **výsledek vyhledávání** vyberte hodnotu **žádné zdanění**.
    
14. Znovu vyberte **přidat** a postupujte podle následujících kroků:

    1. V poli **Kód** vyberte kód daně **InVAT0**.
    2. V poli **výsledek vyhledávání** vyberte hodnotu **žádné zdanění**.
    
15. Znovu vyberte **přidat** a postupujte podle následujících kroků:

    1. V poli **kód** vyberte možnost **\*Notblank\***.
    2. V poli **výsledek vyhledávání** vyberte hodnotu **Jiné**.
    
    Přidáte-li tento poslední záznam, definujete následující pravidlo: vždy, když kód daně předaný jako argument nesplňuje žádné z předchozích pravidel, vrátí zdroj dat vyhledávání jako požadovanou úroveň zdanění **Jiné**.

    ![Stránka specifické parametry aplikace ER](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. V poli **Stav** vyberte možnost **Dokončeno**.

    Po spuštění verze formátu ER, která má stav **Dokončeno** nebo **Sdíleno**, musí mít tato sada pravidel stav **Dokončeno**. V opačném případě bude provedení základního formátu ER přerušeno při pokusu o načtení dat z této sady pravidel v době, kdy je spuštěn zdroj dat vyhledávání **Selektor**.
    
    Při spuštění verze formátu ER, která má stav **koncept**, může základní formát ER přistupovat k této sadě pravidel bez ohledu na její stav.
    
17. Zvolte **Uložit**.
18. zavřete stránku **Parametry specifické podle aplikace**.

## <a name="run-the-er-format-in-the-demf-company"></a>Spuštění formátu ER ve společnosti DEMF

1.  Ve stromu konfigurace vyberte formát **Formát pro ověření, jak vyhledat data LE**.
2.  V podokně akcí zvolte **Spustit**.
3.  V zobrazeném dialogovém okně vyberte **OK**.
4.  Stáhněte výpis, který je vygenerován, a uložte ho místně.

    V generovaném výpisu si všimněte, že souhrn kódu daně **InVAT7** byl vložen na **Redukované** úrovni a souhrny **VAT19** d **InVA19** byly umístěny na **běžnou** úroveň. Toto chování je určeno konfigurací pro sadu pravidel závislých na právnické osobě.
    
5.  Přejděte na **Daň \> Nepřímé daně \> DPH \> Kódy DPH**.
6.  Vyberte kód daně **InVAT7**.
7.  V podokně akcí na kartě **Kód DPH** ve skupině **Dotazy** vyberte **Zaúčtovaná DPH** k zobrazení informací o hodnotě daně a použité daňové sazbě podle kódu daně.

    ![Zaúčtovaná stránka DPH](./media/GER-AppSpecParms-Statement.PNG)

8.  Zavřete stránku Zaúčtovaná DPH.

## <a name="set-up-parameters-for-the-usmf-company"></a>Nastavení parametrů pro společnost USMF

1.  Vyberte právnickou osobu **USMF**.
2.  Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.
3.  Ve stromu konfigurací rozbalte položku **Model k učení parametrizovaných volání**, rozbalte položku **Formát k učení se parametrizovaných volání** a vyberte **Formát k učení se, jak vyhledávat data LE**.
4.  V podokně akcí na kartě **Konfigurace** ve skupině **Parametry specifické pro aplikaci** vyberte **Nastavení**.
5.  Vyberte verzi **1.1.1** vybraného formátu ER.
6.  Na pevné záložce **Podmínky** vyberte **Přidat**.
7.  V poli **Kód** nového záznamu výběrem šipky rozevíracího seznamu otevřete vyhledávání.

    Vyhledávání nyní představuje seznam kódů daní pro daň **USMF** společnosti pro výběr.

    ![Stránka specifické parametry aplikace ER](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  Vyberte kód daně **EXEMPT**.
9.  V poli **výsledek vyhledávání** nového záznamu vyberte hodnotu **žádné zdanění**.
10. Znovu vyberte **Přidat**.
11. V poli **kód** nového záznamu vyberte možnost **\*Notblank\***.
12. V poli **výsledek vyhledávání** nového záznamu vyberte hodnotu **běžné zdanění**.
13. V poli **Stav** vyberte možnost **Dokončeno**.
14. Zvolte **Uložit**.

    ![Stránka specifické parametry aplikace ER](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. zavřete stránku **Parametry specifické podle aplikace**.

## <a name="run-the-er-format-in-the-usmf-company"></a>Spuštění formátu ER ve společnosti USMF

1.  Ve stromu konfigurace vyberte formát **Formát pro ověření, jak vyhledat data LE**.
2.  V podokně akcí zvolte **Spustit**.
3.  V zobrazeném dialogovém okně vyberte **OK**.
4.  Stáhněte výpis, který je vygenerován, a uložte ho místně.

    V generovaném příkazu si všimněte, že jste nyní opakovaně použili stejný formát ER pro jinou právnickou osobu, ale bez provedení úprav formátu ER.

## <a name="reuse-legal-entitydependent-parameters"></a>Znovu použít parametry závislé na právnické osobě

### <a name="export-parameters"></a>Parametry exportu

1.  Přejděte do části **Správa organizace \> Pracovní prostory \> Elektronické výkaznictví**.
2.  Vyberte **Konfigurace vykazování**.
3.  Ve stromu konfigurace vyberte formát **Formát pro ověření, jak vyhledat data LE**.
4.  V podokně akcí na kartě **Konfigurace** ve skupině **Parametry specifické pro aplikaci** vyberte **Nastavení**.
5.  Vyberte verzi **1.1.1** formátu ER.
6.  V podokně akcí klikněte na možnost **Export**.
7.  Stáhněte soubor, který je vygenerován, a uložte ho místně.

    Konfigurovaná sada parametrů specifických pro aplikaci byla nyní exportována jako soubor XML.

### <a name="import-parameters"></a>Parametry importu

1.  Vyberte verzi **1.1.2** formátu ER.
2.  V podokně akcí klikněte na možnost **Import**.
3.  Výběrem možnosti **Ano** potvrďte, že chcete přepsat existující parametry specifické pro aplikaci pro tuto verzi formátu.
4.  Vyberte **Procházet**, pokud chcete vyhledat soubor obsahující exportované parametry specifické pro aplikaci verze **1.1.1**.
5.  Vyberte **OK**.

    Verze **1.1.2** ve formátu ER má nyní stejné parametry specifické pro danou aplikaci, které jste původně nakonfigurovali pro verzi **1.1.1**.
    
    Všimněte si, že parametry formátu ER specifické pro aplikaci jsou závislé na právnické osobě. Chcete-li znovu použít specifické parametry aplikace, které byly nakonfigurovány pro jednu právnickou osobu v jiné právnické osobě, je nutné je exportovat v době, kdy jste se přihlásili k první právnické osobě, a poté je importovat po přihlášení k jiné právnické osobě.

    Tento přístup lze také použít k převodu formátu ER, které jsou specifické pro konkrétní aplikace, které byly původně nakonfigurovány v jedné instanci finančního oddělení na jinou instanci modulu finance.

    Uvědomte si, že pokud konfigurujete parametry specifické pro určitou aplikaci pro jednu verzi formátu ER a importujete vyšší verzi stejného formátu do aktuální instance finance, nebudou pro importovanou verzi použity existující parametry specifické pro danou aplikaci.
    
    Je také nutné mít na paměti, že při výběru souboru pro import bude porovnána struktura parametrů specifických pro aplikaci v tomto souboru se strukturou odpovídajícího zdroje dat typu **vyhledávání** ve formátu ER, který je vybrán pro import. Import je proveden v případě, že struktura jednotlivých parametrů specifických pro aplikaci odpovídá struktuře odpovídajícího zdroje dat ve formátu ER vybraném pro import. Pokud se struktury neshodují, zobrazí se varovná zpráva oznamující, že import nelze provést. Pokud vynutíte provedení importu, budou vymazány stávající parametry specifické pro vybraný formát ER a bude nutné je nastavit až od začátku.

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a>Vztah mezi parametry specifickými pro aplikaci a formátem ER

Vztah mezi formátem ER a jeho parametry specifickými pro danou aplikaci je vytvořen jedinečným identifikačním kódem nezávislým na instanci formátu ER. Pokud tedy z modulu Finance odeberete formát ER, budou parametry specifické pro aplikaci, které jsou nakonfigurovány pro formát ER, uloženy v aktuální instanci modulu finance. Lze k nim přistupovat při každém zpětném importu základního formátu ER do této instance modulu Finance.

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a>Přístup k parametrům specifickým pro aplikaci pomocí architektury ER

V předchozím příkladu jste získali přístup k parametrům formátu ER, které jsou specifické pro jednotlivé aplikace, pomocí architektury ER. Tento přístup neumožňuje omezit přístup k parametrům specifického formátu ER, které jsou specifické pro jednotlivé aplikace. Pokud je nutné tato omezení použít, postupujte podle následujících kroků. 

1.  Znovu použijte existující položku nabídky **ERSolutionAppSpecificParametersDesigner** nebo implementujte vlastní položku nabídky **ERSolutionAppSpecificParametersDesigner**.

    ![Stránka Visual Studio](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  Proveďte jeden z následujících kroků:

    1.  Vytvořte tlačítko položky nové nabídky a propojte ho s příslušným záznamem z tabulky **ERSolutionTable** nastavením jeho vlastnosti **Data Source** na **ERSolutionTable**.
    
        ![Stránka Visual Studio](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  Vytvořte jednoduché tlačítko a přepište metodu **Kliknuto**, jak je znázorněno v následujícím příkladu.
    
        Použijete-li tento přístup, můžete zadat jedinečné ID řešení (definované pomocí hodnoty **GUID**), které umožní přístup k parametrům specifickým pouze pro specifický formát ER a kopií, které byly od něj odvozeny.
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a>Další zdroje

[Návrhář receptur v elektronickém výkaznictví](general-electronic-reporting-formula-designer.md)

[Konfigurace formátů ER pro použití parametrů zadaných pro právnickou osobu](er-app-specific-parameters-configure-format.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
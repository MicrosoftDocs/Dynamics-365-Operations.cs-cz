---
title: Nastavení parametrů formátu elektronického výkaznictví podle právnické osoby
description: V tomto článku je vysvětleno, jak nastavit parametry formátu elektronického výkaznictví (ER) podle právnické osoby.
author: NickSelin
ms.date: 03/25/2022
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
ms.openlocfilehash: dbcf968dde432da182b5bd2d6a7bcb9f83dad6fa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890205"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a>Nastavení parametrů formátu ER podle právnické osoby

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a>Předpoklady

Chcete-li provést tento postup, musíte nejprve dokončit kroky v tématu [Nastavení formátů ER, které budou používat parametry specifikované podle právnické osoby](er-app-specific-parameters-configure-format.md).

K dokončení příkladů v tomto článku musíte mít přístup k aplikaci Microsoft Dynamics 365 Finance pro některou z následujících rolí:

- Návrhář elektronického výkaznictví
- Funkční konzultant elektronického výkaznictví
- Správce systému

## <a name="import-er-configurations"></a>Import konfigurací ER
K importu konfigurací ER postupujte takto: 

1. Přihlaste se k prostředí.
2. Na výchozím řídicím panelu vyberte **Elektronické vykazování**.
3. Vyberte **Konfigurace vykazování**.
4. Importujte do aktuální instance aplikace Finance konfigurace, které jste exportovali ze služby Regulatory Configuration Services (RCS) při dokončování kroků v tématu [Konfigurace formátů ER pro použití parametrů zadaných pro právnickou osobu](er-app-specific-parameters-configure-format.md). Tyto kroky proveďte pro každou konfiguraci [elektronického výkaznictví (ER)](general-electronic-reporting.md) v následujícím pořadí: datový model, mapování modelu a formáty.

    1. Vyberte **Exchange \> Načíst ze souboru XML**.
    2. Zvolte **Procházet** a vyberte soubor pro požadovanou konfiguraci elektronického výkaznictví ve formátu XML.
    3. Vyberte **OK**.

    Následující ilustrace znázorňuje konfigurace, které je nutné mít po dokončení.

    ![Stránka konfigurací elektronického výkaznictví.](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a>Nastavení parametrů pro společnost DEMF

Pomocí systému ER můžete nastavit specifické parametry aplikace pro formát ER.

1. Vyberte právnickou osobu **DEMF**.
2. Ve stromu konfigurace vyberte formát **Formát pro ověření, jak vyhledat data LE**.
3. V podokně akcí na kartě **Konfigurace** ve skupině **Parametry specifické pro aplikaci** vyberte **Nastavení**.

    ![Stránka parametrů specifických pro ER pro nastavení parametrů.](./media/GER-AppSpecParms-LookupForm.PNG)

    Na stránce **Parametry specifické pro aplikaci** můžete konfigurovat pravidla pro zdroj dat **Selektor** formátu **Formát pro učení se, jak vyhledávat data ER**.

    Pokud základní formát ER bude obsahovat několik zdrojů dat typu **vyhledávání**, musíte vybrat požadovaný zdroj dat na pevné záložce **Vyhledávání** před zahájením konfigurace sady pravidel pro zdroj dat.

    Pro každý zdroj dat lze nakonfigurovat samostatná pravidla pro každou verzi vybraného formátu ER.

    Celá sada pravidel pro všechny vyhledávací zdroje dat, které jsou k dispozici ve vybrané verzi základního formátu ER, tvoří parametry specifické pro aplikaci ve formátu ER.

4. Vyberte verzi **1.1.1** formátu ER.
5. Na pevné záložce **Podmínky** vyberte **Přidat**.
6. V poli **Kód** nového záznamu výběrem šipky rozevíracího seznamu otevřete vyhledávání.

    Vyhledávání představuje seznam kódů daní pro výběr. Tento seznam je vrácen zdrojem dat **Model.Data.Tax**, který byl nakonfigurován v základním formátu ER. Vzhledem k tomu, že tento zdroj dat obsahuje pole **Název**, zobrazí se názvy jednotlivých kódů daní ve vyhledávání.

    ![Vyhledání pole kódu na stránce specifických parametrů aplikace ER.](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)

7. Vyberte kód daně **VAT19**.
8. V poli **Výsledek vyhledávání** nového záznamu výběrem šipky rozevíracího seznamu otevřete vyhledávání. Vyhledávání představuje seznam hodnot pro formát výčtu TaxationLevel pro výběr.

    Všimněte si, že pokud je jako preferovaný jazyk uživatele, jako který jste přihlášeni, vybrána němčina, budou popisky hodnot ve vyhledávání v němčině, pokud byly přeloženy do formátu Base ER. Kromě toho, pokud byl přeložen popisek vyhledávacího zdroje dat, bude tento popisek zobrazen na kartě **vyhledávání** v preferovaném jazyce uživatele.

    ![Vyhledávací pole přeložené do němčiny na stránce parametrů specifických pro aplikaci ER.](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9. Vyberte hodnotu **Běžné zdanění**.

    Přidáte-li tento záznam, definujete následující pravidlo: když je požadován zdroj dat vyhledávání **Selektor**, je požadován datový zdroj výběru, a kód DPH **VAT19** je předán jako argument, bude vrácena hodnota **Běžné zdanění** jako požadovaná úroveň zdanění.

10. Vyberte **přidat** a postupujte podle následujících kroků:

    1. V poli **Kód** vyberte kód daně **InVAT19**.
    2. V poli **výsledek vyhledávání** vyberte hodnotu **normální zdanění**.

11. Vyberte **přidat** a postupujte podle následujících kroků:

    1. V poli **Kód** vyberte kód daně **VAT7**.
    2. V poli **výsledek vyhledávání** vyberte hodnotu **redukované zdanění**.

12. Vyberte **přidat** a postupujte podle následujících kroků:

    1. V poli **Kód** vyberte kód daně **InVAT7**.
    2. V poli **výsledek vyhledávání** vyberte hodnotu **redukované zdanění**.

13. Vyberte **přidat** a postupujte podle následujících kroků:

    1. V poli **Kód** vyberte kód daně **THIRD**.
    2. V poli **výsledek vyhledávání** vyberte hodnotu **žádné zdanění**.

14. Vyberte **přidat** a postupujte podle následujících kroků:

    1. V poli **Kód** vyberte kód daně **InVAT0**.
    2. V poli **výsledek vyhledávání** vyberte hodnotu **žádné zdanění**.

15. Vyberte **přidat** a postupujte podle následujících kroků:

    1. V poli **kód** vyberte možnost **\*Notblank\***.
    2. V poli **výsledek vyhledávání** vyberte hodnotu **Jiné**.

    Přidáte-li tento poslední záznam, definujete následující pravidlo: když kód daně předaný jako argument nesplňuje žádné z předchozích pravidel, vrátí zdroj dat vyhledávání jako požadovanou úroveň zdanění **Jiné**.

    ![Poslední přidaný záznam na stránce specifických parametrů aplikace ER.](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)

16. V poli **Stav** vyberte možnost **Dokončeno**.

    Po spuštění verze formátu ER, která má stav **Dokončeno** nebo **Sdíleno**, musí mít tato sada pravidel stav **Dokončeno**. V opačném případě bude provedení základního formátu ER přerušeno při pokusu o načtení dat z této sady pravidel v době, kdy je spuštěn zdroj dat vyhledávání **Selektor**.

    Při spuštění verze formátu ER, která má stav **koncept**, může základní formát ER přistupovat k této sadě pravidel bez ohledu na její stav.

17. Zvolte **Uložit**.
18. zavřete stránku **Parametry specifické podle aplikace**.

## <a name="run-the-er-format-in-the-demf-company"></a>Spuštění formátu ER ve společnosti DEMF
Ke spuštění formátu ER ve společnosti DEMF postupujte následovně: 

1. Ve stromu konfigurace vyberte formát **Formát pro ověření, jak vyhledat data LE**.
2. V podokně akcí zvolte **Spustit**.
3. V zobrazeném dialogovém okně vyberte **OK**.
4. Stáhněte výpis, který je vygenerován, a uložte ho místně.

    V generovaném výpisu si všimněte, že souhrn kódu daně **InVAT7** je na **Redukované** úrovni a souhrny **VAT19** d **InVA19** jsou na **běžné** úrovni. Toto chování je určeno konfigurací pro sadu pravidel závislých na právnické osobě.

5. Přejděte na **Daň \> Nepřímé daně \> DPH \> Kódy DPH**.
6. Vyberte kód daně **InVAT7**.
7. V podokně akcí na kartě **Kód DPH** ve skupině **Dotazy** vyberte **Zaúčtovaná DPH** k zobrazení informací o hodnotě daně a použité daňové sazbě podle kódu daně.

    ![Zaúčtovaná stránka DPH.](./media/GER-AppSpecParms-Statement.PNG)

8. Zavřete stránku **Zaúčtovaná DPH**.

## <a name="set-up-parameters-for-the-usmf-company"></a>Nastavení parametrů pro společnost USMF
Chcete-li nastavit parametry pro společnost USMF, proveďte následující kroky: 

1. Vyberte právnickou osobu **USMF**.
2. Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.
3. Ve stromu konfigurací rozbalte položku **Model k učení parametrizovaných volání**, rozbalte položku **Formát k učení se parametrizovaných volání** a vyberte **Formát k učení se, jak vyhledávat data LE**.
4. V podokně akcí na kartě **Konfigurace** ve skupině **Parametry specifické pro aplikaci** vyberte **Nastavení**.
5. Vyberte verzi **1.1.1** vybraného formátu ER.
6. Na pevné záložce **Podmínky** vyberte **Přidat**.
7. V poli **Kód** nového záznamu výběrem šipky rozevíracího seznamu otevřete vyhledávání.

    Vyhledávání nyní představuje seznam kódů daní pro daň **USMF** společnosti pro výběr.

    ![Daňové kódy pro daň společnosti USMF.](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)

8. Vyberte kód daně **EXEMPT**.
9. V poli **výsledek vyhledávání** nového záznamu vyberte hodnotu **žádné zdanění**.
10. Vyberte **přidat**.
11. V poli **kód** nového záznamu vyberte možnost **\*Notblank\***.
12. V poli **výsledek vyhledávání** nového záznamu vyberte hodnotu **běžné zdanění**.
13. V poli **Stav** vyberte možnost **Dokončeno**.
14. Zvolte možnost **Uložit**.

    ![Stránka specifické parametry aplikace ER.](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)

15. zavřete stránku **Parametry specifické podle aplikace**.

## <a name="run-the-er-format-in-the-usmf-company"></a>Spuštění formátu ER ve společnosti USMF
Ke spuštění formátu ER ve společnosti USMF postupujte následovně:

1. Ve stromu konfigurace vyberte formát **Formát pro ověření, jak vyhledat data LE**.
2. V podokně akcí zvolte **Spustit**.
3. V zobrazeném dialogovém okně vyberte **OK**.
4. Stáhněte výpis, který je vygenerován, a uložte ho místně.

    V generovaném příkazu si všimněte, že jste nyní opakovaně použili stejný formát ER pro jinou právnickou osobu, ale bez provedení úprav formátu ER.

## <a name="reuse-legal-entitydependent-parameters"></a>Znovu použít parametry závislé na právnické osobě

### <a name="duplicate-existing-parameters"></a>Duplicitní existující parametry

#### <a name="export-parameters"></a>Parametry exportu
Pomocí následujících kroků exportujete parametry:

1. Přejděte do části **Správa organizace \> Pracovní prostory \> Elektronické výkaznictví**.
2. Vyberte **Konfigurace vykazování**.
3. Ve stromu konfigurace vyberte formát **Formát pro ověření, jak vyhledat data LE**.
4. V podokně akcí na kartě **Konfigurace** ve skupině **Parametry specifické pro aplikaci** vyberte **Nastavení**.
5. Vyberte verzi **1.1.1** formátu ER.
6. V podokně akcí klikněte na možnost **Export**.
7. Stáhněte soubor, který je vygenerován, a uložte ho místně.

    Konfigurovaná sada parametrů specifických pro aplikaci byla nyní exportována jako soubor XML.

#### <a name="import-parameters"></a>Parametry importu
Pomocí následujících kroků importujete parametry:

1. Vyberte verzi **1.1.2** formátu ER.
2. V podokně akcí klikněte na možnost **Import**.
3. Výběrem možnosti **Ano** potvrďte, že chcete přepsat existující parametry specifické pro aplikaci pro tuto verzi formátu.
4. Vyberte **Procházet**, pokud chcete vyhledat soubor obsahující exportované parametry specifické pro aplikaci verze **1.1.1**.
5. Vyberte **OK**.

    Verze **1.1.2** ve formátu ER má nyní stejné parametry specifické pro danou aplikaci, které jste původně nakonfigurovali pro verzi **1.1.1**.

##### <a name="applicability-considerations"></a>Posouzení použitelnosti

Parametry formátu ER specifické pro aplikaci jsou závislé na právnické osobě. Chcete-li znovu použít specifické parametry aplikace, které byly nakonfigurovány pro jednu právnickou osobu v jiné právnické osobě, je nutné je exportovat v době, kdy jste se přihlásili k první právnické osobě. Poté je importujte po přihlášení k jiné právnické osobě.

Tento přístup exportu a importu lze také použít k převodu formátu ER, které jsou specifické pro konkrétní aplikace, které byly původně nakonfigurovány v jedné instanci finančního oddělení na jinou instanci modulu finance.

Pokud nakonfigurujete parametry specifické pro aplikaci pro jednu verzi formátu ER a poté importujete novější verzi stejného formátu do aktuální instance Finance, stávající parametry specifické pro aplikaci se na importovanou verzi nepoužijí, pokud nepoužijete funkci **Použít parametry specifické pro aplikaci z předchozích verzí formátů ER**. Více informací naleznete v části [Opětovné použití stávajících parametrů](#reuse-existing-parameters) dále v tomto článku.

Při výběru souboru pro import bude porovnána struktura parametrů specifických pro aplikaci v tomto souboru se strukturou odpovídajících zdrojů dat typu **vyhledávání** ve formátu ER, který je vybrán pro import. Ve výchozím nastavení je import proveden pouze v případě, že struktura jednotlivých parametrů specifických pro aplikaci odpovídá struktuře odpovídajícího zdroje dat ve formátu ER vybraném pro import. Pokud se struktury neshodují, zobrazí se varovná zpráva oznamující, že import nelze provést. Pokud import vynutíte, budou vymazány stávající parametry specifické pro vybraný formát ER a bude nutné je nastavit až od začátku.


Od verze 10.0.24 aplikace Finance můžete změnit výchozí chování a vyhnout se přijímání varovné zprávy aktivací funkce **Při importu zarovnejte parametry specifické pro aplikaci elektronického výkaznictví** v pracovním prostoru **Správa funkcí**. Když je tato funkce aktivní a struktura parametrů specifických pro aplikaci, které importujete se liší od struktury odpovídajících zdrojů dat v cílovém formátu ER, který je vybrán pro import, import se podaří v následujících případech:

- Struktura cílového formátu ER byla změněna přidáním nových sloupců podmínek do libovolných existujících zdrojů dat typu **Vyhledat**. Po dokončení importu se aktualizují parametry specifické pro aplikaci. Ve všech importovaných záznamech parametrů specifických pro aplikaci jsou hodnoty v každém přidaném sloupci podmínky inicializovány s výchozí hodnotou pro [datový typ](er-formula-supported-data-types-primitive.md) toho sloupce.
- Struktura cílového formátu ER byla změněna odstraněním některých sloupců podmínek z libovolných existujících zdrojů dat typu **Vyhledat**. Po dokončení importu se aktualizují parametry specifické pro aplikaci. Ve všech importovaných záznamech parametrů specifických pro aplikaci jsou odstraněny hodnoty v každém sloupci odstraněných podmínek.
- Struktura cílového formátu ER byla změněna přidáním nových zdrojů dat typu **Vyhledat**. Po dokončení importu se přidaná vyhledávání připojí k parametrům specifickým pro aplikaci.
- Struktura cílového formátu ER byla změněna odstraněním některých existujících zdrojů dat typu **Vyhledat**. Po dokončení importu všechny artefakty, které souvisejí se zdroji dat typu **Vyhledat**, které byly odstraněny z cílového formátu ER, jsou odstraněny z importovaných parametrů specifických pro aplikaci.

Po dokončení importu se kromě změn, které byly právě popsány, změní stav importovaných parametrů specifických pro aplikaci na **Probíhá**. Varovné hlášení vás informuje, že automaticky nastavené parametry specifické pro aplikaci je nutné upravit ručně.

#### <a name="replicate-parameters"></a>Replikace parametrů

Od verze 10.0.27 aplikace Finance můžete zkopírovat parametry, které jste konfigurovali v jedné společnosti, do jiných společností současně.

Pomocí následujících kroků zkopírujete parametry.

1. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
2. Vyberte **Konfigurace vykazování**.
3. Ve stromu konfigurace vyberte formát **Formát pro ověření, jak vyhledat data LE**.
4. V podokně akcí na kartě **Konfigurace** ve skupině **Parametry specifické pro aplikaci** vyberte **Nastavení**.
5. Vyberte verzi **1.1.1** formátu ER.
6. V podokně Akce klikněte na možnost **Replikovat**.
7. V dialogu **Replikovat** na kartě **Společnosti** vyberte společnosti, do kterých chcete parametry zkopírovat.

    > [!NOTE]
    > Seznam cílových společností je nabízen pouze uživatelům s přiřazenou [rolí zabezpečení](../sysadmin/role-based-security.md#security-roles), která uděluje přístup ke všem organizacím.

8. Vyberte **OK**.

    > [!NOTE]
    > Potvrzovací dialogové okno vás informuje o tom, že některé cílové společnosti obsahují dříve konfigurované parametry pro vybranou verzi formátu ER. Výběrem možnosti **Ano** přepíšete parametry jejich zkopírováním z aktuální společnosti.

    Konfigurovaná sada parametrů specifických pro aplikaci je nyní zkopírována do vybraných společností.

### <a name="reuse-existing-parameters"></a>Opakované použití existujících parametrů

Od verze 10.0.23 aplikace Finance můžete znovu použít parametry specifické pro aplikaci, které byly nakonfigurovány pro jednu verzi formátu ER, když spustíte vyšší verzi stejného formátu. Chcete-li znovu použít existující parametry, aktivujte funkci **Použít parametry specifické pro aplikaci z předchozích verzí formátů ER** v pracovním prostoru **Správa funkcí**. Když je tato funkce povolena a spustíte jednu verzi formátu ER, která se pokouší číst parametry specifické pro aplikaci, ER se pokusí najít parametry specifické pro aplikaci, které byly konfigurovány pro běžící verzi tohoto formátu. Když nejsou k dispozici, ER zkusí najít parametry pro nejbližší nižší verzi tohoto formátu.

> [!NOTE]
> Parametry specifické pro aplikaci můžete znovu použít pouze v rozsahu aktuálního právního subjektu.
>
> Chyba se zobrazí za běhu, když spustíte vyšší verzi formátu ER, která se pokouší znovu použít parametry specifické pro aplikaci, které byly nakonfigurovány pro nižší verzi stejného formátu, a struktura alespoň jednoho zdroje dat typu **Vyhledat** ve vyšší verzi formátu se změnila.

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a>Vztah mezi parametry specifickými pro aplikaci a formátem ER

Vztah mezi formátem ER a jeho parametry specifickými pro danou aplikaci je vytvořen jedinečným identifikačním kódem nezávislým na instanci formátu ER. Pokud tedy z modulu Finance odeberete formát ER, budou parametry specifické pro aplikaci, které jsou nakonfigurovány pro formát ER, uloženy v aktuální instanci modulu finance. Lze k nim přistupovat při zpětném importu základního formátu ER do této instance modulu Finance.

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a>Přístup k parametrům specifickým pro aplikaci pomocí architektury ER

V předchozím příkladu jste získali přístup k parametrům formátu ER, které jsou specifické pro jednotlivé aplikace, pomocí architektury ER. Tento přístup neumožňuje omezit přístup k parametrům specifického formátu ER, které jsou specifické pro jednotlivé aplikace. Pokud je nutné tato omezení použít, postupujte podle následujících kroků. 

1. Znovu použijte existující položku nabídky **ERSolutionAppSpecificParametersDesigner** nebo implementujte vlastní položku nabídky **ERSolutionAppSpecificParametersDesigner**.

    ![Zobrazení položky nabídky ERSolutionAppSpecificParametersDesigner.](./media/GER-AppSpecParms-LookupForm-Access1.PNG)

2. Proveďte jeden z následujících kroků:

    1. Vytvořte tlačítko položky nové nabídky a propojte ho s příslušným záznamem z tabulky **ERSolutionTable** nastavením jeho vlastnosti **Data Source** na **ERSolutionTable**.

        ![Zobrazení nastavení nových položek nabídky.](./media/GER-AppSpecParms-LookupForm-Access2.PNG)

    2. Vytvořte jednoduché tlačítko a přepište metodu **Kliknuto**, jak je znázorněno v následujícím příkladu.

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

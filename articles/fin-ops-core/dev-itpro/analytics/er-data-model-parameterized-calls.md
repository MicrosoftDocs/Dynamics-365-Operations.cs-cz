---
title: Podpora parametrizovaných volání datových modelů ER
description: Tento článek vysvětluje, jak implementovat parametrizovaná volání datových modelů Elektronického výkaznictví (ER).
author: kfend
ms.date: 03/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: 10.0.15
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula, ERDataModelDesigner
ms.openlocfilehash: 5be189c19d963991ec012de189bbf7b721b88fef
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275981"
---
# <a name="support-parameterized-calls-of-er-data-models"></a>Podpora parametrizovaných volání datových modelů ER

[!include [banner](../includes/banner.md)]

Chcete-li generovat obchodní dokumenty, konfigurujte řešení [Elektronické výkaznictví (ER)](general-electronic-reporting.md), které obsahuje následující komponenty ER:

- **[Formát](er-overview-components.md#format-component)** – Tato komponenta určuje strukturu obchodního dokumentu.
- **Mapování formátu** – Tato komponenta řídí, jak se obchodní dokument za běhu vyplní informacemi.
- **[Mapování modelu](er-overview-components.md#model-mapping-component)** – Tato komponenta určuje, co data přebírají z aplikace do mapování formátu.
- **[Datový model](er-overview-components.md#data-model-component)** – Tato komponenta předává informace mezi jednotlivými komponentami.

Když spustíte formát ER, spustí se každý prvek formátu, počínaje kořenovým prvkem. Jestliže spuštěný prvek formátu obsahuje vazbu na [zdroj dat](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents), tento zdroj dat se spustí, aby dodal očekávaná data a použil je k vyplnění prvku formátu. Když je zavolán zdroj dat typu *Model*, zavolá se příslušné mapování modelu, které načte data z aplikace na základě nastavení mapování modelu.

Dříve nebylo možné tato volání mapování modelu parametrizovat, aby byla závislá na logice spouštěného formátu. Podporován byl pouze následující datový tok.

<table>
<tbody>
<tr align="center">
<td>
<b>Formát</b><br>
Prvek&nbsp;formátu<br>
&nbsp;
</td>
<td>
<i>Vazba</i><br>
&gt;&nbsp;žádost&nbsp;&gt;<br>
&lt;&nbsp;hodnota&nbsp;&lt;
</td>
<td><b>Mapování&nbsp;formátu</b><br>
Zdroj dat<br>
&nbsp;
</td>
<td>
<i>Datový&nbsp;model</i><br>
&gt;&nbsp;žádost&nbsp;&gt;<br>
&lt;&nbsp;hodnota&nbsp;&lt;
</td>
<td>
<b>Mapování&nbsp;modelu</b><br>
Zdroj&nbsp;dat<br>
&nbsp;
</td>
<td>
<i>Vazba</i><br>
&gt;&nbsp;žádost&nbsp;&gt;<br>
&lt;&nbsp;hodnota&nbsp;&lt;
</td>
<td>
<b>Tabulka</b><br>
Záznam<br>
Pole
</td>
</tr>
</tbody>
</table>

Ve verzi 10.0.15 a novější však můžete konfigurovat pole datového modelu, která lze volat pouze tehdy, jsou-li uvedeny hodnoty konfigurovaných parametrů. Když je takové pole konfigurováno a voláno z komponenty formátu, musejí být požadované parametry zadány ve vazbě formátu jako argumenty volání. V těchto případech lze hodnoty argumentů zadat na základě hodnot specifických pro daný formát. Proto můžete použít **dynamickou parametrizaci spuštění** pro volání datového modelu, která podporují následující datový tok.

<table>
<tbody>
<tr align="center">
<td>
<b>Formát</b><br>
Prvek&nbsp;formátu&nbsp;1<br>
<br>
Prvek&nbsp;formátu&nbsp;2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Vazba</i><br>
&gt;&nbsp;žádost&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;hodnota&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;žádost&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;hodnota&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Mapování&nbsp;formátu</b><br>
Zdroj&nbsp;dat&nbsp;1<br>
&nbsp;<br>
<b>hodnota2=Func(hodnota1)</b><br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Datový&nbsp;model</i><br>
&gt;&nbsp;pole1&nbsp;&gt;<br>
&lt;&nbsp;hodnota&nbsp;1&nbsp;&lt;<br>
<b>&gt;&nbsp;pole2(hodnota2)&nbsp;&gt;</b><br>
&lt;&nbsp;hodnota&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Mapování&nbsp;modelu</b><br>
Zdroj&nbsp;dat&nbsp;1<br>
<br>
Zdroj&nbsp;dat&nbsp;2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Vazba</i><br>
&gt;&nbsp;žádost&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;hodnota&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;žádost&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;hodnota&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Tabulka&nbsp;1</b><br>
Záznam&nbsp;1<br>
Pole&nbsp;1<br>
<b>Tabulka&nbsp;2</b><br>
Záznam&nbsp;2<br>
Pole&nbsp;2
</td>
</tr>
</tbody>
</table>

Nová funkce umožňuje parametrizovat volání libovolného pole datového modelu typu [*Záznam*](er-formula-supported-data-types-composite.md#record) nebo [*Seznam záznamů*](er-formula-supported-data-types-composite.md#record-list). U parametrů pole datového modelu jsou podporovány následující datové typy:

- [Logická](er-formula-supported-data-types-primitive.md#boolean)
- [Kontejner](er-formula-supported-data-types-composite.md#container)
- [Datum](er-formula-supported-data-types-primitive.md#date)
- [Datum/čas](er-formula-supported-data-types-primitive.md#datetime)
- [GUID](er-formula-supported-data-types-primitive.md#guid)
- [Int64](er-formula-supported-data-types-primitive.md#int64)
- [Celé číslo](er-formula-supported-data-types-primitive.md#integer)
- [Reálný](er-formula-supported-data-types-primitive.md#real)
- [Řetězec](er-formula-supported-data-types-primitive.md#string)

Zadat můžete každý parametr pole datového modelu, u kterého lze argument poskytnout jako jednu hodnotu definovaného datového typu a [*seznam*](er-formula-supported-data-types-composite.md#record-list) takových hodnot.

> [!NOTE]
> Výchozí hodnota není u parametru pole datového modelu podporována. Když přidáte parametr do pole v datovém modelu a verze tohoto datového modelu již byla vydána a publikována, musíte [přeskládat](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) všechna odpovídající mapování a formáty modelu na novou verzi tohoto modelu, protože tato změna datového modelu není zpětně kompatibilní.

Pole parametrizovaných datových modelů můžete konfigurovat tak, aby byla volání mapování modelu závislá na formátu. Tento přístup vám pomůže snížit počet mapování modelu, která musí být konfigurována pro více formátů jednoho datového modelu. Tento přístup můžete také použít ke zlepšení výkonu svých formátů a zkrácení času potřebného k generování obchodních dokumentů. Chcete-li získat další informace o této funkci, vyplňte příklad tomto článku.

## <a name="example-use-parameterized-calls-of-er-data-models"></a>Příklad: Podpora parametrizovaných volání datových modelů ER

Následující kroky vysvětlují, jak může uživatel s rolí Správce systému nebo Návrhář elektronického výkaznictví navrhnout řešení ER, které obsahuje datový model, mapování modelu a komponentu ER formátu, které jsou konfigurovány pro volání mapování modelu z formátu poskytnutím argumentu pro volání, jehož hodnota byla vypočtena za běhu pomocí vzorce spuštěného formátu. 

Tyto kroky lze provést v rámci společnosti **DEMF**. Nejsou vyžadovány žádné úpravy kódu. 

V tomto příkladu vytvoříte požadované [konfigurace](general-electronic-reporting.md#Configuration) ER pro vzorovou společnost **Litware, Inc**. Ověřte, že je dostupný poskytovatel konfigurace ukázkové společnosti **Litware, Inc.** (`http://www.litware.com`) uveden pro rámec ER a že označen jako **Aktivní**. Není-li tento poskytovatel konfigurace uveden v seznamu nebo není-li označen jako **Aktivní**, postupujte podle kroků v tématu [Vytvoření poskytovatele konfigurace a jeho označení jako aktivního](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="business-scenario"></a>Scénáře obchodu

Máte řešení ER obsahující formát, který můžete spustit a generovat v něm elektronický dokument pro účely auditu. Tento formát obsahuje daňové transakce, které souvisejí s prodejními objednávkami a nákupními objednávkami a které obsahují požadované podrobnosti, jako je datum transakce a daňová hodnota. Od nového fiskálního roku se struktura tohoto dokumentu změnila. Nyní musíte odeslat rozšířený dokument, který obsahuje další podrobnosti (jména) všech stran (zákazníků a dodavatelů), jejichž transakce jsou prezentovány na generovaných sestavách. Proto musíte upravit své řešení ER tak, aby generovalo dokumenty splňující tento nový požadavek.

### <a name="configure-the-er-framework"></a>Konfigurace rámce ER

Postupujte podle kroků uvedených v části [Konfigurace architektury ER](er-quick-start2-customize-report.md#ConfigureFramework) a nastavte minimální sadu parametrů ER. Toto nastavení musíte dokončit, než začnete používat architekturu ER k návrhu nového řešení ER.

### <a name="design-a-domain-specific-data-model"></a>Návrh datového modelu specifického pro doménu

Musíte vytvořit novou konfiguraci ER obsahující požadovanou komponentu datového modelu. Tento datový model bude později použit jako zdroj dat, když navrhujete formát ER pro generování auditní sestavy.

Chcete-li importovat požadovaný datový model ze souboru XML, který poskytuje společnost Microsoft, postupujte podle těchto kroků.

1. Stáhněte si soubor [Sample audit model.version.1.xml](https://download.microsoft.com/download/7/1/9/719b0132-fed7-4c73-8afa-90cac29c2fee/Sample-audit-model.version.1.xml) a uložte jej do místního počítače.
2. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
3. V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.
4. Na stránce **Konfigurace** v podokně akcí vyberte možnost **Exchange** \> **Načíst ze souboru XML**.
5. Vyberte **Procházet**, a poté najděte a vyberte soubor **Sample audit model.version.1.xml**.
6. Kliknutím na tlačítko **OK** importujte konfiguraci.

    ![Importovaná konfigurace datového modelu ER na stránce Konfigurace.](./media/er-data-model-parameterized-calls-imported-model.png)

Následující obrázek ukazuje upravitelnou verzi konfigurovaného datového modelu na stránce **Návrhář datového modelu**.

![Struktura datového modelu ER na stránce Návrhář datového modelu.](./media/er-data-model-parameterized-calls-model1.png)

V současné době je model navržen tak, aby zveřejňoval pouze daňové transakce, které mají požadované podrobnosti.

### <a name="design-a-model-mapping-for-the-configured-data-model"></a>Návrh mapování modelu pro konfigurovaný datový model

Jako uživatel v roli Návrhář elektronického výkaznictví musíte vytvořit novou konfiguraci ER, která obsahuje komponentu mapování modelu pro datový model Sample audit. Tato komponenta implementuje konfigurovaný datový model pro Microsoft Dynamics 365 Finance a je specifická pro tuto aplikaci. Komponentu mapování modelu musíte nakonfigurovat, abyste určili aplikační objekty, které musí být použity k vyplnění nakonfigurovaného datového modelu aplikačními daty za běhu. K provedení tohoto úkolu musíte chápat implementaci datové struktury daňové obchodní domény ve Finance.

Chcete-li importovat požadované mapování modelu ze souboru XML, který poskytuje společnost Microsoft, postupujte podle těchto kroků.

1. Stáhněte si soubor [Sample audit model mapping.version.1.1.xml](https://download.microsoft.com/download/c/0/3/c03a4673-b1b1-4ef8-96d0-bf96518be6e0/Sample-audit-model-mapping.version.1.1.xml) a uložte jej do místního počítače.
2. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
3. V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.
4. Na stránce **Konfigurace** v podokně akcí vyberte možnost **Exchange** \> **Načíst ze souboru XML**.
5. Vyberte **Procházet**, a poté najděte a vyberte soubor **Sample audit model mapping.version.1.1.xml**.
6. Kliknutím na tlačítko **OK** importujte konfiguraci.

    ![Importovaná konfigurace mapování modelu ER na stránce Konfigurace.](./media/er-data-model-parameterized-calls-imported-mapping.png)

Následující obrázek ukazuje upravitelnou verzi konfigurovaného mapování modelu na stránce **Návrhář mapování modelu**.

![Struktura mapování modelu ER na stránce Návrhář mapování modelu.](./media/er-data-model-parameterized-calls-mapping1.png)

V současné době je mapování modelu navrženo tak, aby zveřejňovalo daňové transakce, které mají požadované podrobnosti. Tyto informace získává z aplikační tabulky `TaxTrans` pomocí konfigurovaných zdrojů dat ER `TaxTrans` a `TaxTransFiltered`.

### <a name="design-a-new-format"></a>Návrh nového formátu

Jako uživatel v roli funkčního konzultanta elektronického výkaznictví musíte vytvořit novou konfiguraci ER, která obsahuje komponent formát. Komponentu formátu musíte konfigurovat, aby vyplnila generované sestavy daňovými transakcemi, které mají všechny požadované podrobnosti.

Chcete-li importovat požadovaný formát ze souboru XML, který poskytuje společnost Microsoft, postupujte podle těchto kroků.

1. Stáhněte si soubor [Sample audit format.version.1.1.xml](https://download.microsoft.com/download/e/b/7/eb7e126e-2bb3-4bbb-a735-ffd4c48920b1/Sample-audit-format.version.1.1.xml) a uložte jej do místního počítače.
2. Přejděte do části **Správa organizace** \> **Pracovní prostory** \> **Elektronické výkaznictví**.
3. V pracovním prostoru **Elektronické výkaznictví** vyberte dlaždici **Konfigurace výkaznictví**.
4. Na stránce **Konfigurace** v podokně akcí vyberte možnost **Exchange** \> **Načíst ze souboru XML**.
5. Vyberte **Procházet**, a poté najděte a vyberte soubor **Sample audit format.version.1.1.xml**.
6. Kliknutím na tlačítko **OK** importujte konfiguraci.

    ![Importovaná konfigurace formátu ER na stránce Konfigurace.](./media/er-data-model-parameterized-calls-imported-format.png)

Následující obrázek ukazuje upravitelnou verzi konfigurovaného formátu na stránce **Návrhář formátu**.

![Struktura formátu ER na stránce Návrhář formátů.](./media/er-data-model-parameterized-calls-format1.png)

Formát ER je konfigurován pro generování sestavy jako textového souboru ve formátu CSV (s hodnotami oddělenými čárkou).

### <a name="run-the-imported-format"></a>Spuštění importovaného formátu

1. Na stránce **Konfigurace** vyberte konfiguraci **Formát Sample audit** a poté v podokně akcí vyberte **Spustit**.
2. V dialogovém okně **Parametry elektronického výkaznictví** na kartě **Záznamy k zahrnutí** vyberte **Filtrovat**.
3. Zadejte podmínky pro výběr daňových transakcí dokladů **PIV-110000004** a **INV-10000001**.
4. Vyberte **OK**.
5. Vyberte **OK**.
6. Zkontrolujte vygenerovaný dokument, který obsahuje daňové transakce vybraných dokladů.

    ![Náhled vygenerovaného dokumentu s daňovými transakcemi.](./media/er-data-model-parameterized-calls-output1.png)

### <a name="adjust-the-imported-er-solution"></a>Úprava importovaného řešení ER

Na základě nového nařízení musí odesílaný dokument obsahovat jména zákazníků a prodejců, jejichž transakce jsou zahrnuty. Proto musíte upravit importované řešení ER tak, aby generovalo dokument splňující toto nové nařízení.

Rozhodněte se, jak chcete implementovat požadované úpravy importovaných komponent ER.

Běžným přístupem je implementace následujících úprav:

- V datovém modelu přidejte nové pole datového modelu `Transaction.Party.Name` typu *Řetězec*.
- V mapování modelu konfigurujte vazbu pro nové pole datového modelu pomocí dostupných relací tabulek pro přístup k příslušnému záznamu aplikační tabulky `DirPartyTable` a načtení hodnoty pole `Name` z ní.

Ačkoli tento přístup bude fungovat, může způsobit problémy s výkonem v databázi SQL, protože `TaxTrans` je transakční tabulka a může tedy obsahovat velký objem záznamů. V tomto případě počet volání do tabulky `DirPartyTable` se musí rovnat počtu záznamů v tabulce `TaxTrans`, což může způsobit problémy s výkonem.

Případně můžete implementovat následující úpravy:

- V datovém modelu přidejte nový kořen `Party` a nové pole `Party.Name`.
- V mapování modelu přidejte nový zdroj dat, který spojí všechny záznamy tabulek používaných v relacích tabulek, abyste získali přístup k příslušnému záznamu aplikační tabulky `DirPartyTable`, počínaje tabulkou `TaxTrans`.

Ačkoli tento přístup bude fungovat, může dojít k nadměrné spotřebě paměti. I když bude nový zdroj dat [JOIN](er-join-data-sources.md) spuštěn jako jediný požadavek SQL do databáze aplikace, aby se předešlo problémům s výkonem databáze, musí být výsledek načten do paměti aplikačního serveru. Protože počet záznamů a počet polí v těchto záznamech bude poměrně velký, může dojít k nadměrné spotřebě paměti. Může být dokonce vyvolána výjimka z důvodu nedostatku paměti.

Úpravy můžete implementovat, když běžící formát shromažďuje v paměti jedinečné identifikační kódy zákazníků a dodavatelů pro všechny daňové transakce, které budou uvedeny ve vygenerované sestavě. Protože by měly být uchovávány pouze jedinečné kódy, konečná sada kódů nebude dostatečně velká, aby ovlivnila spotřebu paměti. Sada kódů pak bude předána do mapování modelu jako argument dalšího volání zdroje dat typu *Model*. Na základě tohoto volání spustí mapování modelu nový zdroj dat ER, který vytvoří jediný požadavek SQL do databáze aplikace k načtení dat z tabulky `DirPartyTable`, a to záznamů pouze pro ty strany, jejichž kódy jsou uvedeny v poskytnuté sadě kódů.

### <a name="adjust-the-imported-data-model"></a>Úprava importovaného datového modelu

1. Přejděte do části **Správa organizace** \> **Elektronické výkaznictví** \> **Konfigurace**.
2. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně vyberte **Model Sample audit**.
3. Na záložce **Verze** vyberte verzi **2** se stavem **Koncept**.
4. Vyberte pevnou záložku **Komponenty konfigurace**.
5. Výběrem položky **Návrhář** otevřete datový model k úpravám.
6. Na stránce **Datový model** zkontrolujte, že je vybráno pole `Root` a poté vyberte **Nový**.
7. V rozevíracím dialogovém okně proveďte následující kroky:

    1. Ve skupině polí **Nový uzel jako** vyberte možnost **Podřízená položka aktivního uzlu**.
    2. Do pole **Název** zadejte **Party**.
    3. V poli **Typ položky** vyberte **Seznam záznamů**.
    4. Výběrem příkazu **Přidat** dokončíte přidání nového pole.

8. Zkontrolujte, že je vybráno pole `Root.Party` a poté na kartě **Uzel** vyberte **Parametry**.
9. V dialogovém okně **Parametry** proveďte následující kroky:

    1. Na kartě **Parametry** vyberte **Nový**.
    2. Do pole **Název** zadejte **PartyRefRecId**.
    3. V poli **Typ** vyberte **Int64**.
    4. Zaškrtněte políčko **Seznam**.
    5. Výběrem **OK** dokončete zadávání parametrů.

    > [!NOTE]
    > Právě jste nakonfigurovali pole datového modelu `Root.Party` jako pole, které je voláno, když je v poli zadána hodnota parametru **PartyRefRecId**. Tato hodnota musí být přítomna v seznamu záznamů, které obsahují pole `Value` datového typu *Int64*.

    ![Dialogové okno Parametry.](./media/er-data-model-parameterized-calls-model2a.png)

10. Ujistěte se, že je pole `Root.Party` stále vybrané, a poté znovu vyberte možnost **Nový**.
11. V rozevíracím dialogovém okně proveďte následující kroky:

    1. Ve skupině polí **Nový uzel jako** vyberte možnost **Podřízená položka aktivního uzlu**.
    2. Do pole **Název** zadejte **Name**.
    3. V poli **Typ položky** vyberte **Řetězec**.
    4. Výběrem příkazu **Přidat** dokončíte přidání nového pole.

12. Vyberte **Uložit** a poté zavřete stránku **Datový model**.

    ![Struktura upraveného datového modelu ER na stránce Návrhář datového modelu.](./media/er-data-model-parameterized-calls-model2b.png)

13. Na záložce **Verze** vyberte u verze **2** možnost **Změnit stav** \> **Dokončeno**. Pak vyberte **OK**.

    > [!NOTE]
    > Změny vašeho datového modelu jsou uloženy ve druhé revizi komponenty datového modelu **Model Sample audit**, která se nachází ve druhé verzi konfigurace ER **Model Sample audit**.

![Aktualizovaná konfigurace datového modelu ER na stránce Konfigurace.](./media/er-data-model-parameterized-calls-updated-model.png)

### <a name="adjust-the-imported-model-mapping"></a>Úprava importovaného mapování modelu

1. Na stránce **Konfigurace** ve stromu konfigurací v levém podokně rozbalte uzel **Model Sample audit**.
2. Vyberte **Mapování modelu Sample audit** a poté na záložce **Verze** vyberte druhou verzi mapování, která je založena na první verzi datového modelu (verze **1.2**), a která má stav **Koncept**.
3. Vyberte **Přeskládat**.
4. V poli **Cílová verze** ponechte verzi **2** ze základního modelu **Model Sample audit**.
5. Výběrem **OK** spustíte přeskládání a sladění mapování modelu s nedávnými změnami datového modelu.

    Všimněte si, že se číslo verze mapování upravitelného modelu změnilo z **1.2** na **2.2**, což vyjadřuje, že se v současnosti používá jako základ verze druhého modelu.

6. Vyberte možnost **Návrhář**.
7. Na stránce **Mapování modelu na zdroj dat** vyberte pro aktuální mapování modelu možnost **Návrhář**.
8. Chcete-li přidat nový zdroj dat pro přístup k aplikační tabulce `DirPartyTable`, postupujte takto:

    1. V podokně **Typ zdroje dat** vyberte **Dynamics 365 for Operations \> Tabulkové záznamy**.
    2. V podokně **Zdroje dat** vyberte **Přidat kořen**.
    3. Do pole **Název** zadejte **PartyTable**.
    4. Do pole **Tabulka** zadejte **DirPartyTable**.
    5. Výběrem **OK** dokončíte přidání nového zdroje dat.

9. Chcete-li přidat nový zdroj dat, který načte záznamy tabulky `DirPartyTable` na základě poskytnutého seznamu identifikačních kódů záznamů, postupujte takto:

    1. V podokně **Typ zdroje dat** rozbalte **Obecné \> Prázdný kontejner**.
    2. V podokně **Zdroje dat** vyberte **Přidat kořen**.
    3. Do pole **Název** zadejte **Data**.
    4. Výběrem **OK** dokončíte přidání nového zdroje dat.
    5. V podokně **Zdroje dat** vyberte zdroj dat **Data**.
    6. V podokně **Typ zdroje dat** vyberte **Funkce \> Vypočítané pole**.
    7. V podokně **Zdroje dat** vyberte **Přidat**.
    8. Do pole **Název** zadejte **DirParty**.
    9. Vyberte možnost **Upravit vzorec**.
    10. Ve stránce **Návrhář vzorců** vyberte **Parametry**.
    11. V dialogovém okně **Parametry** proveďte následující kroky:

        1. Na kartě **Parametry** vyberte **Nový**.
        2. Do pole **Název** zadejte **DirPartyId**.
        3. V poli **Typ** vyberte **Int64**.
        4. Zaškrtněte políčko **Seznam**.
        5. Vyberte **OK**.

        > [!NOTE]
        > Právě jste nakonfigurovali toto vypočítané pole tak, aby za běhu akceptovalo argument jediného parametru, který je nakonfigurován jako seznam záznamů s jedním polem `Value` typu *Int64*.

    12. V poli **Vzorec** zadejte následující výraz:

        `FILTER(PartyTable, VALUEINLARGE(PartyTable.RecId, DirPartyId, DirPartyId.Value))`

        > [!NOTE]
        > Právě jste nakonfigurovali vypočítané pole `DirParty`, které načte pouze ty záznamy tabulky `DirPartyTable`, jejichž identifikační kódy záznamu jsou zahrnuty v seznamu `DirPartyId`, který je předáván jako argument, když je voláno pole `DirParty`.

        ![Vzorec pro načtení názvů stran z aplikační tabulky na stránce Návrhář vzorců.](./media/er-data-model-parameterized-calls-formula1.png)

    13. Vyberte **Uložit** a zavřete stránku **Návrhář vzorců**.
    14. Vyberte **Uložit** a poté výběrem **OK** dokončete přidávání nového zdroje dat.

10. Chcete-li svázat nový zdroj dat s polem nového datového modelu, aby byl datový model použit ke zveřejnění názvů stran, postupujte takto:

    1. V podokně **Datový model** vyberte pole datového modelu `Root.Party`.
    2. V podokně **Datový model** vyberte **Upravit**.
    3. Na stránce **Návrhář vzorců** v poli **Vzorec** zadejte výraz `Data.DirParty(PartyRefRecId)`.
    4. Vyberte **Uložit** a zavřete stránku **Návrhář vzorců**.

        > [!NOTE]
        > Právě jste nakonfigurovali vazbu tak, aby volala konfigurovaný zdroj dat `Data.DirParty` a poskytla seznam identifikačních kódů záznamu, které budou specifikovány ve formátu, když bude voláno pole `Root.Party` datového modelu.

    5. V podokně **Datový model** vyberte pole datového modelu `Root.Party.Name`.
    6. V podokně **Datový model** vyberte **Upravit**.
    7. Na stránce **Návrhář vzorce** v podokně **Zdroj dat** rozbalte **Data \> DirParty** a vyberte položku **Name**.
    8. Vyberte **Přidat zdroj dat**.
    9. Vyberte **Uložit** a zavřete stránku **Návrhář vzorců**.

    ![Struktura upraveného mapování modelu ER na stránce Návrhář mapování modelu.](./media/er-data-model-parameterized-calls-mapping2.png)

11. Vyberte **Uložit** a zavřete stránku **Návrhář mapování modelů**.
12. Zavřete stránku **Mapování modelu na zdroj dat**.
13. Na záložce **Verze** vyberte u verze **2.2** možnost **Změnit stav \> Dokončeno**. Pak vyberte **OK**.

### <a name="adjust-the-imported-format"></a>Úprava importovaného formátu

1. Na stránce **Konfigurace** zvolte **Formát Sample audit**.
2. Na záložce **Verze** vyberte verzi **1.2** se stavem **Koncept**.
3. Vyberte **Přeskládat**.
4. V poli **Cílová verze** ponechte verzi **2** ze základního modelu **Model Sample audit**.
5. Výběrem **OK** spustíte přeskládání a sladění formátu s nedávnými změnami datového modelu.
6. Vyberte možnost **Návrhář**.
7. Na stránce **Návrhář formátu** ve stromu struktury formátu v levém podokně vyberte **Rozbalit/sbalit**.
8. Chcete-li přidat nový prvek formátu pro shromažďování identifikačních kódů záznamů stran, jejichž transakce jsou prezentovány v generovaných sestavách, postupujte takto.

    1. Ve stromu struktury formátu vyberte prvek posloupnosti **Report.Row.Trans**.
    2. Vyberte **přidat**.
    3. V dialogovém okně **Přidat** vyberte **Zdroj dat \> Položka**.
    4. V dialogovém okně **Vlastnosti komponenty** do pole **Název** zadejte **ID**.
    5. V poli **Typ dat** vyberte **Int64**.
    6. Vyberte **OK**.

    > [!NOTE]
    > Prvek **Zdroj dat \> Položka** lze použít k provádění interních výpočtů a transformaci dat pouze v rozsahu spuštěného formátu. Přidáním tohoto prvku formátu tedy nezměníte obsah generovaného dokumentu.

9. Chcete-li přidat nové prvky formátu pro zadávání názvů stran do generovaných sestav, postupujte takto:

    1. Vyberte prvek posloupnosti **Report.Row**.
    2. Vyberte **přidat**.
    3. V dialogovém okně **Přidat** vyberte **Text \> Posloupnost**.
    4. V dialogovém okně **Vlastnosti komponenty** do pole **Název** zadejte **Party**.
    5. Vyberte **OK**.
    6. Vyberte prvek posloupnosti **Report.Row.Party**.
    7. Vyberte **přidat**.
    8. V dialogovém okně **Přidat** vyberte **Text \> Řetězec**.
    9. V dialogovém okně **Vlastnosti komponenty** do pole **Název** zadejte **Name**.
    10. Vyberte **OK**.

10. Chcete-li přidat nový zdroj dat pro shromažďování identifikačních kódů záznamů stran, jejichž transakce jsou prezentovány v generovaných sestavách, postupujte takto:

    1. Na kartě **Mapování** vyberte **Přidat kořen**.
    2. V dialogovém okně **Přidat zdroj dat** vyberte **Funkce \> Sběr dat**.
    3. V dialogovém okně **Vlastnosti zdroje dat „Shromažďování dat“** v poli **Název** zadejte **PartyIds**.
    4. V poli **Typ položky** vyberte **Int64**.
    5. Vyberte **OK**.

11. Chcete-li přidat novou vazbu pro shromažďování identifikačních kódů záznamů stran, jejichž transakce jsou prezentovány v generovaných sestavách, postupujte takto:

    1. Ve stromu struktury formátu vyberte prvek položky dat **Report.Row.Trans.Id**.
    2. Vyberte možnost **Upravit vzorec**.
    3. Na stránce **Návrhář vzorce** zadejte `PartyIds.Collect(model.Transaction.Party.RecId)`.
    4. Vyberte **Uložit** a zavřete stránku **Návrhář vzorců**.

12. Chcete-li přidat nové vazby pro zadávání názvů stran do generovaných sestav, postupujte takto:

    1. Ve stromu struktury formátu vyberte prvek posloupnosti **Report.Party**.
    2. Vyberte možnost **Upravit vzorec**.
    3. Na stránce **Návrhář vzorce** zadejte `model.Party(PartyIds.Result)`.
    4. Vyberte **Uložit** a zavřete stránku **Návrhář vzorců**.
    5. Ve stromu struktury formátu vyberte prvek posloupnosti **Report.Party.Name**.
    6. Na kartě **Mapování** vyberte pole datového modelu `model.Party.Name`.
    7. Vyberte možnost **vazba**.

    ![Struktura upraveného formátu ER na stránce Návrhář formátů.](./media/er-data-model-parameterized-calls-format2.png)

13. Vyberte **Uložit** a zavřete stránku **Návrhář formátu**.
14. Zavřete stránku **Mapování modelu na zdroj dat**.
15. Na záložce **Verze** vyberte u verze **2.2** možnost **Změnit stav** \> **Dokončeno**. Pak vyberte **OK**.

### <a name="run-the-adjusted-format"></a>Spuštění upraveného formátu

1. Na stránce **Konfigurace** vyberte **Formát Sample audit** a poté v podokně akcí vyberte **Spustit**.
2. V dialogovém okně **Parametry elektronického výkaznictví** na kartě **Záznamy k zahrnutí** vyberte **Filtrovat**.
3. Zadejte podmínky pro výběr daňových transakcí dokladů **PIV-110000004** a **INV-10000001**.
4. Vyberte **OK**.
5. Vyberte **OK**.
6. Zkontrolujte vygenerovaný dokument, který obsahuje daňové transakce vybraných dokladů a jména odpovídajícího zákazníka a dodavatele.

    ![Náhled vygenerovaného dokumentu s daňovými transakcemi a názvy stran.](./media/er-data-model-parameterized-calls-output2.png)

7. Přejděte do nabídky **Závazky** \> **Dodavatelé** \> **Všichni dodavatelé** a zkontrolujte podrobnosti vybraného dokladu **PIV-110000004** včetně jména dodavatele.

    ![Kontrola podrobností nákupního dokladu na stránkách Všichni dodavatelé a Deník faktur.](./media/er-data-model-parameterized-calls-review1.gif)

8. Přejděte do nabídky **Pohledávky** \> **Zákazníci** \> **Všichni zákazníci** a zkontrolujte podrobnosti vybraného dokladu **INV-10000001** včetně jména zákazníka.

    ![Kontrola podrobností prodejního poukazu na stránkách Všichni zákazníci a Zaúčtování DPH.](./media/er-data-model-parameterized-calls-review2.gif)

Více podrobností o tomto spuštění řešení ER získáte ve vestavěném analyzátoru ER pro [sledování výkonu](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>Další prostředky

- [Podpora parametrizovaných volání zdrojů dat elektronického výkaznictví typu vypočítaného pole](er-calculated-field-type.md)
- [Sledování provedení formátů elektronického výkaznictví pro při řešení problémů s výkonem](trace-execution-er-troubleshoot-perf.md)
- [Používejte datové zdroje SHROMAŽĎOVÁNÍ DAT ve formátech elektronického hlášení](er-data-collection-data-sources.md)
- [Funkce ValueInLarge elektronického výkaznictví](er-functions-logical-valueinlarge.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

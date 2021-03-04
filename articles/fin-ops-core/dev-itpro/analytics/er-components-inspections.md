---
title: Kontrola konfigurované komponenty ER zabraňující problémům za běhu
description: Toto téma vysvětluje, jak zkontrolovat konfigurované komponenty elektronického výkaznictví (ER), aby se předešlo problémům za běhu, ke kterým může dojít.
author: NickSelin
manager: AnnBe
ms.date: 12/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72db7660c07b2f57f8609ab6c14964193e842d75
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688560"
---
# <a name="inspect-the-configured-er-component-to-prevent-runtime-issues"></a>Kontrola konfigurované komponenty ER zabraňující problémům za běhu

[!include[banner](../includes/banner.md)]

Každá konfigurovaná komponenta pro [formátování](general-electronic-reporting.md#FormatComponentOutbound) a [mapování modelu](general-electronic-reporting.md#data-model-and-model-mapping-components) [elektronického výkaznictví (ER)](general-electronic-reporting.md) může projít [ověřením platnosti](er-fillable-excel.md#validate-an-er-format) v době návrhu. Během tohoto ověřování se provádí kontrola konzistence, která pomáhá předcházet výskytu problémů za běhu, jako jsou chyby spuštění a snížení výkonu. U každého nalezeného problému je uvedena cesta k problematickému prvku. U některých problémů je k dispozici automatická oprava.

Ve výchozím nastavení se v následujících případech ověření automaticky použije u konfigurace ER, která obsahuje dříve zmíněné komponenty ER:

- [Importujte](general-electronic-reporting.md#importing-an-er-component-from-lcs-to-use-it-internally) novou [verzi](general-electronic-reporting.md#component-versioning) konfigurace ER do vaší instance Microsoftu Dynamics 365 Finance.
- Změňte [stav](general-electronic-reporting.md#component-versioning) upravitelné konfigurace ER z hodnoty **Koncept** na **Dokončeno**.
- [Přeneste změny](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) do upravitelné konfigurace ER použitím nové základní verze.

Toto ověření můžete explicitně spustit. Vyberte jednu z následujících tří možností a postupujte podle uvedených kroků:

- Možnost 1:

    1. Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.
    2. Ve stromu konfigurací v levém podokně vyberte požadovanou konfiguraci ER, která obsahuje komponentu formátu nebo mapování modelu ER.
    3. Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.
    4. V podokně Akce klikněte na možnost **Ověřit**.

- Možnost 2, pro formát ER:

    1. Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.
    2. Ve stromu konfigurací v levém podokně vyberte požadovanou konfiguraci ER, která obsahuje komponentu formátu ER.
    3. Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.
    4. V podokně akcí zvolte **Návrhář**.
    5. Na stránce **Návrhář formátu** v podokně akcí vyberte **Ověřit**.

- Možnost 3, pro mapování modelu ER:

    1. Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.
    2. Ve stromu konfigurací v levém podokně vyberte požadovanou konfiguraci ER, která obsahuje komponentu mapování modelu ER.
    3. Na pevné záložce **Verze** vyberte požadovanou verzi vybrané konfigurace ER.
    4. V podokně akcí zvolte **Návrhář**.
    5. Na stránce **Mapování modelu na zdroj dat** v podokně Akce vyberte možnost **Návrhář**.
    6. Na stránce **Návrhář mapování modelu** v podokně Akce vyberte možnost **Ověřit**.

Chcete-li přeskočit ověření při importu konfigurace, postupujte takto.

1. Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.
2. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
3. Nastavte možnost **Po importu ověřit konfiguraci** na **Ne**.

Chcete-li přeskočit ověření, když je změněn stav verze nebo základ, postupujte takto.

1. Přejděte do části **Správa organizace \> Elektronické výkaznictví \> Konfigurace**.
2. Na stránce **Konfigurace** v podokně akcí na kartě **Konfigurace** ve skupině **Pokročilá nastavení** vyberte **Parametry uživatelů**.
3. Nastavte možnost **Přeskočit ověření při změně stavu konfigurace a základu** na **Ano**.

ER používá k seskupení inspekcí kontroly konzistence následující kategorie:

- **Proveditelnost** - Inspekce, které detekují kritické problémy, ke kterým by za běhu mohlo dojít. Tyto problémy jsou většinou na úrovni **Chyba**. 
- **Výkon** - Inspekce, které detekují problémy, které by mohly způsobit neefektivní provádění konfigurovaných komponent ER. Tyto problémy jsou většinou na úrovni **Upozornění**.
- **Integrita dat** - Inspekce, které detekují problémy, které by mohly způsobit ztrátu dat nebo problémy běhového prostředí. Tyto problémy jsou většinou na úrovni **Upozornění**.

## <a name="list-of-inspections"></a>Seznam inspekcí

Následující tabulka poskytuje přehled inspekcí, které ER poskytuje. Další informace o těchto inspekcích získáte pomocí odkazů v prvním sloupci, kterými přejdete na příslušné části tohoto tématu. Tyto oddíly vysvětlují typy komponent, u kterých ER poskytuje kontroly, a návod na rekonfiguraci komponent ER, abyste zabránili problémům.

<table>
<thead>
<tr>
<th>Jméno</th>
<th>Kategorie</th>
<th>Úroveň</th>
<th>Zpráva</th>
</tr>
</thead>
<tbody>
<tr>
<td><a href='#i1'>Převod typu</a></td>
<td>Proveditelnost</td>
<td>Chyba</td>
<td>
<p>Nelze převést výraz typu &lt;typ&gt; na pole typu &lt;typ&gt;.</p>
<p><b>Chyba za běhu:</b> Výjimka typu</p>
</td>
</tr>
<tr>
<td><a href='#i2'>Kompatibilita typů</a></td>
<td>Proveditelnost</td>
<td>Chyba</td>
<td>
<p>Konfigurovaný výraz nelze použít jako vazbu aktuálního prvku formátu ke zdroji dat, protože tento výraz vrací hodnotu datového typu &lt;typ&gt;, tedy mimo rámec datových typů, které jsou podporovány aktuálním prvkem formátu typu &lt;typ&gt;.</p>
<p><b>Chyba za běhu:</b> Výjimka typu</p>
</td>
</tr>
<tr>
<td><a href='#i3'>Chybějící konfigurační prvek</a></td>
<td>Proveditelnost</td>
<td>Chyba</td>
<td>
<p>Cesta nenalezena: &lt;cesta&gt;.</p>
<p><b>Chyba za běhu:</b> Prvek konfigurace &lt; cesta&gt; nenalezen</p>
</td>
</tr>
<tr>
<td><a href='#i4'>Spustitelnost výrazu s funkcí FILTER</a></td>
<td>Proveditelnost</td>
<td>Chyba</td>
<td>
<p>Výraz seznamu funkce FILTER není dotazovatelný.</p>
<p><b>Chyba za běhu:</b> Filtrování není podporováno. Chcete-li získat další podrobnosti o chybě, ověřte konfiguraci.</p>
</td>
</tr>
<tr>
<td rowspan='2'><a href='#i5'>Spustitelnost zdroje dat GROUPBY</a></td>
<td>Proveditelnost</td>
<td>Chyba</td>
<td>Cesta &lt;cesta&gt; nepodporuje dotazování.</td>
</tr>
<tr>
<td>Proveditelnost</td>
<td>Chyba</td>
<td>
<p>Seskupení podle funkce nelze provést pomocí dotazu.</p>
<p><b>Chyba za běhu:</b> Seskupení podle funkce nelze provést pomocí dotazu.</p>
</td>
</tr>
<tr>
<td><a href='#i6'>Spustitelnost zdroje dat JOIN</a></td>
<td>Proveditelnost</td>
<td>Chyba</td>
<td>
<p>Nelze připojit seznam &lt;cesta&gt;, který není filtrem v dotazu.</p>
<p><b>Chyba za běhu:</b> Funkce datového zdroje JOIN by měla být výrazem filtru vypočítaného pole, který byl nesprávně volán.</p>
</td>
</tr>
<tr>
<td><a href='#i7'>Je vhodnější funkce FILTER nebo WHERE?</a></td>
<td>Výkonnost</td>
<td>Upozornění</td>
<td>Použití funkce FILTER ve výrazu je z hlediska výkonu vhodnější než použití funkce WHERE. Vyberte možnost Opravit, aby došlo k automatickému nahrazení.</td>
</tr>
<tr>
<td><a href='#i8'>Je vhodnější funkce ALLITEMSQUERY nebo ALLITEMS?</a></td>
<td>Výkonnost</td>
<td>Upozornění</td>
<td>Použití funkce ALLITEMSQUERY ve výrazu je z hlediska výkonu vhodnější než použití funkce ALLITEMS. Vyberte možnost Opravit, aby došlo k automatickému nahrazení.</td>
</tr>
<tr>
<td><a href='#i9'>Možnost výskytů prázdného seznamu</a></td>
<td>Proveditelnost</td>
<td>Upozornění</td>
<td>
<p>Seznam &lt;cesta&gt; nemá žádnou kontrolu výskytu prázdného seznamu, což může způsobit chybu za běhu. Přidejte kontrolu výskytu prázdného seznamu.</p>
<p><b>Chyba za běhu:</b> Seznam je prázdný v cestě &lt;cesta&gt;</p>
<p><b><a href='#i9a'>Potenciální problém</a> :</b> Řádek se naplní jednou, zatímco zdroj dat, ze kterého je naplněn, obsahuje více záznamů</p>
</td>
</tr>
<tr>
<td><a href='#i10'>Spustitelnost výrazu s funkcí FILTER (použití mezipaměti)</a></td>
<td>Proveditelnost</td>
<td>Chyba</td>
<td>
<p>Funkci FILTER nelze použít na vybraný typ zdroje dat. Zdroj dat typu Záznamy tabulky je použitelný pouze v případě, že není uložen do mezipaměti a nemá žádné ručně přidané vnořené zdroje dat.</p>
<p><b>Chyba za běhu:</b> Filtrování není podporováno. Chcete-li získat další podrobnosti o chybě, ověřte konfiguraci.</p>
</td>
</tr>
<tr>
<td><a href='#i11'>Chybějící vazba</a></td>
<td>Proveditelnost</td>
<td>Upozornění</td>
<td>
<p>Cesta &lt;cesta&gt; nemá žádnou vazbu na žádný zdroj dat při používání mapování modelu.</p>
<p><b>Chyba za běhu:</b> Cesta &lt;cesta&gt; není vázána</p>
</td>
</tr>
<tr>
<td><a href='#i12'>Nepropojená šablona</a></td>
<td>Integrita dat</td>
<td>Upozornění</td>
<td>Soubor &lt;název&gt; není propojen s žádnými souborovými komponentami a bude odstraněn po změně stavu verze konfigurace.</td>
</tr>
<tr>
<td><a href='#i13'>Nesynchronizovaný formát</a></td>
<td>Integrita dat</td>
<td>Upozornění</td>
<td>Definovaný název &lt;název komponenty&gt; neexistuje v listu aplikace Excel &lt;název listu&gt;</td>
</tr>
</tbody>
</table>

## <a name="type-conversion"></a><a id="i1"></a>Převod typu

ER kontroluje, zda je datový typ pole datového modelu kompatibilní s datovým typem výrazu, který je konfigurován jako vazba daného pole. Pokud jsou datové typy nekompatibilní, dojde v návrháři mapování modelu ER k chybě ověření. Zpráva, kterou obdržíte, uvádí, že ER nemůže převést výraz typu A na pole typu B.

Následující kroky ukazují, jak může k tomuto problému dojít.

1. Začněte konfigurovat datový model ER a komponenty mapování modelu ER současně.
2. Ve stromu datového modelu přidejte pole s názvem **X** a jako datový typ vyberte **Celé číslo**.

    ![Pole X a datový typ Celé číslo byly přidány do stromu datového modelu na stránce Datový model](./media/er-components-inspections-01.png)

3. V podokně zdrojů dat mapování modelu přidejte zdroj dat typu **Vypočítané pole**.
4. Pojmenujte nový zdroj dat jako **Y** a konfigurujte jej tak, aby obsahoval výraz `INTVALUE(100)`.
5. Navažte **X** na **Y**.
6. V návrháři datového modelu změňte datový typ pole **X** z hodnoty **Celé číslo** na **Int64**.
7. Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu mapování modelu na stránce **Návrhář mapování modelu**.

    ![ověřování upravitelné komponenty mapování modelu na stránce Návrhář mapování modelu](./media/er-components-inspections-01.gif)

8. Výběrem příkazu **Ověřit** zkontrolujete komponentu mapování modelu vybrané konfigurace ER na stránce **Konfigurace**.

    ![Ověření komponenty mapování modelu na stránce Konfigurace](./media/er-components-inspections-01a.png)

9. Všimněte si, že dojde k chybě ověření. Zpráva uvádí, že hodnotu typu **Celé číslo**, kterou vrátí výraz `INTVALUE(100)` zdroje dat **Y**, nelze uložit do pole datového modelu **X** typu **Int64**.

Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát, který má konfigurováno použití mapování modelu.

![Chyby za běhu na stránce Návrhář formátu](./media/er-components-inspections-01b.png)

### <a name="automatic-resolution"></a>Automatické řešení

Není k dispozici žádná možnost automatického řešení tohoto problému.

### <a name="manual-resolution"></a>Ruční řešení

#### <a name="option-1"></a>Možnost 1

Aktualizujte strukturu datového modelu změnou datového typu pole datového modelu tak, aby odpovídal datovému typu výrazu, který je konfigurován pro vazbu daného pole. V předchozím příkladu musíte datový typ pole **X** změnit zpět na **Celé číslo**.

#### <a name="option-2"></a>Možnost 2

Aktualizujte mapování modelu změnou výrazu zdroje dat, který je svázán s polem datového modelu. V předchozím příkladu musíte změnit výraz zdroje dat **Y** na `INT64VALUE(100)`.

## <a name="type-compatibility"></a><a id="i2"></a>Kompatibilita typů

ER kontroluje, zda je datový typ prvku formátu kompatibilní s datovým typem výrazu, který je konfigurován jako vazba daného prvku formátu. Pokud jsou datové typy nekompatibilní, dojde v návrháři operací ER k chybě ověření. Zpráva, kterou obdržíte, říká, že konfigurovaný výraz nelze použít jako vazbu aktuálního prvku formátu ke zdroji dat, protože tento výraz vrací hodnotu datového typu A, tedy mimo rámec datových typů, které jsou podporovány aktuálním prvkem formátu typu B.

Následující kroky ukazují, jak může k tomuto problému dojít.

1. Začněte konfigurovat datový model ER a komponenty formátu ER současně.
2. Ve stromu datového modelu přidejte pole s názvem **X** a jako datový typ vyberte **Celé číslo**.
3. Ve stromu struktury formátu přidejte prvek formátu typu **Číslo**.
4. Pojmenujte nový prvek formátu jako **Y**. V poli **Číselný typ** vyberte jako datový typ hodnotu **Celé číslo**.
5. Navažte **X** na **Y**.
6. Ve stromu struktury formátu změňte datový typ prvku formátu **Y** z hodnoty **Celé číslo** na **Int64**.
7. Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu formátu na stránce **Návrhář formátu**.

    ![Ověření kompatibility typů na stránce Návrhář formátu](./media/er-components-inspections-02.gif)

8. Všimněte si, že dojde k chybě ověření. Zpráva uvádí, že konfigurovaný výraz může přijmout pouze hodnoty typu **Int64**. Proto nelze hodnotu pole datového modelu **X** typu **Celé číslo** zadat do prvku formátu **Y**.

### <a name="automatic-resolution"></a>Automatické řešení

Není k dispozici žádná možnost automatického řešení tohoto problému.

### <a name="manual-resolution"></a>Ruční řešení

#### <a name="option-1"></a>Možnost 1

Aktualizujte strukturu formátu změnou datového typu prvku formátu **Číslo** tak, aby odpovídal datovému typu výrazu, který je konfigurován pro vazbu tohoto prvku. V předchozím příkladu musíte datový typ **Číslo** prvku formátu **X** změnit zpět **Celé číslo**.

#### <a name="option-2"></a>Možnost 2

Aktualizujte mapování formátu prvku formátu **X** změnou výrazu z `model.X` na `INT64VALUE(model.X)`.

## <a name="missing-configuration-element"></a><a id="i3"></a>Chybějící konfigurační prvek

ER zkontroluje, zda vazební výrazy obsahují pouze zdroje dat, které jsou konfigurovány v upravitelné komponentě ER. U každé vazby, která obsahuje zdroj dat, který chybí v upravitelné komponentě ER, dojde k chybě ověření v návrháři operací ER nebo návrháři mapování modelu ER.

Následující kroky ukazují, jak může k tomuto problému dojít.

1. Začněte konfigurovat datový model ER a komponenty mapování modelu ER současně.
2. Ve stromu datového modelu přidejte pole s názvem **X** a jako datový typ vyberte **Celé číslo**.

    ![Strom datového modelu s polem X a datovým typem Celé číslo na stránce Datový model](./media/er-components-inspections-01.png)

3. V podokně zdrojů dat mapování modelu přidejte zdroj dat typu **Vypočítané pole**.
4. Pojmenujte nový zdroj dat jako **Y** a konfigurujte jej tak, aby obsahoval výraz `INTVALUE(100)`.
5. Navažte **X** na **Y**.
6. V návrháři mapování modelu v podokně zdroje dat odstraňte zdroj dat **Y**.
7. Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu mapování modelu na stránce **Návrhář mapování modelu**.

    ![kontrola upravitelné komponenty mapování modelu ER na stránce Návrhář mapování modelu](./media/er-components-inspections-03.gif)

8. Všimněte si, že dojde k chybě ověření. Zpráva uvádí, že vazba pole datového modelu **X** obsahuje cestu, která odkazuje na zdroj dat **Y**, ale tento zdroj dat nebyl nalezen.

### <a name="automatic-resolution"></a>Automatické řešení

Výběrem příkazu **Odpojit** automaticky opravíte tento problém odstraněním vazby na chybějící zdroj dat.

### <a name="manual-resolution"></a>Ruční řešení

#### <a name="option-1"></a>Možnost 1

Odpojte pole datového modelu **X**, aby přestalo odkazovat na neexistující zdroj dat **Y**.

#### <a name="option-2"></a>Možnost 2

V podokně zdrojů dat návrháře mapování modelu ER přidejte znovu zdroj dat **Y**.

## <a name="executability-of-an-expression-with-filter-function"></a><a id="i4"></a>Spustitelnost výrazu s funkcí FILTER

Integrovaná funkce ER [FILTER](er-functions-list-filter.md) se používá pro přístup k aplikačním tabulkám, pohledům nebo datovým entitám umístěním jediného volání SQL, které získá požadovaná data jako seznam záznamů. Zdroj dat typu **Seznam záznamů** se používá jako argument této funkce a určuje zdroj aplikace pro volání. ER kontroluje, zda lze navázat přímý dotaz SQL do zdroje dat, na který se odkazuje ve funkci `FILTER`. Pokud nelze navázat přímý dotaz, dojde v návrháři mapování modelu ER k chybě ověření. Zpráva, kterou obdržíte, uvádí, že výraz ER obsahující funkci `FILTER` nelze spustit za běhu programu. 

Následující kroky ukazují, jak může k tomuto problému dojít.

1. Začněte konfigurací komponenty mapování modelu ER.
2. Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.
3. Pojmenujte nový zdroj dat jako **Vendor**. V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.
4. Přidejte zdroj dat typu **Vypočítané pole**.
5. Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Vendor, Vendor.AccountNum="US-101")`.
6. Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** stránku a ověřte, zda výraz `FILTER(Vendor, Vendor.AccountNum="US-101")` ve zdroji dat **Vendor** lze používat v dotazech.
7. Upravte zdroj dat **Vendor** přidáním vnořeného pole typu **Vypočítané pole** a získejte oříznuté číslo účtu dodavatele.
8. Pojmenujte nové vnořené pole jako **$AccNumber** a konfigurujte jej tak, aby obsahovalo výraz `TRIM(Vendor.AccountNum)`.
9. Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** stránku a ověřte, zda výraz `FILTER(Vendor, Vendor.AccountNum="US-101")` ve zdroji dat **Vendor** lze používat v dotazech.

    ![Ověření výrazu lze zkontrolovat dotazem na stránce Návrhář mapování modelů](./media/er-components-inspections-04.gif)

10. Všimněte si, že dojde k chybě ověření, protože zdroj dat **Vendor** obsahuje vnořené pole typu **Vypočítané pole**, které neumožňuje přeložit výraz **FilteredVendor** zdroje dat na přímý příkaz SQL.

Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát, který má konfigurováno použití mapování modelu.

![Chyby za běhu, ke kterým dochází při spuštění upravitelného formátu na stránce Návrhář formátů](./media/er-components-inspections-04a.png)

### <a name="automatic-resolution"></a>Automatické řešení

Není k dispozici žádná možnost automatického řešení tohoto problému.

### <a name="manual-resolution"></a>Ruční řešení

#### <a name="option-1"></a>Možnost 1

Místo přidání vnořeného pole typu **Vypočítané pole** do zdroje dat **Vendor** přidejte vnořené pole **$AccNumber** do zdroje dat **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `TRIM(FilteredVendor.AccountNum)`. Tímto způsobem lze výraz `FILTER(Vendor, Vendor.AccountNum="US-101")` spustit na úrovni SQL a vypočítat vnořené pole **$AccNumber** později.

#### <a name="option-2"></a>Možnost 2

Změňte výraz zdroje dat **FilteredVendor** z `FILTER(Vendor, Vendor.AccountNum="US-101")` na `WHERE(Vendor, Vendor.AccountNum="US-101")`. Nedoporučujeme měnit výraz pro tabulku, která obsahuje velké množství dat (transakční tabulka), protože budou načteny všechny záznamy a výběr požadovaných záznamů bude proveden v paměti. Tento přístup proto může způsobit špatný výkon. Další informace viz část [Funkce WHERE ER](er-functions-list-where.md).

## <a name="executability-of-a-groupby-data-source"></a><a id="i5"></a>Spustitelnost zdroje dat GROUPBY

Zdroj dat **GROUPBY** rozděluje výsledek dotazu do skupin záznamů, obvykle za účelem provedení jedné nebo více agregací v každé skupině. Každý zdroj dat **GROUPBY** lze konfigurovat tak, aby běžel na úrovni databáze nebo v paměti. Když je zdroj dat **GROUPBY** konfigurován tak, aby byl spuštěn na úrovni databáze, ER zkontroluje, zda lze navázat přímý dotaz SQL do zdroje dat, na který se tento zdroj dat odkazuje. Pokud nelze navázat přímý dotaz, dojde v návrháři mapování modelu ER k chybě ověření. Zpráva, kterou obdržíte, uvádí, že konfigurovaný zdroj dat **GROUPBY** nelze spustit za běhu.

Následující kroky ukazují, jak může k tomuto problému dojít.

1. Začněte konfigurací komponenty mapování modelu ER.
2. Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.
3. Pojmenujte nový zdroj dat jako **Trans**. V poli **Tabulka** vyberte hodnotu **VendTrans** a určete tak, že tento zdroj dat bude vyžadovat tabulku VendTrans.
4. Přidejte zdroj dat typu **Seskupit podle**.
5. Pojmenujte nový zdroj dat jako **GroupedTrans** a konfigurujte jej následujícím způsobem:

    - Vyberte zdroj dat **Trans** jako zdroj záznamů, které by měly být seskupeny.
    - V poli **Místo provedení** vyberte **Dotaz** a určete tak, že chcete spustit tento zdroj dat na úrovni databáze.

    ![Konfigurace zdroje dat na stránce Upravit parametry „Seskupit podle“](./media/er-components-inspections-05a.gif)

6. Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** a ověřte, zda je možné konfigurovaný zdroj dat **GroupedTrans** používat v dotazech.
7. Upravte zdroj dat **Trans** přidáním vnořeného pole typu **Vypočítané pole** a získejte oříznuté číslo účtu dodavatele.
8. Pojmenujte nový zdroj dat jako **$AccNumber** a konfigurujte jej tak, aby obsahoval výraz `TRIM(Trans.AccountNum)`.

    ![Konfigurace zdroje dat na stránce návrháře mapování modelů](./media/er-components-inspections-05a.png)

9. Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** a ověřte, zda je možné konfigurovaný zdroj dat **GroupedTrans** používat v dotazech.

    ![Po ověření komponenty mapování modelu ER a ověření konfigurovaného zdroje dat je možné zdroj dat GroupedTrans používat v dotazech na stránce návrháře mapování modelů](./media/er-components-inspections-05b.png)

10. Všimněte si, že dojde k chybě ověření, protože zdroj dat **Trans** obsahuje vnořené pole typu **Vypočítané pole**, které neumožňuje přeložit volání určené pro zdroj dat **GroupedTrans** na přímý příkaz SQL.

Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát, který má konfigurováno použití mapování modelu.

![Chyby za běhu, ke kterým dochází při ignorování upozornění na stránce Návrhář formátů](./media/er-components-inspections-05c.png)

### <a name="automatic-resolution"></a>Automatické řešení

Není k dispozici žádná možnost automatického řešení tohoto problému.

### <a name="manual-resolution"></a>Ruční řešení

#### <a name="option-1"></a>Možnost 1

Místo přidání vnořeného pole typu **Vypočítané pole** zadejte do zdroje dat **Trans** přidejte vnořené pole **$AccNumber** pro položku **GroupedTrans.lines** zdroje dat **GroupedTrans** a konfigurujte jej tak, aby obsahovalo výraz `TRIM(GroupedTrans.lines.AccountNum)`. Tímto způsobem lze zdroj dat **GroupedTrans** spustit na úrovni SQL a vypočítat vnořené pole **$AccNumber** později.

#### <a name="option-2"></a>Možnost 2

Změňte hodnotu pole **Místo provedení** pro zdroj dat **GroupedTrans** z hodnoty **Dotaz** na **V paměti**. Nedoporučujeme měnit hodnotu pro tabulku, která obsahuje velké množství dat (transakční tabulka), protože budou načteny všechny záznamy a seskupení spolu s agregací budou provedeny v paměti. Tento přístup proto může způsobit špatný výkon.

## <a name="executability-of-a-join-data-source"></a><a id="i6"></a>Spustitelnost zdroje dat JOIN

Zdroj dat [JOIN](er-join-data-sources.md) kombinuje záznamy ze dvou nebo více databázových tabulek na základě souvisejících polí. Každý zdroj dat **JOIN** lze konfigurovat tak, aby běžel na úrovni databáze nebo v paměti. Když je zdroj dat **JOIN** konfigurován tak, aby byl spuštěn na úrovni databáze, ER zkontroluje, zda lze navázat přímý dotaz SQL do zdrojů dat, na které se tento zdroj dat odkazuje. Pokud nelze navázat přímý dotaz SQL s nejméně jedním odkazovaným zdrojem dat, dojde v návrháři mapování modelu ER k chybě ověření. Zpráva, kterou obdržíte, uvádí, že konfigurovaný zdroj dat **JOIN** nelze spustit za běhu.

Následující kroky ukazují, jak může k tomuto problému dojít.

1. Začněte konfigurací komponenty mapování modelu ER.
2. Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.
3. Pojmenujte nový zdroj dat jako **Vendor**. V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.
4. Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.
5. Pojmenujte nový zdroj dat jako **Trans**. V poli **Tabulka** vyberte hodnotu **VendTrans** a určete tak, že tento zdroj dat bude vyžadovat tabulku VendTrans.
6. Přidejte zdroj dat typu **Vypočítané pole** jako vnořené pole zdroje dat **Vendor**.
7. Pojmenujte nový zdroj dat jako **FilteredTrans** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`.
8. Přidejte zdroj dat typu **Spojit**.
9. Pojmenujte nový zdroj dat jako **JoinedList** a konfigurujte jej následujícím způsobem:

    1. Přidejte zdroj dat **Vendor** jako první sadu záznamů, která bude spojena.
    2. Přidejte zdroj dat **Vendor.FilteredTrans** jako druhou sadu záznamů, která bude spojena. Vyberte typ spojení **INNER**.
    3. V poli **Provést** vyberte **Dotaz** a určete tak, že chcete spustit tento zdroj dat na úrovni databáze.

    ![Konfigurace zdroje dat na stránce návrháře spojení](./media/er-components-inspections-06a.gif)

10. Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** a ověřte, zda je možné konfigurovaný zdroj dat **JoinedList** používat v dotazech.
11. Změňte výraz zdroje dat **Vendor.FilteredTrans** z `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)` na `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)`.
12. Výběrem příkazu **Ověřit** zkontrolujte upravitelnou komponentu mapování modelu na stránce **návrháře mapování modelů** a ověřte, zda je možné konfigurovaný zdroj dat **JoinedList** používat v dotazech.

    ![Výběrem příkazu Ověřit zkontrolujte upravitelnou komponentu mapování modelu a ověřte že je možné konfigurovaný zdroj dat JoinedList používat v dotazech na stránce návrháře mapování modelu](./media/er-components-inspections-06b.png)

13. Všimněte si, že dojde k chybě ověření, protože výraz zdroje dat **Vendor.FilteredTrans** nelze přeložit na přímé volání SQL. Přímé volání SQL navíc neumožňuje volání zdroje dat **JoinedList**, které má být přeloženo do přímého příkazu SQL.

    ![Chyby za běhu z neúspěšného ověření zdroje dat JoinedList na stránce návrháře mapování modelů](./media/er-components-inspections-06c.png)

Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát, který má konfigurováno použití mapování modelu.

![Spuštění upravitelného formátu na stránce Návrhář formátů](./media/er-components-inspections-06e.png)

### <a name="automatic-resolution"></a>Automatické řešení

Není k dispozici žádná možnost automatického řešení tohoto problému.

### <a name="manual-resolution"></a>Ruční řešení

#### <a name="option-1"></a>Možnost 1

Změňte výraz zdroje dat **Vendor.FilteredTrans** z `WHERE(Trans, Trans.AccountNum=Vendor.AccountNum)` zpět na `FILTER(Trans, Trans.AccountNum=Vendor.AccountNum)`, jak doporučovalo zobrazené upozornění.

![Aktualizovaný výraz zdroje dat na stránce návrháře mapování modelů](./media/er-components-inspections-06d.png)

#### <a name="option-2"></a>Možnost 2

Změňte hodnotu pole **Provést** pro zdroj dat **JoinedList** z hodnoty **Dotaz** na **V paměti**. Nedoporučujeme měnit hodnotu v tabulce, která obsahuje velké množství dat (transakční tabulka), protože budou načteny všechny záznamy a seskupení bude provedeno v paměti. Tento přístup proto může způsobit špatný výkon. Zobrazí se upozornění ověření, které vás bude informovat o tomto riziku.

## <a name="preferability-of-filter-vs-where-function"></a><a id="i7"></a>Je vhodnější funkce FILTER nebo WHERE?

Integrovaná funkce ER [FILTER](er-functions-list-filter.md) se používá pro přístup k aplikačním tabulkám, pohledům nebo datovým entitám umístěním jediného volání SQL, které získá požadovaná data jako seznam záznamů. Funkce [WHERE](er-functions-list-where.md) načte všechny záznamy z daného zdroje a provede výběr záznamů v paměti. Zdroj dat typu **Seznam záznamů** se používá jako argument obou funkcí a určuje zdroj pro načtení záznamů. ER kontroluje, zda lze navázat přímé volání SQL do zdroje dat, na který se odkazuje ve funkci **WHERE**. Pokud nelze navázat přímé volání, je v návrháři mapování modelu ER vyvoláno upozornění ověření. Zpráva, kterou obdržíte, doporučuje použít funkci **FILTER** namísto **WHERE**, která pomůže zlepšit efektivitu.

Následující kroky ukazují, jak může k tomuto problému dojít.

1. Začněte konfigurací komponenty mapování modelu ER.
2. Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.
3. Pojmenujte nový zdroj dat jako **Trans**. V poli **Tabulka** vyberte hodnotu **VendTrans** a určete tak, že tento zdroj dat bude vyžadovat tabulku VendTrans.
4. Přidejte zdroj dat typu **Vypočítané pole** jako vnořené pole zdroje dat **Vendor**.
5. Pojmenujte nový zdroj dat jako **FilteredTrans** a konfigurujte jej tak, aby obsahoval výraz `WHERE(Trans, Trans.AccountNum="US-101")`.
6. Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.
7. Pojmenujte nový zdroj dat jako **Vendor**. V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.
8. Přidejte zdroj dat typu **Vypočítané pole**.
9. Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `WHERE(Vendor, Vendor.AccountNum="US-101")`.
10. Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu mapování modelu na stránce **Návrhář mapování modelu**.

    ![Výběrem příkazu Ověřit zkontrolujete upravitelnou komponentu mapování modelu na stránce návrháře mapování modelu](./media/er-components-inspections-07a.png)

11. Všimněte si, že upozornění ověření doporučují používat funkci **FILTER** namísto funkce **WHERE** u zdrojů dat **FilteredVendor** a **FilteredTrans**.

    ![Upozornění ověření doporučující funkci FILTER namísto funkce WHERE na stránce návrháře mapování modelů](./media/er-components-inspections-07b.png)

### <a name="automatic-resolution"></a>Automatické řešení

Výběrem příkazu **Opravit** automaticky nahradíte funkci **WHERE** funkcí **FILTER** ve výrazu všech zdrojů dat, které se objevují v mřížce na kartě **Upozornění** pro tento typ kontroly.

Alternativně můžete vybrat řádek pro jedno upozornění v mřížce a poté vybrat příkaz **Opravit vybrané**. V tomto případě se výraz automaticky změní pouze ve zdroji dat, který je uveden ve vybraném upozornění.

![Výběrem možnosti Opravit automaticky nahradíte funkci WHERE funkcí FILTER na stránce návrháře mapování modelů](./media/er-components-inspections-07c.png)

### <a name="manual-resolution"></a>Ruční řešení

Výrazy všech zdrojů dat, které jsou uvedeny v ověřovací mřížce, můžete ručně upravit nahrazením funkce **WHERE** za funkci **FILTER**.

## <a name="preferability-of-allitemsquery-vs-allitems-function"></a><a id="i8"></a>Je vhodnější funkce ALLITEMSQUERY nebo ALLITEMS?

Integrované funkce ER [ALLITEMS](er-functions-list-allitems.md) a [ALLITEMSQUERY](er-functions-list-allitemsquery.md) se používají k získání ploché hodnoty **seznamu záznamů**, která se skládá ze seznamu záznamů, které představují všechny položky odpovídající zadané cestě. ER kontroluje, zda lze navázat přímé volání SQL do zdroje dat, na který se odkazuje ve funkci **ALLITEMS**. Pokud nelze navázat přímé volání, je v návrháři mapování modelu ER vyvoláno upozornění ověření. Zpráva, kterou obdržíte, doporučuje použít funkci **ALLITEMSQUERY** namísto **ALLITEMS**, která pomůže zlepšit efektivitu.

Následující kroky ukazují, jak může k tomuto problému dojít.

1. Začněte konfigurací komponenty mapování modelu ER.
2. Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.
3. Pojmenujte nový zdroj dat jako **Vendor**. V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.
4. K získání záznamů za několik dodavatelů přidejte zdroj dat typu **Vypočítané pole**.
5. Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Vendor, OR(Vendor.AccountNum="US-101",Vendor.AccountNum="US-102"))`.
6. K získání transakcí všech vyfiltrovaných dodavatelů přidejte zdroj dat typu **Vypočítané pole**.
7. Pojmenujte nový zdroj dat jako **FilteredVendorTrans** a konfigurujte jej tak, aby obsahoval výraz `ALLITEMS(FilteredVendor.'<Relations'.'VendTrans.VendTable_AccountNum')`.
8. Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu mapování modelu na stránce **Návrhář mapování modelu**.

    ![Stránka návrháře mapování modelů, tlačítko Ověřit](./media/er-components-inspections-08a.png)

9. Všimněte si, že se zobrazí upozornění ověření. Zpráva doporučuje použít funkci **ALLITEMSQUERY** namísto funkce **ALLITEMS** pro zdroj dat **FilteredVendorTrans**.

    ![Upozornění ověření s radou použít funkci ALLITEMSQUERY namísto funkce ALLITEMS v komponentě mapování modelu ER na stránce návrháře mapování modelů](./media/er-components-inspections-08b.png)

### <a name="automatic-resolution"></a>Automatické řešení

Výběrem příkazu **Opravit** automaticky nahradíte funkci **ALLITEMS** funkcí **ALLITEMSQUERY** ve výrazu všech zdrojů dat, které se objevují v mřížce na kartě **Upozornění** pro tento typ kontroly.

Alternativně můžete vybrat řádek pro jedno upozornění v mřížce a poté vybrat příkaz **Opravit vybrané**. V tomto případě se výraz automaticky změní pouze ve zdroji dat, který je uveden ve vybraném upozornění.

![Na stránce návrháře mapování modelů vyberte příkaz Opravit vybrané](./media/er-components-inspections-08c.png)

### <a name="manual-resolution"></a>Ruční řešení

Výrazy všech zdrojů dat, které jsou uvedeny v ověřovací mřížce, můžete ručně upravit nahrazením funkce **ALLITEMS** za funkci **ALLITEMSQUERY**.

## <a name="consideration-of-empty-list-cases"></a><a id="i9"></a>Možnost výskytů prázdného seznamu

Komponentu formátu nebo mapování modelu ER můžete konfigurovat tak, abyste získali hodnotu pole zdroje dat typu **Seznam záznamů**. ER zkontroluje, zda váš návrh zohledňuje případ, kdy zdroj dat, který je volán, neobsahuje žádné záznamy (tedy je prázdný), aby se předešlo chybám za běhu při načtení hodnoty z pole neexistujícího záznamu.

Následující kroky ukazují, jak může k tomuto problému dojít.

1. Začněte konfigurovat datový model ER, mapování modelu ER a komponenty formátu ER současně.
2. Ve stromu datového modelu přidejte kořenovou položku s názvem **Root3**.
3. Upravte položku **Root3** přidáním vnořené položky typu **Seznam záznamů**.
4. Pojmenujte novou vnořenou položku jako **Vendor**.
5. Upravte položku **Vendor** následujícím způsobem:

    - Přidejte vnořené pole typu **Řetězec** a pojmenujte jej jako **Name**.
    - Přidejte vnořené pole typu **Řetězec** a pojmenujte jej jako **AccountNumber**.

    ![Přidání vnořených polí na stránce Datový model](./media/er-components-inspections-09a.png)

6. V podokně zdrojů dat mapování modelu přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.
7. Pojmenujte nový zdroj dat jako **Vendor**. V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.
8. Přidejte zdroj dat typu **Všeobecné \\ Uživatelský vstupní parametr** pro vyhledání účtu dodavatele v dialogovém okně modulu runtime.
9. Pojmenujte nový zdroj dat jako **RequestedAccountNum**. Do pole **Popisek** zadejte **Číslo účtu dodavatele**. V poli **Název datového typu Operations** ponechte výchozí hodnotu **Popis**.
10. K vyfiltrování dodavatele, o kterého se zajímáte, přidejte zdroj dat typu **Vypočítané pole**.
11. Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
12. Vytvořte vazbu položek datového modelu na konfigurované zdroje dat následujícím způsobem:

    - Vytvořte vazbu položky **FilteredVendor** na položku **Vendor**.
    - Vytvořte vazbu položky **FilteredVendor.AccountNum** na položku **Vendor.AccountNumber**.
    - Vytvořte vazbu položky **FilteredVendor.'name()'** na položku **Vendor.Name**.

    ![Vázání položek datového modelu na stránce návrháře mapování modelů](./media/er-components-inspections-09b.png)

13. Ve stromu struktury formátu přidejte následující položky, které generují odchozí dokument ve formátu XML obsahující podrobnosti o dodavateli:

    1. Přidejte kořenový prvek XML **Statement**.
    2. U prvku XML **Statement** přidejte vnořený prvek XML **Party**.
    3. U prvku XML **Party** přidejte následující vnořené atributy XML:

        - Jméno
        - AccountNum

14. Navažte prvky formátu na poskytnuté zdroje dat následujícím způsobem:

    - Vytvořte vazbu prvku formátu **Statement\\Party\\Name** na pole zdroje dat **model.Vendor.Name**.
    - Vytvořte vazbu prvku formátu **Statement\\Party\\AccountNum** na pole zdroje dat **model.Vendor.AccountNumber**.

15. Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu formátu na stránce **Návrhář formátu**.

    ![Ověření prvků formátu navázaných na zdroje dat na stránce Návrhář formátů](./media/er-components-inspections-09c.png)

16. Všimněte si, že dojde k chybám ověření. Zpráva uvádí, že chyba může být za běhu vyvolána u konfigurovaných komponent formátu **Statement\\Party\\Name** a **Statement\\Party\\AccountNum**, pokud je seznam **model.Vendor** prázdný.

    ![Chyba ověření, která upozorňuje na potenciální chybu u konfigurovaných komponent formátu](./media/er-components-inspections-09d.png)

Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění, vyberete příkaz **Spustit** a zvolíte číslo účtu neexistujícího dodavatele. Protože požadovaný dodavatel neexistuje, seznam **model.Vendor** bude prázdný (to znamená, že nebude obsahovat žádné záznamy).

![Chyby za běhu, ke kterým došlo za běhu mapování formátu](./media/er-components-inspections-09e.png)

### <a name="automatic-resolution"></a>Automatické řešení

Pro vybraný řádek v mřížce na kartě **Upozornění** můžete vybrat příkaz **Zrušit vazbu**. Vazba, na kterou se ukazuje ve sloupci **Cesta**, je automaticky odebrána z prvků formátu.

### <a name="manual-resolution"></a>Ruční řešení

#### <a name="option-1"></a>Možnost 1

Můžete navázat prvek formátu **Statement\\Party\\Name** na položku zdroje dat **model.Vendor**. Za běhu tato vazba volá nejprve zdroj dat **model.Vendor**. Když **model.Vendor** vrátí prázdný seznam záznamů, vnořené prvky formátu se nespustí. Proto u této konfigurace formátu nejsou vyvolána žádná upozornění ověření.

![Vazba prvku formátu na položku zdroje dat na stránce Návrhář formátů](./media/er-components-inspections-09e.gif)

#### <a name="option-2"></a>Možnost 2

Změňte vazbu prvku formátu **Statement\\Party\\Name** z `model.Vendor.Name` na `FIRSTORNULL(model.Vendor).Name`. Aktualizovaná vazba podmíněně převede první záznam zdroje dat **model.Vendor** typu **Seznam záznamů** na nový zdroj dat typu **Záznam**. Tento nový zdroj dat obsahuje stejnou sadu polí.

- Pokud je ve zdroji dat **model.Vendor** k dispozici alespoň jeden záznam, pole tohoto záznamu jsou vyplněna hodnotami polí prvního záznamu zdroje dat **model.Vendor**. V takovém případě aktualizovaná vazba vrátí název dodavatele.
- V opačném případě je každé pole vytvořeného záznamu vyplněno výchozí hodnotou pro datový typ daného pole. V tomto případě je vrácen prázdný řetězec jako výchozí hodnota datového typu **Řetězec**.

Proto se pro prvek formátu **Statement\\Party\\Name** nevyskytují žádná upozornění ověření, když je vázán na výraz `FIRSTORNULL(model.Vendor).Name`.

![Změněná vazba řeší upozornění ověření na stránce Návrhář formátů](./media/er-components-inspections-09f.gif)

#### <a name="option-3"></a>Možnost 3

Pokud chcete explicitně určit data, která se zadávají do generovaného dokumentu, když zdroj dat **model.Vendor** typu **Seznam záznamů** nevrátí žádné záznamy (v tomto příkladu text **Not available**), změňte vazbu prvku formátu **Statement\\Party\\Name** z hodnoty `model.Vendor.Name` na `IF(NOT(ISEMPTY(model.Vendor)), model.Vendor.Name, "Not available")`. Můžete také použít výraz `IF(COUNT(model.Vendor)=0, model.Vendor.Name, "Not available")`.

### <a name="additional-consideration"></a><a id="i9a"></a>Další faktor ke zvážení

Inspekce vás také upozorňuje na další možný problém. Ve výchozím nastavení při vazbě prvků formátu **Statement\\Party\\Name** a **Statement\\Party\\AccountNum** na příslušná pole zdroje dat **model.Vendor** typu **Seznam záznamů** budou tyto vazby spuštěny a načtou hodnoty odpovídajících polí prvního záznamu zdroje dat **model.Vendor**, pokud tento seznam není prázdný.

Protože jste nevytvořili vazbu prvku formátu **Statement\\Party** se zdrojem dat **model.Vendor**, prvek **Statement\\Party** nebude během provádění formátu iterován pro každý záznam zdroje dat **model.Vendor**. Místo toho bude vygenerovaný dokument vyplněn informacemi pouze z prvního záznamu seznamu záznamů, pokud tento seznam obsahuje více záznamů. Proto může nastat problém, pokud je formát určen k vyplnění generovaného dokumentu informacemi o všech dodavatelích ze zdroje dat **model.Vendor**. Chcete-li tento problém napravit, vytvořte vazbu prvku **Statement\\Party** se zdrojem dat **model.Vendor**.

## <a name="executability-of-an-expression-with-filter-function-caching"></a><a id="i10"></a>Spustitelnost výrazu s funkcí FILTER (použití mezipaměti)

Některé Integrované funkce ER, včetně [FILTER](er-functions-list-filter.md) a [ALLITEMSQUERY](er-functions-list-allitemsquery.md), se používají pro přístup k aplikačním tabulkám, pohledům nebo datovým entitám umístěním jediného volání SQL, které získá požadovaná data jako seznam záznamů. Zdroj dat typu **Seznam záznamů** se používá jako argument každé z těchto funkcí a určuje zdroj aplikace pro volání. ER kontroluje, zda lze navázat přímé volání SQL do zdroje dat, na který se odkazuje v jedné z těchto funkcí. Pokud nelze navázat přímé volání, protože zdroj dat byl označen jako [ukládaný do mezipaměti](trace-execution-er-troubleshoot-perf.md#improve-the-model-mapping-based-on-information-from-the-execution-trace), dojde v návrháři mapování modelu ER k chybě ověření. Zpráva, kterou obdržíte, uvádí, že výraz ER obsahující jednu z těchto funkcí nelze spustit za běhu programu.

Následující kroky ukazují, jak může k tomuto problému dojít.

1. Začněte konfigurací komponenty mapování modelu ER.
2. Přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.
3. Pojmenujte nový zdroj dat jako **Vendor**. V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.
4. Přidejte zdroj dat typu **Všeobecné \\ Uživatelský vstupní parametr** pro vyhledání účtu dodavatele v dialogovém okně modulu runtime.
5. Pojmenujte nový zdroj dat jako **RequestedAccountNum**. Do pole **Popisek** zadejte **Číslo účtu dodavatele**. V poli **Název datového typu Operations** ponechte výchozí hodnotu **Popis**.
6. K vyfiltrování dodavatele, o kterého se zajímáte, přidejte zdroj dat typu **Vypočítané pole**.
7. Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
8. Označte konfigurovaný zdroj dat **Vendor** jako ukládaný v mezipaměti.

    ![Konfigurace komponenty mapování modelu na stránce Návrhář mapování modelu](./media/er-components-inspections-10a.gif)

9. Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu mapování modelu na stránce **Návrhář mapování modelu**.

    ![Ověření funkce FILTER použité na zdroj dat dodavatele ukládaný do mezipaměti na stránce návrháře mapování modelů](./media/er-components-inspections-10a.png)

10. Všimněte si, že dojde k chybě ověření. Zpráva uvádí, že funkci **FILTER** nelze použít na zdroj dat **Vendor**, který je ukládán do mezipaměti.

Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát.

![Chyba za běhu, ke které dojde během provádění mapování formátu na stránce Návrhář formátů](./media/er-components-inspections-10b.png)

### <a name="automatic-resolution"></a>Automatické řešení

Není k dispozici žádná možnost automatického řešení tohoto problému.

### <a name="manual-resolution"></a>Ruční řešení

#### <a name="option-1"></a>Možnost 1

Odstraňte příznak **Mezipaměť** ze zdroje dat **Vendor**. Zdroj dat **FilteredVendor** zdroj dat se poté stane spustitelným, ale zdroj dat **Vendor**, na který se odkazuje v tabulce VendTable, bude přístupný pokaždé, když je volán zdroj dat **FilteredVendor**.

#### <a name="option-2"></a>Možnost 2

Změňte výraz zdroje dat **FilteredVendor** z `FILTER(Vendor, Vendor.AccountNum="US-101")` na `WHERE(Vendor, Vendor.AccountNum="US-101")`. V tomto případě bude ke zdroji dat **Vendor**, na který se odkazuje v tabulce VendTable, přistupováno pouze během prvního volání zdroje dat **Vendor**. Výběr záznamů se však provede v paměti. Tento přístup proto může způsobit špatný výkon.

## <a name="missing-binding"></a><a id="i11"></a>Chybějící vazba

Když konfigurujete komponentu formátu ER, nabídne se základní datový model ER jako výchozí zdroj dat pro formát ER. Když je spuštěn konfigurovaný formát ER, použije se k vyplnění datového modelu aplikačními daty [výchozí mapování modelu](er-country-dependent-model-mapping.md) pro základní model. Návrhář formátu ER zobrazí upozornění, pokud vytvoříte vazbu prvku formátu na položku datového modelu, která není vázána na žádný zdroj dat v tom mapování modelu, který je aktuálně vybrán jako výchozí mapování modelu pro upravitelný formát. Tento typ vazby nelze spustit za běhu, protože spuštěný formát nemůže vyplnit vázaný prvek daty aplikace. Proto za běhu dojde k chybě.

Následující kroky ukazují, jak může k tomuto problému dojít.

1. Začněte konfigurovat datový model ER, mapování modelu ER a komponenty formátu ER současně.
2. Ve stromu datového modelu přidejte kořenovou položku s názvem **Root3**.
3. Upravte položku **Root3** a přidejte do ní novou vnořenou položku typu **Seznam záznamů**.
4. Pojmenujte novou vnořenou položku jako **Vendor**.
5. Upravte položku **Vendor** následujícím způsobem:

    - Přidejte vnořené pole typu **Řetězec** a pojmenujte jej jako **Name**.
    - Přidejte vnořené pole typu **Řetězec** a pojmenujte jej jako **AccountNumber**.

    ![Přidání vnořených polí k položce dodavatele na stránce Datový model](./media/er-components-inspections-11a.png)

6. V podokně zdrojů dat mapování modelu přidejte zdroj dat typu **Záznamy tabulky \\ Dynamics 365 for Operations**.
7. Pojmenujte nový zdroj dat jako **Vendor**. V poli **Tabulka** vyberte **VendTable** a určete tak, že tento zdroj dat bude požadovat tabulku VendTable.
8. Přidejte zdroj dat typu **Všeobecné \\ Uživatelský vstupní parametr** pro získání informací o účtu dodavatele v dialogovém okně modulu runtime.
9 Pojmenujte nový zdroj dat jako **RequestedAccountNum**. Do pole **Popisek** zadejte **Číslo účtu dodavatele**. V poli **Název datového typu Operations** ponechte výchozí hodnotu **Popis**.
10. K vyfiltrování dodavatele, o kterého se zajímáte, přidejte zdroj dat typu **Vypočítané pole**.
11. Pojmenujte nový zdroj dat jako **FilteredVendor** a konfigurujte jej tak, aby obsahoval výraz `FILTER(Vendor, Vendor.AccountNum=RequestedAccountNum)`.
12. Vytvořte vazbu položek datového modelu na konfigurované zdroje dat následujícím způsobem:

    - Vytvořte vazbu položky **FilteredVendor** na položku **Vendor**.
    - Vytvořte vazbu položky **FilteredVendor.AccountNum** na položku **Vendor.AccountNumber**.

    > [!NOTE]
    > Pole datového modelu **Vendor.Name** zůstává nevázané.

    ![Položky datového modelu vázané na konfigurované zdroje dat a položka datového režimu na stránce Návrháře mapování modelů](./media/er-components-inspections-11b.png)

13. Ve stromu struktury formátu přidejte následující položky, které generují odchozí dokument ve formátu XML obsahující podrobnosti o dodavatelích, kteří vás zajímají:

    1. Přidejte kořenový prvek XML **Statement**.
    2. U prvku XML **Statement** přidejte vnořený prvek XML **Party**.
    3. U prvku XML **Party** přidejte následující vnořené atributy XML:

        - Jméno
        - AccountNum

14. Navažte prvky formátu na poskytnuté zdroje dat následujícím způsobem:

    - Vytvořte vazbu prvku formátu **Statement\\Party** na položku zdroje dat **model.Vendor**.
    - Vytvořte vazbu prvku formátu **Statement\\Party\\Name** na pole zdroje dat **model.Vendor.Name**.
    - Vytvořte vazbu prvku formátu **Statement\\Party\\AccountNum** na pole zdroje dat **model.Vendor.AccountNumber**.

15. Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu formátu na stránce **Návrhář formátu**.

    ![Ověření komponenty formátu ER na stránce Návrhář formátů](./media/er-components-inspections-11c.png)

16. Všimněte si, že se zobrazí upozornění ověření. Zpráva uvádí, že pole zdroje dat **model.Vendor.Name** není vázáno na žádný zdroj dat v mapování modelu, který je konfigurován pro použití ve formátu. Proto prvek formátu **Statement\\Party\\Name** nemusí být za běhu vyplněn a může dojít k výjimce za běhu.

    ![Ověření komponenty formátu ER na stránce Návrhář formátů](./media/er-components-inspections-11d.png)

Následující obrázek ukazuje chybu za běhu, která nastane, pokud ignorujete upozornění a výběrem příkazu **Spustit** spustíte formát.

![Spuštění upravitelného formátu na stránce Návrhář formátů](./media/er-components-inspections-11e.png)

### <a name="automatic-resolution"></a>Automatické řešení

Není k dispozici žádná možnost automatického řešení tohoto problému.

### <a name="manual-resolution"></a>Ruční řešení

#### <a name="option-1"></a>Možnost 1

Upravte konfigurované mapování modelu přidáním vazby pro pole zdroje dat **model.Vendor.Name**.

#### <a name="option-2"></a>Možnost 2

Upravte konfigurovaný formát odebráním vazby pro prvek formátu **Statement\\Party\\Name**.

## <a name="not-linked-template"></a><a id="i12"></a>Nepropojená šablona

Když [ručně](er-fillable-excel.md#manual-entry) nakonfigurujete komponentu formátu ER tak, aby pomocí šablony generovala odchozí dokument, musíte ručně přidat prvek **Excel\\File**, přidat požadovanou šablonu jako přílohu upravitelné komponenty, a vybrat tuto přílohu v přidaném prvku **Excel\\File**. Tímto způsobem dáváte najevo, že přidaný prvek za běhu vyplní vybranou šablonu. Při konfiguraci verze komponenty formátu ve [stavu](general-electronic-reporting.md#component-versioning) **Návrh** můžete do upravitelné komponenty přidat několik šablon a poté vybrat každou šablonu v prvku **Excel\\File**, aby spustila formát ER. Tímto způsobem můžete vidět, jak jsou různé šablony vyplněny za běhu. Pokud máte šablony, které nejsou vybrány v žádném prvku **Excel\\File**, návrhář formátu ER vás upozorní, že tyto šablony budou odstraněny z upravitelné verze komponenty formátu ER, když se jeho stav změní z **Návrh** na **Dokončeno**.

Následující kroky ukazují, jak může k tomuto problému dojít.

1. Začněte konfigurací komponenty formátu ER.
2. Ve stromu struktury formátu přidejte prvek **Excel\\File**.
3. U prvku **Excel\\File**, který jste právě přidali, přidejte soubor sešitu aplikace Excel **A.xlsx** jako přílohu. Použijte typ dokumentu, který je konfigurován v [parametrech ER](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) k určení úložiště šablon formátu ER.
4. U prvku **Excel\\File**, který jste právě přidali, přidejte další soubor sešitu aplikace Excel **B.xlsx** jako přílohu. Použijte stejný typ dokumentu jako u souboru sešitu A.
5. V prvku **Excel\\File** vyberte soubor sešitu A.
6. Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu formátu na stránce **Návrhář formátu**.

    ![Ověření komponenty upravitelného formátu souboru sešitu na stránce Návrhář formátů](./media/er-components-inspections-12a.gif)

7. Všimněte si, že se zobrazí upozornění ověření. Zpráva uvádí, že soubor sešitu **B.xlsx** není propojen se žádnými komponentami a že bude odstraněn po změně stavu verze konfigurace.

### <a name="automatic-resolution"></a>Automatické řešení

Není k dispozici žádná možnost automatického řešení tohoto problému.

### <a name="manual-resolution"></a>Ruční řešení

Upravte konfigurovaný formát odebráním všech šablon, které nejsou propojeny s žádným prvkem **Excel\\File**.

## <a name="not-synced-format"></a><a id="i13"></a>Nesynchronizovaný formát

Když [nakonfigurujete](er-fillable-excel.md) komponentu formátu ER tak, aby pomocí šablony Excelu generovala odchozí dokument, můžete ručně přidat prvek **Excel\\File**, přidat požadovanou šablonu jako přílohu upravitelné komponenty, a vybrat tuto přílohu v přidaném prvku **Excel\\File**. Tímto způsobem dáváte najevo, že přidaný prvek za běhu vyplní vybranou šablonu. Protože přidaná šablona Excelu byla navržena externě, může upravitelný formát ER obsahovat názvy aplikace Excel, které v přidané šabloně chybí. Návrhář formátu ER vás upozorní na jakékoli nesrovnalosti mezi vlastnostmi prvků formátu ER odkazující na názvy, které nejsou zahrnuty v přidané šabloně Excelu.

Následující kroky ukazují, jak může k tomuto problému dojít.

1. Začněte konfigurací komponenty formátu ER.
2. Ve stromu struktury formátu přidejte prvek **Excel\\File** s názvem **Report**.
3. U prvku **Excel\\File**, který jste právě přidali, přidejte soubor sešitu aplikace Excel **A.xlsx** jako přílohu. Použijte typ dokumentu, který je konfigurován v [parametrech ER](electronic-reporting-er-configure-parameters.md#parameters-to-manage-documents) k určení úložiště šablon formátu ER.

    > [!IMPORTANT]
    > Ujistěte se, že přidaný sešit Excelu neobsahuje název **ReportTitle**.

4. Přidejte následující prvek **Excel\\Cell** s názvem **Title** jako vnořený prvek prvku **Report**. Do pole **Oblast Excelu** zadejte **ReportTitle**.
5. Výběrem příkazu **Ověřit** zkontrolujete upravitelnou komponentu formátu na stránce **Návrhář formátu**.

    ![Ověření vnořených prvků a polí na stránce Návrhář formátu](./media/er-components-inspections-13a.png)

6. Všimněte si, že se zobrazí upozornění ověření. Zpráva uvádí, že název **ReportTitle** neexistuje v listu **Sheet1** šablony aplikace Excel, kterou používáte.

    ![Upozornění ověření na fakt, že název ReportTitle neexistuje na listu Sheet1 šablony aplikace Excel](./media/er-components-inspections-13b.png)

### <a name="automatic-resolution"></a>Automatické řešení

Není k dispozici žádná možnost automatického řešení tohoto problému.

### <a name="manual-resolution"></a>Ruční řešení

#### <a name="option-1"></a>Možnost 1

Upravte konfigurovaný formát odebráním všech prvků odkazujících na názvy aplikace Excel, které v šabloně chybí.

#### <a name="option-2"></a>Možnost 2

[Aktualizujte](er-fillable-excel.md#template-import) upravitelný formát ER importem šablony aplikace Excel. Struktura upravitelného formátu ER bude [synchronizována](modify-electronic-reporting-format-reapply-excel-template.md) se strukturou importované šablony Excelu.

### <a name="additional-consideration"></a>Další faktor ke zvážení

Chcete-li se naučit synchronizovat strukturu formátu se šablonou ER v editoru šablon [Správy obchodních dokumentů](er-business-document-management.md), přečtěte si část [Aktualizace struktury šablony obchodního dokumentu](er-bdm-update-structure.md).

## <a name="additional-resources"></a>Další prostředky

[Funkce elektronického výkaznictví ALLITEMS](er-functions-list-allitems.md)

[Funkce elektronického výkaznictví ALLITEMSQUERY](er-functions-list-allitemsquery.md)

[Funkce el. výkaznictví INT64VALUE](er-functions-conversion-int64value.md)

[Funkce INTVALUE ER](er-functions-conversion-intvalue.md)

[Funkce elektronického výkaznictví FILTER](er-functions-list-filter.md)

[Funkce elektronického výkaznictví WHERE](er-functions-list-where.md)

[Použití zdrojů dat JOIN v mapování modelu ER k získání dat z více aplikačních tabulek](er-join-data-sources.md)

[Sledování provedení formátů elektronického výkaznictví pro při řešení problémů s výkonem](trace-execution-er-troubleshoot-perf.md)

[Přehled správy obchodních dokumentů](er-business-document-management.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
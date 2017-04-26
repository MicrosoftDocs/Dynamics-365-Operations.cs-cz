---
title: "Přehled převodů SEPA"
description: "Tento článek poskytuje obecné informace o ISO 20022 bezhotovostní platby, které zahrnují převody jednoho eura platby oblasti (SEPA) a ostatních elektronických plateb pro dodavatele. SEPA převod je určitý typ platby v eurech z jedné společnosti nebo jiné společnosti individuální nebo individuální. V tématu vysvětluje, jak nastavit a předá soubor platební převod platby."
author: twheeloc
manager: AnnBe
ms.date: 2017-03-16
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 848df5e3898f37284d7746c59bff8b38d35ac883
ms.lasthandoff: 03/31/2017


---

# <a name="sepa-credit-transfer-overview"></a>Přehled převodů SEPA

Tento článek poskytuje obecné informace o ISO 20022 bezhotovostní platby, které zahrnují převody jednoho eura platby oblasti (SEPA) a ostatních elektronických plateb pro dodavatele. SEPA převod je určitý typ platby v eurech z jedné společnosti nebo jiné společnosti individuální nebo individuální. V tématu vysvětluje, jak nastavit a předá soubor platební převod platby.

## <a name="what-is-a-credit-transfer-message"></a>Co je přenos zprávy Dal?
Zpráva přenosu Dal je požadavek, který odešle převádět finanční prostředky z vlastního účtu věřiteli zahajující ze stran (společnost). Existuje celá řada implementací specifické pro zemi/oblast a konkrétní bankovní převod zpráv. Některé z nich se používají v rámci jedné země a některé se stávají standardy. Jeden dobře zavedené globální standard je ISO 20022 a jeho zahájení, jako jsou například bezhotovostních plateb. Následující obrázek znázorňuje vztahy a pokrytí pro vybrané platební převod zpráv. 
![Přenesení Dal](./media/credit-transfer.jpg) Dal přenos zprávy\[/titulek\] 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Co jsou ISO 20022 a SEPA platby?
Jednotná oblast pro platby v eurech (SEPA) je definována Evropskou komisí a určuje, že všechny elektronické platby jsou považovány za domácí bez ohledu na zemi nebo oblast, kde se osoba, podnik, nebo organizace a banka nachází. Není žádný rozdíl mezi vnitrostátní platby a přeshraničních plateb. SEPA obsahuje 28 členských států Evropské unie (EU) a také Island, Lichtenštejnsko, Norsko, Švýcarsko, Monako a San Marino. SEPA umožňuje vytvořit jednotný trh pro platební transakce v Evropském hospodářském prostoru (EHP). Použitím SEPA se očekává snížit počet formátů plateb, se kterými banky, společnosti a jednotlivci musí pracovat. Evropská komise ustanovila právní základ pro platby SEPA prostřednictvím směrnice týkající se platebních služeb (PSD). Evropská rada pro platby (EPC) podporuje platby SEPA prostřednictvím následujících činností:

-   Stanovuje normy pro elektronické platby SEPA s použitím formátu ISO 20022 – Univerzální schéma zpráv ve finančnictví XML.
-   Stanovuje pravidla a pokyny pro zpracování plateb v eurech.

EPC, která zahrnuje evropské banky, vyvíjí obchodní a technické předlohy pro nástroje plateb SEPA. Používají se tři typy plateb SEPA:

-   Bezhotovostní převody
-   Příkazy k inkasu
-   Karty

## <a name="what-is-a-sepa-credit-transfer"></a>Co je bezhotovostní převod SEPA?
Převod SEPA je platba od jedné společnosti nebo osoby pro jinou společnost nebo osobu. Platby musí být v eurech a musí obsahovat mezinárodní číslo bankovního účtu (IBAN) a identifikační kód BIC (Bank Identifier Code) pro obě strany. (BIC je známá také jako Society for Worldwide Interbank Financial Telecommunication \[SWIFT\] kód.) Kromě toho náklady na transakce musí být sdílena mezi oběma stranami. Převody prováděné mezi stranami by měly používat soubory XML, které vyhovují normám zpracování plateb ISO 20022 a formátu XML, jak uvádí EPC.

## <a name="how-is-a-credit-transfer-implemented"></a>Jak je implementována bezhotovostních plateb
Formát platby platební převod pro Evropské země je implementováno pomocí elektronických sestav (ER) a způsoby platby funkce Dynamics 365 pro operace. Několik Dal přenosové formáty, které jsou použity v jiných oblastech i nadále používat starší platby framework. Mezi mnoha jinými formáty jsou dvanáct ISO 20022 platební převod formátů souborů, které jsou k dispozici. Tyto formáty pro export standardům SEPA ISO 20022 XML. Používají se ke generování non-euro platebních převodů pro země, kde se používají a euro platby podle verze 8.2 Rulebook schéma přenosu SEPA Dal, který se vydává EPC. Předtím, než můžete provádět bezhotovostní platby, obraťte se na vaše banka získat software, který je vyžadován při odesílání souborů pro elektronické bankovnictví. Budete používat tento software pro přenos souborů XML, které obsahují platebních příkazů do banky.

## <a name="what-credit-transfer-formats-are-currently-supported-in-dynamics-365-for-operations"></a>Jaké formáty převodu úvěru jsou aktuálně podporovány v 365 Dynamics pro operace?
Vždy má přejít do majetku knihovny sdílené v Microsoft Dynamics Lifecycle services (LCS) a zobrazit aktuální seznam dostupných souborů, které mají typ majetku **konfigurace pravidel**. Další oddíl "Co musím nastavit?", obsahuje odkaz na téma, které vysvětluje, jak vytvořit úložiště LCS zkontrolovat dostupné konfigurace a importovat vybrané konfigurace.

## <a name="what-do-i-have-to-set-up"></a>Co je nutné nastavit?
-   Před převodem je možné vytvořit soubory, alespoň jednu konfiguraci aktivní platební převod třeba importovat do konfigurace ER. Pokyny naleznete v tématu [stáhnout elektronické vykazování konfigurace služby životního cyklu](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
-   Při konfiguraci účtů závazků způsoby platby vyberte **obecný elektronických sestav** zaškrtněte políčko a vyberte formát přenosu odpovídající úvěrové (například **ISO 20022 bezhotovostní (AT)**) jako informace o nastavení formátu exportu.
-   Musíte také nastavit právní entity a bankovní účet informace v 365 Dynamics pro operace.
-   Čísla bankovních účtů, IBANs a někdy SWIFT kódů (BICs) nebo jiné ID, které jsou potřebné k vytvoření platného bezhotovostní platby. Proto musíte vytvořit je pro bankovní účet dodavatele a bankovní účet pro organizaci, která žádá o převod.
-   Další informace může být vyžadován, například daň z přidané hodnoty (DPH) pro smluvní strany, které jsou podle zprávy převod úvěru. Tyto informace musí být nastavit pro dodavatele a pro právnickou osobu při požadavku.
-   Některé účty splatné platební metody, převážně na základě ISO 20022 metody platby, mohou vyžadovat další nastavení pro **sady kódů formátu platby**, jako **služba typu** = **SLEV**. Tyto kódy se používají jako další označení pro platební transakce během zpracování platby. Jako výchozí hodnoty kódů platebních **účel kategorie**, **poplatek doručitele**, **místní přístroj** a **úrovni služby** můžete nastavit na dvou místech. Na prvním místě je **účty záhlaví deníku plateb závazků** a druhý je **účty závazků metody platby pro**. Po vytvoření řádků deníku plateb platební kód hodnoty nastavené v záhlaví deníku plateb jsou převedeny do řádku deníku, není-li nastaven, budou použity hodnoty z metody platby.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Jaké parametry jsou k dispozici pro generování plateb platební převod?
Seznam specifických parametrů závisí na formátu platební převod. Následující tabulka uvádí parametry, které jsou k dispozici při generování souboru ISO 20022 Dal převodu platby pro Německo do deníku plateb dodavatele. Pomocí možnosti, které jsou k dispozici na **běží na pozadí** na kartě generování plateb lze spustit v dávkovém režimu.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Pole</th>
<th>popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Dávková rezervace</td>
<td>Zaškrtnutím tohoto políčka můžete zahrnout do souboru XML značku dávkové rezervace.</td>
</tr>
<tr class="even">
<td>Datum zpracování</td>
<td>Zadejte datum, kdy má banka platby zpracovat.</td>
</tr>
<tr class="odd">
<td>Formát</td>
<td>Vyberte formát informací o úhradě v závislosti na požadavcích vaší země/regionu nebo banky:
<ul>
<li><strong>Strd</strong> – vyberte tuto možnost, chcete-li použít strukturovaném formátu, když jeden řádek platby je vyrovnána vůči jedné faktury. Tato možnost není k dispozici pro formáty exportu specifické pro zemi/oblast pro Francii, Německo a Nizozemsko.</li>
<li><strong>Nestrukt.</strong> – Tuto možnost vyberte, chcete-li použít nestrukturovaný formát, když je platba vyrovnána proti několika fakturám. Čísla faktur pro vyrovnání faktur jsou zřetězeny a použity jako informace o úhradě. V souladu s ISO 20022 pokyny, úhrady nestrukturované informace jsou omezeny na 140znaků $2.</li>
</ul></td>
</tr>
<tr class="even">
<td>Počet faktur</td>
<td>Zadejte číslo faktury tento <strong>avízo platby</strong> ze se vytiskne sestava.</td>
</tr>
<tr class="odd">
<td>Pořadové číslo</td>
<td>Zadejte pořadové číslo pro identifikaci souboru. Pořadové číslo se zobrazí na <strong>průvodka</strong> sestavy.</td>
</tr>
<tr class="even">
<td>Tisk průvodky</td>
<td>Zaškrtnutím tohoto políčka můžete vytisknout sestavu <strong>Průvodka</strong>.</td>
</tr>
<tr class="odd">
<td>Vytisknout kontrolní sestavu</td>
<td>Zaškrtnutím tohoto políčka můžete vytisknout sestavu, která obsahuje informace o platbě.</td>
</tr>
<tr class="even">
<td>Vytisknout průvodní dopis</td>
<td>Chcete-li vytisknout sestavu <strong>Avízo platby</strong>, zaškrtněte toto políčko.</td>
</tr>
</tbody>
</table>

## <a name="what-are-ibans-and-bics"></a>Co jsou kódy IBAN a BIC?
Mezinárodní číslo bankovního účtu (IBAN) a bankovní identifikátor kód (BIC) slouží k identifikaci libovolného účtu v mnoha zemích po celém světě. Patří sem 34 SEPA zemí. Zadejte IKB v **kód SWIFT** pole a kód IBAN v **IBAN** pole. Pro věřitele bankovního účtu a bankovní účet zákazníka, tato pole se nacházejí na **další identifikační** s náhledem na **bankovního účtu** karty **bankovní účty** stránky. Již je vynuceno použití BIC pro SEPA platby.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Jak mohu přenést soubor platby do banky?
Při generování plateb platební dokumentace je generována a budete vyzváni k uložení z webového prohlížeče na libovolné místo k dispozici. Dalším krokem je soubor XML odeslat do banky. Tento proces se v jednotlivých bankách liší. Postupujte podle pokynů vaší banky k odeslání souborů do banky ke zpracování.



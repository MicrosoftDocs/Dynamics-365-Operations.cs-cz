---
title: Přehled převodů SEPA
description: Toto téma poskytuje obecné informace o převodech kreditů ISO 20022, které zahrnují převody kreditů v jednotné oblasti pro platby v eurech a jakékoli další elektronické platby pro dodavatele.
author: sunfzam
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.reviewer: twheeloc
ms.custom:
- "11124"
- intro-internal
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f43c45aa4f22f5044e7c10329dafa76226970b3d
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/10/2022
ms.locfileid: "8734509"
---
# <a name="sepa-credit-transfer-overview"></a>Přehled převodů SEPA

[!include [banner](../includes/banner.md)]

Toto téma poskytuje obecné informace o převodech kreditů ISO 20022, které zahrnují převody kreditů v jednotné oblasti pro platby v eurech a jakékoli další elektronické platby pro dodavatele. Převod SEPA je specifický typ platby v eurech od jedné společnosti nebo osoby pro jinou společnost nebo osobu. Toto téma také vysvětluje, jak nastavit a převést soubor platby platebního převodu.

## <a name="what-is-a-credit-transfer-message"></a>Co je zpráva o bezhotovostním převodu?
Zpráva o převodu kreditu je požadavek, který odešle iniciující strana (vaše společnost) pro převod financí z vlastního účtu věřiteli. Existuje celá řada implementací specifických pro zemi/oblast a konkrétní implementace zpráv o převodu kreditu. Některé z nich se používají v rámci jedné země nebo oblasti a některé se stávají standardem. Jeden dobře zavedený globální standard je ISO 20022 a jeho iniciační zprávy, jako je například převod kreditu. Následující obrázek znázorňuje vztahy a pokrytí pro vybrané zprávy o převodu kreditu. 
![Peněžní převod](./media/credit-transfer.jpg) Zprávy o peněžním převodu 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Co jsou platby ISO 20022 a SEPA?
Jednotná oblast pro platby v eurech (SEPA) je definována Evropskou komisí a určuje, že všechny elektronické platby jsou považovány za domácí bez ohledu na zemi nebo oblast, kde se osoba, podnik, nebo organizace a banka nachází. Neexistuje žádný rozdíl mezi národní a zahraniční platbou. SEPA zahrnuje 28 členských států Evropské unie (EU) plus Island, Lichtenštejnsko, Norsko, Švýcarsko, Monako a San Marino. SEPA umožňuje vytvořit jednotný trh pro platební transakce v Evropském hospodářském prostoru (EHP). Použitím SEPA se očekává snížit počet formátů plateb, se kterými banky, společnosti a jednotlivci musí pracovat. Evropská komise ustanovila právní základ pro platby SEPA prostřednictvím směrnice týkající se platebních služeb (PSD). Evropská rada pro platby (EPC) podporuje platby SEPA prostřednictvím následujících činností:

-   Stanovuje normy pro elektronické platby SEPA s použitím formátu ISO 20022 – Univerzální schéma zpráv ve finančnictví XML.
-   Stanovuje pravidla a pokyny pro zpracování plateb v eurech.

EPC, která zahrnuje evropské banky, vyvíjí obchodní a technické předlohy pro nástroje plateb SEPA. Používají se tři typy plateb SEPA:

-   Bezhotovostní převody
-   Příkazy k inkasu
-   Karty

## <a name="what-is-a-sepa-credit-transfer"></a>Co je bezhotovostní převod SEPA?
Převod SEPA je platba od jedné společnosti nebo osoby pro jinou společnost nebo osobu. Platby musí být v eurech a musí obsahovat mezinárodní číslo bankovního účtu (IBAN) a identifikační kód BIC (Bank Identifier Code) pro obě strany. (BIC je známý také jako kód Society for Worldwide Interbank Financial Telecommunication \[SWIFT\].) Kromě toho musí být náklady na transakce sdíleny mezi oběma stranami. Převody prováděné mezi stranami by měly používat soubory XML, které vyhovují normám zpracování plateb ISO 20022 a formátu XML, jak uvádí EPC.

## <a name="how-is-a-credit-transfer-implemented"></a>Jak je převod kreditu implementován?
Formát platby platebního převodu pro evropské země je implementován pomocí funkce elektronického výkaznictví a metod plateb v aplikaci Microsoft Dynamics 365 Finance. Několik formátů převodu kreditu, které se používají v jiných regionech, již používá systém zastaralé platby. Mezi mnoha jinými formáty je dvanáct formátů převodu kreditu ISO 20022, které jsou k dispozici. Tyto formáty pro export odpovídají standardu SEPA ISO 20022 XML. Používají se ke generování platebních převodů jiného typu než euro pro země, kde se používají, a pro euro se používají platby podle určení ve verzi 8.2 pravidel přenosu, které vydává EPC. Než bude možné implementovat převody kreditu, obraťte se na vaši banku za účelem získání softwaru, který je nutný k načtení souborů elektronického bankovnictví. Tento software budete používat pro přenos souborů XML obsahujících platební příkazy do banky.

## <a name="what-credit-transfer-formats-are-currently-supported"></a>Jaké formáty převodu kreditu jsou aktuálně podporovány?
Měli byste vždy přejít do knihovny sdílený majetek ve službě Microsoft Dynamics Lifecycle services (LCS) a zobrazit nejaktuálnější seznam dostupných souborů, které mají typ majetku **konfigurace GER**. Další oddíl "Co musím nastavit?" obsahuje odkaz na téma, které vysvětluje, jak vytvořit úložiště LCS ke kontrole dostupných konfigurací a importovat vybrané konfigurace.

## <a name="what-do-i-have-to-set-up"></a>Co je nutné nastavit?
-   Před vytvořením souborů převodu kreditu je třeba alespoň jednu aktivní konfigurace převodu importovat do vaší konfigurace obecného elektronického výkaznictví. Pokyny viz [Stažení konfigurace elektronického vykazování ze služby Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
-   Při konfiguraci metody platby Závazky zaškrtněte políčko **Obecné elektronické výkaznictví** a vyberte vhodný formát převodu kreditu (například **Převod kreditu ISO 20022 (AT)**) jako konfiguraci formátu exportu.
-   Musíte nastavit také informace o právnické osobě a bankovním účtu.
-   Čísla bankovních účtů, IBAN a někdy SWIFT kódy (BIC) nebo jiné ID, která jsou potřebná k vytvoření platné bezhotovostní platby. Proto je musíte nastavit pro bankovní účet dodavatele a bankovní účet pro organizaci, která žádá o převod.
-   Další informace mohou být vyžadovány, například daň z přidané hodnoty (DPH) pro smluvní strany, které jsou odkazovány ve zprávě o převodu úvěru. Tyto informace musí být nastaveny pro dodavatele a pro právnickou osobu na vyžádání.
-   Některé způsoby platby splatných účtů, většinou metody na základě ISO 20022, mohou vyžadovat další nastavení pro **sady kódů formátu plateb**, jako je **Typ služby** = **SLEV**. Tyto kódy se používají jako další označení pro platební transakce během zpracování platby. Výchozí hodnoty kódů plateb jako **účel kategorie**, **poplatek doručitele**, **místní instrument** a **úroveň služby** můžete nastavit na dvou místech. První místo je **záhlaví deníku plateb závazků** a druhé je **Metody platby závazků**. Po vytvoření řádků deníku plateb jsou hodnoty kódu platby nastavené v záhlaví deníku plateb převedeny do řádku deníku. Pokud nastaveny nejsou, budou použity hodnoty z metod platby.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Jaké parametry jsou k dispozici pro generování plateb převodů?
Seznam specifických parametrů závisí na formátu převodu kreditu. V následující tabulce jsou uvedeny parametry, které jsou k dispozici při generování souboru platby platebního převodu ISO 20022 do deníku plateb dodavatele pro Německo. Pomocí možností, které jsou k dispozici na kartě **Spustit na pozadí** můžete spustit generování platby v dávkovém režimu.

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
<td>Vyberte formát informací o úhradě v závislosti na požadavcích vaší země/oblasti nebo banky:
<ul>
<li><strong>Strukt.</strong> – Tuto možnost vyberte, chcete-li použít strukturovaný formát, když je jeden řádek platby vyrovnán proti jedné faktuře. Tato možnost není k dispozici pro formát exportu specifický pro zemi/oblast pro Francii, Německo nebo Nizozemsko.</li>
<li><strong>Nestrukt.</strong> – Tuto možnost vyberte, chcete-li použít nestrukturovaný formát, když je platba vyrovnána proti několika fakturám. Čísla faktur pro vyrovnání faktur jsou zřetězeny a použity jako informace o úhradě. V souladu s pokyny ISO 20022 jsou nestrukturované informace o úhradě omezeny na 140 znaků.</li>
</ul></td>
</tr>
<tr class="even">
<td>Počet faktur</td>
<td>Zadejte čísla faktur, ze kterých je vytištěna sestava <strong>Avízo platby</strong>.</td>
</tr>
<tr class="odd">
<td>Pořadové číslo</td>
<td>Zadejte pořadové číslo pro identifikaci souboru. Pořadové číslo se zobrazí v sestavě <strong>Průvodka</strong>.</td>
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
Mezinárodní číslo bankovního účtu (IBAN) a identifikační kód banky (IKB) slouží pro identifikaci každého účtu v 32 zemích/oblastech po celém světě. Patří sem 34 SEPA zemí / oblastí. Zadejte BIC do pole **Kód SWIFT** a IBAN do pole **IBAN**. Pro bankovní účet příjemce platby i bankovní účet odběratele jsou tato pole umístěny na pevné záložce **Další identifikační** na kartě **Bankovní účet** na stránce **Bankovní účty**. Použití BIC pro SEPA platby již není vynuceno.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Jak mohu přenést soubor platby do banky?
Při generování plateb je vygenerován soubor platby a budete vyzváni k jeho uložení z webového prohlížeče do kteréhokoli dostupného umístění. Dalším krokem je odeslání souboru XML do banky. Tento proces se v jednotlivých bankách liší. Postupujte podle pokynů vaší banky k odeslání souborů do banky ke zpracování.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

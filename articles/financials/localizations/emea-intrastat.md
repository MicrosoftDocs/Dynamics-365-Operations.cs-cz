---
title: Intrastat
description: Toto téma obsahuje informace o vykazování Intrastat pro obchodování se zbožím a v některých případech mezi zeměmi/oblastmi Evropské unie (EU). Poskytuje přehled o procesu vykazování a popisuje požadované nastavení a požadavky.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Intrastat
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 28581
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 50eb50c636d70dbdc374e8cfc89438433fb1f1b0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555506"
---
# <a name="intrastat"></a>Intrastat

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o vykazování Intrastat pro obchodování se zbožím a v některých případech mezi zeměmi/oblastmi Evropské unie (EU). Poskytuje přehled o procesu vykazování a popisuje požadované nastavení a požadavky.

Intrastat je systém pro shromažďování informací a generování statistik o obchodování se zbožím mezi zeměmi/oblastmi Evropské unie (EU). Vykazování v systému Intrastat je požadováno vždy, když produkt překročí hranice jiné země nebo oblasti v rámci EU. V některých zemích či oblastech platí povinnost vykazování v systému Intrastat také pro služby. V sestavách v systému Intrastat lze shromažďovat povinné i volitelné prvky. Následující prvky jsou povinné: identifikátor pro daň z přidané hodnoty (DPH) strany zodpovědné za poskytnutí informací, referenční období, tok (doručení nebo odeslání), číselný kód zboží, členský stát partnera (členský stát dodání při příjmu a členský stát pro cíl výdeje), hodnota zboží, množství zboží (čisté hmotnosti a doplňující jednotka) a druh transakce. Země či oblasti mohou za různých podmínek shromažďovat také volitelné prvky. Mezi volitelné prvky patří země/oblast původu, dodací podmínky, způsob dopravy, podrobnější kód zboží než CN8, oblast původu pro výdej a oblast určení na příjmu, statistická hodnota, popis zboží a přístav/letiště nakládky a vykládky.

## <a name="overview-of-the-intrastat-reporting-process"></a>Přehled procesu vykazování v systému Intrastat
V následujících částech je popsán celkový tok informací, které se používají k vykazování v systému Intrastat.

### <a name="1-enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>1. Zadání transakce, která překračuje hranice jiné země nebo oblasti EU

Faktura odběratele, faktura s volným textem, nákupní faktura, faktura projektu, dodací list odběratele, příjemka produktu dodavatele nebo převodní příkaz je převeden do deníku systému Intrastat pouze v případě, že je typ země/oblast cíle (na výdeji) nebo místo určení (na příjmu) **EU**. Tato funkce byla v aplikaci Microsoft Dynamics 365 for Operations (verze 1611) rozšířena a umožňuje zadat adresy nakládky pro intrakomunitární transakce. Pokud se liší adresa přepravních dokladů dodavatele od obchodní adresy (nebo obchodní adresy zákazníka pro objednávku vratky), bude hlášení Intrastat pracovat s těmito informacemi. Při vytvoření prodejní objednávky, faktury s volným textem, nákupní objednávky, faktury dodavatele, faktury projektu nebo převodního příkazu mají některá pole, která souvisejí se zahraničním obchodem, výchozí hodnoty v záhlaví dokumentu nebo na řádku. Výchozí kód transakce je převzat z odpovídajícího pole na stránce **Parametry zahraničního obchodu**. Výchozí kód komodity, země/oblast původu a stát/provincie původu jsou převzaty z položky. Výchozí hodnoty lze změnit a také můžete vyplnit další informace související se zahraničním obchodem: statistickou proceduru, způsob přepravy a přístav.

### <a name="2-use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>2. Použití deníku v systému Intrastat k vygenerování informací o obchodu mezi zeměmi/oblastmi EU

Každý měsíc generujete pro statistické účely informace o obchodu mezi zeměmi/oblastmi EU. Můžete převést transakce z faktury s volným textem, faktury odběratele, dodacího listu odběratele, faktury dodavatele, dodacího listu dodavatele, faktury projektu nebo převodního příkazu podle kritérií převodu, která jsou nastavena na stránce **Parametry zahraničního obchodu**. Případně můžete zadat transakci ručně. Je-li nutné upravit některé údaje, můžete převedené transakce v deníku systému Intrastat ručně aktualizovat. Za určitých podmínek, které jsou nastaveny na stránce **Komprese pro systém Intrastat**, můžete transakce v deníku systému Intrastat komprimovat. U některých zemí či oblastí lze aplikovat práh malé transakce. Transakce pod tuto prahovou hodnotu tak můžete vykazovat pod určeným kódem komodity. Kód komodity lze upravit na příslušných řádcích deníku systému Intrastat na základě nastavení **Minimální limit** na stránce **Parametry zahraničního obchodu**. Tyto transakce je možné také komprimovat podle nastavení **Komprese pro systém Intrastat**. Úplnost transakce v deníku systému Intrastat můžete ověřit na základě nastavení **Zkontrolovat nastavení** na stránce **Parametry zahraničního obchodu**. Úplnost dat v odpovídajících polích může být ověřena: země/oblast, stát nebo provincie, hmotnost, kód komodity, kód transakce, dodatečná jednotka, přístav, původ, podmínky dodání, způsob přepravy a číslo osvobození od daně. Nedokončené transakce budou označeny jako neplatné.

### <a name="3-use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>3. Použití deníku v systému Intrastat k vykázání informací o obchodu mezi zeměmi/oblastmi EU

Každý měsíc vykazujete pro statistické účely informace o obchodu mezi zeměmi/oblastmi EU. Můžete vytisknout sestavy systému Intrastat na základě nastavení **Mapování formátu sestavy** na stránce **Parametry zahraničního obchodu**. Také můžete vytvořit elektronický soubor na základě nastavení **Mapování formátu souboru** na stránce **Parametry zahraničního obchodu**. Další informace o souhrnném hlášení Intrastat, včetně požadovaných předpokladů naleznete na stránce souhrnného hlášení Intrastat:

-   Generování prohlášení Intrastat EU,
-   Přenos transakcí do systému Intrastat,
-   Zadání adresy nakládky pro interní transakci.

## <a name="prerequisites"></a>Předpoklady
V následující tabulce jsou uvedeny předpoklady pro vykazování v systému Intrastat.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Předpoklad</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Nastavení adresy</td>
<td>Nastavte kód země nebo oblasti používaný Mezinárodní organizací pro normalizaci (ISO).</td>
</tr>
<tr class="even">
<td>Právnická osoba</td>
<td>Nastavte číslo osvobození od daně pro import či export, rozšíření DIČ pobočky pro import/export a kód systému Intrastat, který je přiřazen k právnické osobě.</td>
</tr>
<tr class="odd">
<td>Hierarchie kategorií produktů (prodejní hierarchie, hierarchie zásobování)</td>
<td>Na kartě <strong>Kódy komodit</strong> na stránce <strong>Hierarchie kategorií</strong> přiřaďte kódy komodit v systému Intrastat k uzlům kategorií. Když přiřadíte kód komodity k nadřazenému uzlu kategorie, lze kód použít pro všechny podřízené uzly kategorií. Vybrané kódy komodit budou dostupné v zobrazení <strong>Vybrané</strong>, pokud daný kód komodity vyberete v podrobnostech o uvolněném produktu, na prodejní objednávce, na nákupní objednávce a na řádcích převodního příkazu.</td>
</tr>
<tr class="even">
<td>Podrobnosti o uvolněném produktu</td>
<td>Pro uvolněné produkty nastavte tato data zahraničního obchodu:
<ul>
<li><strong>Kód komodity</strong> – vyberte buď seznam vybraných komodit získaný z kategorie přiřazené produktu, nebo celý seznam kódů komodit v systému Intrastat.</li>
<li><strong>Statistické procento nákladů</strong></li>
<li><strong>Země/oblast původu</strong> – vyberte výchozí zemi nebo oblast, kde bylo zboží zcela získáno nebo vyrobeno.</li>
<li><strong>Stát/provincie původu/určení</strong> – vyberte výchozí stát/provincii určení a stát/provincii původu zásilky.</li>
<li><strong>Čistá hmotnost v kg</strong></li>
</ul></td>
</tr>
<tr class="odd">
<td>Zákazníci</td>
<td>Nastavte dodací adresu odběratele v zemi/regionu EU.</td>
</tr>
<tr class="even">
<td>Dodavatelé</td>
<td>Nastavte adresu dodavatele v zemi/regionu EU.</td>
</tr>
<tr class="odd">
<td>Vedlejší náklady</td>
<td>Nastavte, zda se má kód vedlejších nákladů zahrnout do fakturované částky, statistické částky, nebo do obou částek. Na stránce <strong>Kódy nákladů</strong> na kartě <strong>Zahraniční obchod</strong> kartu povolte, aby <strong>Hodnota faktury Intrastat</strong> zahrnovala částku nákladů v hodnotě faktury a aby <strong>Statistická hodnota Intrastat</strong> zahrnovala částku nákladů ve statistické hodnotě.</td>
</tr>
<tr class="even">
<td>Elektronické výkaznictví</td>
<td>Upravte konfiguraci elektronického vykazování tak, aby se data ze systému Intrastat exportovala do elektronického souboru v takovém formátu, který je vyžadován příslušnými orgány, a aby se tato data zobrazovala v uživatelsky přívětivém a čitelném formátu (například v aplikaci Microsoft Excel).</td>
</tr>
<tr class="even">
<td>Sklady</td>
<td>Přidružte účty dodavatele ke kódům skladu pro vyplnění čísla osvobození od daně při převodu převodního příkazu.</td>
</tr>
</tbody>
</table>

## <a name="setup"></a>Nastavení
V následujících částech je popsáno nastavení, které je nutné pro vykazování v systému Intrastat.

### <a name="set-up-all-required-intrastat-related-lists"></a>Nastavení všech požadovaných seznamů souvisejících se systémem Intrastat

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Seznam</th>
<th>Doplňkové informace</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Kódy komodit</td>
<td>Nastavte hierarchii kategorií typu <strong>Kód komodity</strong> a zadejte všechny kódy komodit podle seznamu kombinované nomenklatury. Pro každou komoditu nastavte tyto informace:
<ul>
<li>Název komodity a kód komodity</li>
<li>Popisný název a/nebo přeložený název</li>
<li>Nastavení pro vykazování dalších (doplňkových) jednotek na kartě <strong>Zahraniční obchod</strong>. Dodatečné jednotky můžete vybrat v seznamu jednotek. Můžete také určit, zda musí být společně se zvolenou dodatečnou jednotkou uvedena také hmotnost komodit.</li>
</ul></td>
</tr>
<tr class="even">
<td>Kódy transakce</td>
<td>Podle požadavků vaší země nebo oblasti nastavte druh transakce. Pro každý kód transakce, který nastavíte, je nutné nastavit pravidla pro výpočet fakturované částky a statistické částky pro převodní příkazy a prodejní nebo nákupní objednávky.
<ul>
<li>U převodních příkazů můžete nastavit některé z následujících pravidel pro výpočet částky faktury a statistických částek:
<ul>
<li><strong>Prázdné</strong> – částka bude mít hodnotu 0 (nula).</li>
<li><strong>Částka finančních nákladů</strong> – částka se bude rovnat finančním nákladům.</li>
<li><strong>Celkové náklady</strong> – částka se bude rovnat celkovým nákladům transakce.</li>
<li><strong>Ruční</strong> – částka se bude rovnat ručně zadané částce na řádku převodního příkazu.</li>
</ul></li>
<li>U prodejních a nákupních objednávek můžete nastavit některé z následujících pravidel pro výpočet fakturovaných částek a statistických částek:
<ul>
<li><strong>Prázdné</strong> – částka bude mít hodnotu 0 (nula).</li>
<li><strong>Fakturovaná částka</strong> – částka se bude rovnat částce fakturované pro komoditu.</li>
<li><strong>Základní částka</strong> – částka se bude rovnat fakturované částce před uplatněním slevy.</li>
</ul></li>
</ul></td>
</tr>
<tr class="odd">
<td>Způsoby přepravy</td>
<td>Podle požadavků vaší země nebo oblasti nastavte režim přepravy. Pro každý způsob dodání můžete na kartě <strong>Zahraniční obchod</strong> nastavit výchozí způsob přepravy.</td>
</tr>
<tr class="even">
<td>Přístavy</td>
<td>Pokud je tato informace vaší zemí nebo oblastí shromažďována, nastavte přístav/letiště nakládky/vykládky.</td>
</tr>
<tr class="odd">
<td>Statistické procedury</td>
<td>Pokud je tato informace vaší zemí nebo oblastí shromažďována, nastavte statistickou proceduru.</td>
</tr>
</tbody>
</table>

### <a name="set-up-rules-for-compressing-intrastat-transactions"></a>Nastavení pravidel pro kompresi transakcí v systému Intrastat

Na stránce **Komprese pro systém Intrastat** můžete vybrat pole, která mají být použita pro kompresi. Všechny transakce se stejnou kombinací hodnoty pro pole vybraná v deníku systému Intrastat budou při spuštění funkce komprese v deníku systému Intrastat komprimovány do jedné transakce.

### <a name="set-up-foreign-trade-parameters"></a>Nastavit parametry zahraničního obchodu

Stránka **Parametry zahraničního obchodu** slouží k nastavení parametrů uvedených v následující tabulce.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Karta</th>
<th>Parametry</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Obecné</td>
<td><ul>
<li><strong>Obecné</strong> – zadejte tyto informace:
<ul>
<li>Výchozí kódy transakce pro prodejní objednávky, nákupní objednávky, dobropisy a převodní příkazy. Kód transakce, který je nastaven pro dobropisy, slouží také jako kód vrácení fyzického zboží a používá se pro odchylky fyzických vratek vůči opravám dobropisů.</li>
<li>Zaměstnanec, který je zodpovědný za přípravu sestav v systému Intrastat.</li>
</ul></li>
<li><strong>Minimální limit</strong> – určete nastavení pro aktualizaci transakcí, které jsou pod prahovou hodnotu:
<ul>
<li>Prahové částka a hmotnost</li>
<li>Kód komodity, který se použije pro transakce spadající pod prahovou hodnotu</li>
</ul></li>
<li><strong>Přenos</strong> – určete kritéria pro přenos transakcí do deníku systému Intrastat. Můžete nastavit, aby se transakce přenášely pouze v případě, že budou položky splňovat všechna tato kritéria:
<ul>
<li>Nejedná se o servisní položky.</li>
<li>Položky mají kód komodity.</li>
<li>Položky mají hmotnost.</li>
<li>Položky mají dodatečné jednotky.</li>
</ul></li>
<li><strong>Zkontrolovat nastavení</strong> – určete pravidla pro ověření úplnosti dat v systému Intrastat. Můžete vybrat data, která budou ověřována.</li>
<li><strong>Pravidla zaokrouhlování</strong> – upravte následující nastavení pro zaokrouhlování částek a hmotností v sestavách v systému Intrastat:
<ul>
<li>Pravidlo zaokrouhlování (přesnost)</li>
<li>Metoda zaokrouhlování: nahoru, dolů nebo normální</li>
<li>Počet desetinných míst pro částky a hmotnosti</li>
<li>Pokyny pro zaokrouhlování hmotnosti, které jsou nižší než 1 kilogram (kg): nahoru na 1 kg, normální nebo bez zaokrouhlení</li>
</ul></li>
<li><strong>Elektronické výkaznictví</strong> – určete odkazy na konfigurace elektronického vykazování, abyste mohli vygenerovat elektronický soubor a sestavu.</li>
<li><strong>Hierarchie kódů komodit</strong> – zadejte hierarchie kategorií typu <strong>Kód komodity</strong>, který představuje kód komodity CN8 v systému Intrastat.</li>
  <li> <strong>Typ směnného kurzu</strong> – Volitelně můžete zadat směnný kurz, který se bude používat pro vykazování prodejů Intrastat a prodejních a nákupních transakcí v cizích měnách. Používá se, pokud je cena jiná než cena použitá při zaúčtování transakce.</li>  
</ul></td>
</tr>
<tr class="even">
<td>Kontaktní informace o zástupci</td>
<td>Zadejte jméno zástupce, jeho adresu, číslo osvobození od daně, telefonní číslo a číslo faxu.</td>
</tr>
<tr class="odd">
<td>Vlastnosti země/oblasti</td>
<td>Nastavte zemi/oblast aktuální právnické osoby na hodnotu <strong>Domácí</strong>. Nastavte zemi/oblasti zemí či oblastí EU, které se účastní obchodu v rámci EU, s aktuální právnickou osobou na hodnotu <strong>EU</strong>. Pro každou zemi/oblast určete také kód země/oblasti pro účely zahraničního obchodu.</td>
</tr>
<tr class="even">
<td>Číselná řada</td>
<td>Zadejte číselnou řadu pro deník systému Intrastat.</td>
</tr>
</tbody>
</table>


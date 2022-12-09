---
title: Intrastat - přehled
description: Tento článek obsahuje informace o vykazování Intrastat pro obchodování se zbožím a v některých případech mezi zeměmi/oblastmi Evropské unie (EU).
author: mrolecki
ms.date: 11/30/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: Intrastat
audience: Application User
ms.reviewer: kfend
ms.custom:
- "28581"
- intro-internal
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: mrolecki
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 762de8a098c61bc0d717c038d6ca0ff6d649bff3
ms.sourcegitcommit: 2804b05214c87f76457608b5db072582ff339852
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 12/01/2022
ms.locfileid: "9815700"
---
# <a name="intrastat-overview"></a>Intrastat - přehled

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o vykazování Intrastat pro obchodování se zbožím a v některých případech mezi zeměmi/oblastmi Evropské unie (EU). Tento článek také poskytuje přehled o procesu vykazování a popisuje požadované nastavení a požadavky.

Intrastat je systém pro shromažďování informací a generování statistik o obchodování se zbožím mezi zeměmi/oblastmi Evropské unie (EU). Vykazování v systému Intrastat je požadováno vždy, když produkt překročí hranice jiné země nebo oblasti v rámci EU. V některých zemích či oblastech platí povinnost vykazování v systému Intrastat také pro služby. V sestavách v systému Intrastat lze shromažďovat povinné i volitelné prvky. Následující prvky jsou povinné: identifikátor pro daň z přidané hodnoty (DPH) strany zodpovědné za poskytnutí informací, referenční období, tok (doručení nebo odeslání), číselný kód zboží, členský stát partnera (členský stát dodání při příjmu a členský stát pro cíl výdeje), hodnota zboží, množství zboží (čisté hmotnosti a doplňující jednotka) a druh transakce. Země či oblasti mohou za různých podmínek shromažďovat také volitelné prvky. Mezi volitelné prvky patří země/oblast původu, dodací podmínky, způsob dopravy, podrobnější kód zboží než CN8, oblast původu pro výdej a oblast určení na příjmu, statistická hodnota, popis zboží a přístav/letiště nakládky a vykládky.

## <a name="overview-of-the-intrastat-reporting-process"></a>Přehled procesu vykazování v systému Intrastat
V následujících částech je popsán celkový tok informací, které se používají k vykazování v systému Intrastat.

### <a name="enter-a-transaction-that-crosses-the-border-of-another-eu-countryregion"></a>Zadání transakce, která překračuje hranice jiné země nebo oblasti EU

Faktura odběratele, faktura s volným textem, nákupní faktura, faktura projektu, dodací list odběratele, příjemka produktu dodavatele nebo převodní příkaz je převeden do deníku systému Intrastat pouze v případě, že je typ země/oblast cíle (na výdeji) nebo místo určení (na příjmu) **EU**. Tato funkce byla v aplikaci Microsoft Dynamics 365 for Operations (verze 1611) rozšířena a umožňuje zadat adresy nakládky pro intrakomunitární transakce. Pokud se liší adresa přepravních dokladů dodavatele od obchodní adresy (nebo obchodní adresy zákazníka pro objednávku vratky), bude hlášení Intrastat pracovat s těmito informacemi. Při vytvoření prodejní objednávky, faktury s volným textem, nákupní objednávky, faktury dodavatele, faktury projektu nebo převodního příkazu mají některá pole, která souvisejí se zahraničním obchodem, výchozí hodnoty v záhlaví dokumentu nebo na řádku. Výchozí kód transakce je převzat z odpovídajícího pole na stránce **Parametry zahraničního obchodu**. Výchozí kód komodity, země/oblast původu a stát/provincie původu jsou převzaty z položky. Výchozí hodnoty lze změnit a také můžete vyplnit další informace související se zahraničním obchodem: statistickou proceduru, způsob přepravy a přístav.

### <a name="use-the-intrastat-journal-to-generate-information-about-trade-among-eu-countriesregions"></a>Použití deníku v systému Intrastat k vygenerování informací o obchodu mezi zeměmi/oblastmi EU

Každý měsíc generujete pro statistické účely informace o obchodu mezi zeměmi/oblastmi EU. Můžete převést transakce z faktury s volným textem, faktury odběratele, dodacího listu odběratele, faktury dodavatele, dodacího listu dodavatele, faktury projektu nebo převodního příkazu podle kritérií převodu, která jsou nastavena na stránce **Parametry zahraničního obchodu**. Případně můžete zadat transakci ručně. Je-li nutné upravit některé údaje, můžete převedené transakce v deníku systému Intrastat ručně aktualizovat. Za určitých podmínek, které jsou nastaveny na stránce **Komprese pro systém Intrastat**, můžete transakce v deníku systému Intrastat komprimovat. U některých zemí či oblastí lze aplikovat práh malé transakce. Transakce pod tuto prahovou hodnotu tak můžete vykazovat pod určeným kódem komodity. Kód komodity lze upravit na příslušných řádcích deníku systému Intrastat na základě nastavení **Minimální limit** na stránce **Parametry zahraničního obchodu**. Tyto transakce je možné také komprimovat podle nastavení **Komprese pro systém Intrastat**. Úplnost transakce v deníku systému Intrastat můžete ověřit na základě nastavení **Zkontrolovat nastavení** na stránce **Parametry zahraničního obchodu**. Úplnost dat v odpovídajících polích může být ověřena: země/oblast, stát nebo provincie, hmotnost, kód komodity, kód transakce, dodatečná jednotka, přístav, původ, podmínky dodání, způsob přepravy a číslo osvobození od daně. Nedokončené transakce budou označeny jako neplatné.

### <a name="use-the-intrastat-journal-to-report-information-about-trade-among-eu-countriesregions"></a>Použití deníku v systému Intrastat k vykázání informací o obchodu mezi zeměmi/oblastmi EU

Každý měsíc vykazujete pro statistické účely informace o obchodu mezi zeměmi/oblastmi EU. Můžete vytisknout sestavy systému Intrastat na základě nastavení **Mapování formátu sestavy** na stránce **Parametry zahraničního obchodu**. Také můžete vytvořit elektronický soubor na základě nastavení **Mapování formátu souboru** na stránce **Parametry zahraničního obchodu**. Další informace o souhrnném hlášení Intrastat, včetně požadovaných předpokladů naleznete na stránce souhrnného hlášení Intrastat:

  - Generování prohlášení Intrastat EU,
  - Přenos transakcí do systému Intrastat,
  - Zadání adresy nakládky pro interní transakci.

## <a name="prerequisites"></a>Předpoklady
V následující tabulce jsou uvedeny předpoklady pro vykazování v systému Intrastat.

|  Předpoklad  |  Popis  |
|-------------------------|-------------------------|
| Nastavení adresy | Nastavte kód země nebo oblasti používaný Mezinárodní organizací pro normalizaci (ISO). |
| Právnická osoba | Nastavte číslo osvobození od daně pro import či export, rozšíření DIČ pobočky pro import/export a kód systému Intrastat, který je přiřazen k právnické osobě. |
| Hierarchie kategorií produktů (prodejní hierarchie, hierarchie zásobování) | Na kartě **Kódy komodit** na stránce **Hierarchie kategorií** přiřaďte kódy komodit v systému Intrastat k uzlům kategorií. Když přiřadíte kód komodity k nadřazenému uzlu kategorie, lze kód použít pro všechny podřízené uzly kategorií. Vybrané kódy komodit budou dostupné v zobrazení **Vybrané**, pokud daný kód komodity vyberete v podrobnostech o produktu, na prodejní objednávce, na nákupní objednávce a na řádcích převodního příkazu. |
| Podrobnosti o uvolněném produktu | Pro uvolněné produkty nastavte tato data zahraničního obchodu:<ul><li>**Kód komodity** – vyberte buď seznam vybraných komodit získaný z kategorie přiřazené produktu, nebo celý seznam kódů komodit v systému Intrastat.</li><li>**Statistické procento nákladů**</li><li>**Země/oblast původu** – vyberte výchozí zemi nebo oblast, kde bylo zboží zcela získáno nebo vyrobeno.</li><li>**Stát/provincie původu/určení** – vyberte výchozí stát/provincii určení a stát/provincii původu zásilky.</li><li>**Čistá hmotnost v kg**</li><li>**Vyloučit** – Povolte tento parametr, aby se transakce s tímto produktem nepřenášely do Intrastatu</li></ul> |
| Odběratelé | Nastavte dodací adresu odběratele v zemi/regionu EU. |
| Dodavatelé | Nastavte adresu dodavatele v zemi/regionu EU. |
| Vedlejší náklady | Nastavte, zda se má kód vedlejších nákladů zahrnout do fakturované částky, statistické částky, nebo do obou částek. Na stránce **Kódy nákladů** na kartě **Zahraniční obchod** kartu povolte, aby **Hodnota faktury Intrastat** zahrnovala částku nákladů v hodnotě faktury a aby **Statistická hodnota Intrastat** zahrnovala částku nákladů ve statistické hodnotě.</br>Další informace naleznete v příkladu [Transakční kódy a různé poplatky](#transaction-codes-and-miscellaneous-charges). |
| Elektronická sestava | Upravte konfiguraci elektronického vykazování tak, aby se data ze systému Intrastat exportovala do elektronického souboru v takovém formátu, který je vyžadován příslušnými orgány, a aby se tato data zobrazovala v uživatelsky přívětivém a čitelném formátu (například v aplikaci Microsoft Excel). |
| Sklady | Přidružte účty dodavatele ke kódům skladu pro vyplnění čísla osvobození od daně při převodu převodního příkazu.</br>Další informace naleznete v příkladu [Převodní příkaz](#transfer-order).|

## <a name="setup"></a>Nastavení
V následujících částech je popsáno nastavení, které je nutné pro vykazování v systému Intrastat.

### <a name="set-up-all-required-intrastat-related-lists"></a>Nastavení všech požadovaných seznamů souvisejících se systémem Intrastat

|   Seznam   |   Doplňkové informace   |
|-------------------------|-------------------------|
| Kódy komodit | Nastavte hierarchii kategorií typu **Kód komodity** a zadejte všechny kódy komodit podle seznamu kombinované nomenklatury. Pro každou komoditu nastavte tyto informace:<ul><li>Název komodity a kód komodity</li><li>Popisný název a/nebo přeložený název</li><li>Nastavení pro vykazování dalších (doplňkových) jednotek na kartě **Zahraniční obchod**. Dodatečné jednotky můžete vybrat v seznamu jednotek. Můžete také určit, zda musí být společně se zvolenou dodatečnou jednotkou uvedena také hmotnost komodit.</li></ul>Další informace naleznete v příkladu [Další jednotky](#additional-units).|
| Kódy transakce | Podle požadavků vaší země nebo oblasti nastavte druh transakce. Pro každý kód transakce, který nastavíte, je nutné nastavit pravidla pro výpočet fakturované částky a statistické částky pro převodní příkazy a prodejní nebo nákupní objednávky.<ul><li>U převodních příkazů můžete nastavit některé z následujících pravidel pro výpočet částky faktury a statistických částek:<ul><li>**Prázdné** – částka bude mít hodnotu 0 (nula).</li><li>**Částka finančních nákladů** – částka se bude rovnat finančním nákladům.</li><li>**Celkové náklady** – částka se bude rovnat celkovým nákladům transakce.</li><li>**Ruční** – částka se bude rovnat ručně zadané částce na řádku převodního příkazu.</li></ul></li><li>U prodejních a nákupních objednávek můžete nastavit některé z následujících pravidel pro výpočet fakturovaných částek a statistických částek:<ul><li>**Prázdné** – částka bude mít hodnotu 0 (nula).</li><li>**Fakturovaná částka** – částka se bude rovnat částce fakturované pro komoditu.</li><li>**Základní částka** – částka se bude rovnat fakturované částce před uplatněním slevy.</li></ul></ul>Další informace naleznete v příkladu [Transakční kódy a různé poplatky](#transaction-codes-and-miscellaneous-charges). |
| Způsoby přepravy | Podle požadavků vaší země nebo oblasti nastavte režim přepravy. Pro každý způsob dodání můžete na kartě **Zahraniční obchod** nastavit výchozí způsob přepravy. |
| Přístavy | Pokud je tato informace vaší zemí nebo oblastí shromažďována, nastavte přístav/letiště nakládky/vykládky. |
| Statistické procedury | Pokud je tato informace vaší zemí nebo oblastí shromažďována, nastavte statistickou proceduru. |



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
<li>Výchozí kódy transakce pro prodejní objednávky, nákupní objednávky, dobropisy a převodní příkazy. Kód transakce, který je nastaven pro dobropisy, slouží také jako kód vrácení fyzického zboží a používá se pro odchylky fyzických vratek vůči opravám dobropisů. Vrácení fyzického zboží se vykazuje v převodu Intrastat jiným směrem. Vrácení při doručení je vykázáno jako odeslání a vrácení při odeslání je vykázáno jako doručení.</li>
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

## <a name="example"></a>Příklad

### <a name="transaction-codes-and-miscellaneous-charges"></a><a name= "transaction-codes-and-miscellaneous-charges"></a>Transakční kódy a různé poplatky

Tento článek pokrývá scénář, kdy společnost v Německu musí nakupovat zboží od společnosti v Itálii. K provedení tohoto nákupu musí německá společnost nastavit nové kódy transakcí a nakonfigurovat pravidla výpočtu pro fakturovanou částku a statistickou částku pro tyto kódy transakcí. Kromě toho, když společnost vytváří fakturu, musí specifikovat různé poplatky a jejich procenta. Tyto hodnoty budou brány v úvahu při výpočtu statistické hodnoty.

Tento scénář používá právnickou osobu **DEMF**.

#### <a name="preliminary-setup"></a>Předběžné nastavení

1. Přejděte na **Správa organizace** > **Organizace** > **Právnické osoby** a vyberte **DEMF**.
2. Na pevné záložce **Adresy** zkontrolujte, že pole **Země/oblast** je nastaveno na **DEU (Německo)**.
3. Přejděte do části **Závazky** > **Dodavatelé** > **Všichni dodavatelé**.
4. V mřížce vyberte **DE-001**.
5. Na záložce s náhledem **Adresa** vyberte **Upravit**.
6. V dialogovém okně **Upravit adresu** v poli **Země/oblast** vyberte **ITA**.
7. Zvolte **OK** a zavřete dialogové okno.

#### <a name="set-up-transaction-codes"></a>Nastavit kódy transakcí

1. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Kódy transakcí**.
2. V mřížce vyberte **11**. Poté v podokně akcí zvolte **Odstranit**.
3. V podokně akcí zvolte **Nový**.
4. Na pevné záložce **Transakční kódy** v poli **Kód** **transakce** zadejte **11**.
5. Do pole **Název** zadejte **Přímý nákup/prodej**.
6. V části **Prodeje a nákupy** v poli **Částka faktury** vyberte **Částka faktury**.
7. V poli **Statistická částka** vyberte **Částka faktury**.
8. V podokně akcí vyberte **Uložit**.

#### <a name="set-up-miscellaneous-charges"></a>Nastavení různých poplatků

1. Přejděte na **Pohledávky** > **Nastavení poplatky** > **Kód nákladů**.
2. V mřížce vyberte **Doprava**.
3. V podokně akcí vyberte **Upravit**.
4. Na pevné záložce **Zahraniční obchod** nastavte možnosti **Hodnota faktury pro Intrastat** a **Statistická hodnota Intrastat** na **Ano**.

#### <a name="set-up-foreign-trade-parameters"></a>Nastavit parametry zahraničního obchodu

1. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Parametry zahraničního obchodu**.
2. Na kartě **Intrastat** na záložce s náhledem **Obecné** v poli **Kód** **transakce** vyberte **11**.
3. Na záložce s náhledem **Hierarchie komoditních kódů** ověřte, že je pole **Hierarchie kategorií** nastaveno na **Intrastat**.

#### <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky

1. Přejděte na **Závazky** > **Nákupní objednávky** > **Všechny nákupní objednávky**.
2. V podokně akcí zvolte **Nový**.
3. V dialogovém okně **Vytvoření nákupní objednávky** v poli **Účet dodavatele** vyberte **DE-001**.
4. Vyberte **OK**.
5. Na kartě **Záhlaví** na pevné záložce **Zahraniční** **obchod** ověřte, že je pole **Kód transakce** nastaveno na **11**.
6. Na kartě **Řádky** na záložce s náhledem **Řádky nákupní objednávky** v poli **Číslo položky** vyberte **D0003**. Poté do pole **Množství** zadejte **10**.
7. Na záložce s náhledem **Podrobnosti řádku** na kartě **Zahraniční obchod** v části **Zahraniční obchod** zkontrolujte, zda je automaticky nastaveno pole **Kód transakce**.
8. Na pevné záložce **Řádky nákupní objednávky** v nabídce **Finanční údaje** v části **Poplatky** vyberte **Spravovat poplatky**.
9. Do pole **Kód poplatků** zadejte **FREIGHT**.
10. Do pole **Kód nákladů** zadejte **30**.
11. V podokně akcí vyberte **Uložit**. Poté stránku zavřete.
12. V podokně akcí na kartě **Nákup** ve skupině **Akce** zvolte **Potvrdit**.
13. V podokně akcí na kartě **Faktura** ve skupině **Generovat** zvolte **Faktura**.
14. V podokně akcí vyberte **Výchozí od**. V poli **Výchozí množství pro řádky** vyberte **Objednané množství**. Pak vyberte **OK**.
15. Na pevné záložce **Záhlaví faktury dodavatele** v sekci **Identifikace faktury** v poli **Číslo** zadejte **00100**.
16. V sekci **Termíny faktur** v poli **Datum faktury** vyberte **24. 11. 2021** (24. listopadu 2021).
17. Chcete-li zaúčtovat fakturu, vyberte **Zaúčtovat** z akčního podokna.

### <a name="transfer-the-vendor-invoice-to-the-intrastat-journal"></a>Přeneste fakturu dodavatele do deníku Intrastat

1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
2. V podokně akcí zvolte **Převod**.
3. V dialogovém okně **Intrastat (přenos)** nastavte možnost **Faktura dodavatele** na **Ano**.
4. Vyberte **OK** pro přenesení transakcí a zkontrolujte deník Intrastat.

   ![Řádek, který představuje nákupní objednávku s různými poplatky na stránce Intrastat](media/intrastat_overview_1.png)

5. Zkontrolujte kartu **Všeobecné** pro nákupní objednávku. Všimněte si, že pole **Hodnota faktury** zobrazuje součet polí **Částka faktury** a **Částka fakturovaných poplatků** a pole **Statistická hodnota** zobrazuje součet polí **Statistická částka** a **Statistická částka poplatků**.

   ![Podrobnosti o nákupní objednávce s různými poplatky na kartě Obecné na stránce Intrastat](media/intrastat_overview_2.png)

### <a name="transfer-order"></a>Převodní příkaz

V tomto příkladu musí společnost v Německu přesunout dvě jednotky zboží ze skladu v Německu do skladu v Itálii. Pro tento produkt musí být také specifikovány poplatky ve výši 20 % pro účtování v poli **Statistická hodnota**. Tento příklad používá právnickou osobu **DEMF**.

#### <a name="preliminary-setup"></a>Předběžné nastavení

1. Přejděte na **Správa organizace** > **Organizace** > **Právnické osoby** a vyberte **DEMF**.
2. Na pevné záložce **Adresy** zkontrolujte, že pole **Země/oblast** je nastaveno na **DEU (Německo)**.
3. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Parametry zahraničního obchodu**.
4. Na záložce s náhledem **Hierarchie komoditních kódů** ověřte, že je pole **Hierarchie kategorií** nastaveno na **Intrastat**.
5. Přejděte do části **Závazky** > **Dodavatelé** > **Všichni dodavatelé**.
6. V mřížce vyberte **DE-001**.
7. Na záložce s náhledem **Adresa** vyberte **Upravit**.
8. V dialogovém okně **Upravit adresu** v poli **Země/oblast** vyberte **ITA**.
9. Zvolte **OK** a zavřete dialogové okno.

#### <a name="set-up-transaction-codes"></a>Nastavit kódy transakcí

1. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Kódy transakcí**.
2. V mřížce vyberte **11**. Poté v podokně akcí zvolte **Odstranit**.
3. V podokně akcí zvolte **Nový**.
4. Na pevné záložce **Transakční kódy** v poli **Kód** **transakce** zadejte **11**.
5. Do pole **Název** zadejte **Přímý nákup/prodej**.
6. V části **Převodní příkaz** v poli **Částka faktury** vyberte **Celkové náklady**.
7. V poli **Statistická částka** vyberte **Celkové náklady**.
8. V podokně akcí vyberte **Uložit**.
9. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Parametry zahraničního obchodu**.
10. Na kartě **Intrastat** na pevné záložce **Všeobecné** v poli **Převodní příkaz** vyberte **11**.

#### <a name="set-up-charges-for-an-item"></a>Nastavení poplatků pro zboží

1. Přejděte na **Řízení informací o produktech** > **Produkty** > **Uvolněné produkty**.
2. V mřížce vyberte **D0001**.
3. Na záložce s náhledem **Zahraniční obchod** v sekci **Intrastat** do pole **Procento poplatků** zadejte **20**.

#### <a name="change-the-site-address"></a>Změňte adresu webu

1. Přejděte do nabídky **Warehouse Management** > **Nastavení** > **Sklad** > **Pracoviště**.
2. V mřížce vyberte **1**.
3. Na záložce s náhledem **Adresy** vyberte **Upravit**.
4. V dialogovém okně **Upravit adresu** v poli **Země/oblast** vyberte **DEU**.
5. Vyberte **OK**.
6. V mřížce vyberte **2**.
7. Na záložce s náhledem **Adresy** vyberte **Upravit**.
8. V dialogovém okně **Upravit adresu** v poli **Země/oblast** vyberte **ITA**.
9. Vyberte **OK**.
10. Přejděte na **Řízení skladu** > **Nastavení** > **Sklad** > **Sklady**.
11. V mřížce vyberte **21**.
12. Na záložce s náhledem **Obecné** v sekci **Reference** v poli **Účet dodavatele** vyberte **DE-001**.

#### <a name="create-a-transfer-order"></a>Vytvoření převodního příkazu

1. Přejděte na **Správa zásob** > **Odchodí objednávky** > **Převodní příkaz**.
2. V podokně akcí zvolte **Nový**.
3. Na kartě **Řádky** na pevné záložce **Hlavička převodního příkazu** v části **Přehled** v poli **Ze skladu** vyberte **11**. V poli **Ze skladu** zvolte **21**.
4. Na kartě **Řádky** na pevné záložce **Řádky převodní objednávky** vyberte **Přidat**.
5. V poli **Číslo položky** zvolte **D0001**. Poté do pole **Převáděné množství** zadejte **2**.
6. Na záložce s náhledem **Podrobnosti řádku** na kartě **Zahraniční obchod** v části **Zahraniční obchod** zkontrolujte, zda je automaticky nastaveno pole **Kód transakce**.
7. V podokně akcí na kartě **Odeslání** ve skupině **Operace** vyberte **Odeslat převodní příkaz**.
8. V dialogovém okně **Dodávka** na kartě **Přehled** v poli **Aktualizace** vyberte **Vše**.
9. Výběrem **OK** odešlete příkaz.
10. V podokně Akce na kartě **Přijmout** ve skupině **Operace** zvolte **Přijmout**.
11. V dialogovém okně **Příjem** na kartě **Přehled** v poli **Aktualizace** vyberte **Vše**.
12. Výběrem **OK** odešlete příkaz.

#### <a name="transfer-the-transfer-order-to-the-intrastat-journal"></a>Přenesení převodního příkazu do deníku Intrastat

1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
2. V podokně akcí zvolte **Převod**.
3. V dialogovém okně **Intrastat (převod)** nastavte možnost **Převodní příkaz** na **Ano** a všechny další možnosti na **Ne**.
4. Vyberte **OK** pro přenesení transakcí a zkontrolujte deník Intrastat.

   ![Řádek, který představuje převodní příkaz na stránce Intrastat](media/intrastat_overview_3.png)

5.  Zkontrolujte kartu **Všeobecné** pro převodního příkazu.

    Všimněte si, že pole v částech **Hodnota faktury** a **Statistická hodnota** jsou nastaveny automaticky. Hodnoty **Částka faktury** a **Statistická částka** jsou založena na nastavení na stránce **Transakční kódy**. Hodnota **20** v poli **Procento poplatků** je hodnota, která je nastavena na stránce **Vydaný produkt**. Hodnota v poli **Statistická výše poplatků** je kvantitativní vyjádření poplatků (protože 107,24 se rovná 20 % z 536,18). Hodnota pole **Statistická hodnota** je součet hodnot z polí **Statistická částka** a **Statistická výše poplatků**.

  ![Podrobnosti o převodním příkazu na kartě Obecné na stránce Intrastat](media/intrastat_overview_4.png)

### <a name="additional-units"></a>Dodatečné jednotky

V tomto příkladu musí společnost v Německu nakoupit 10 jednotek zboží od společnosti v Itálii. Kromě kódů zboží musí být pro toto zboží uvedeny další jednotky. Příklad ukazuje, jak vytvořit nové měrné jednotky, přiřadit další jednotky ke kódu komodity Intrastat, zaúčtovat transakce, které mají další jednotky, a zkontrolovat deník Intrastat, kde je nastaveno pole pro další jednotky.

#### <a name="preliminary-setup"></a>Předběžné nastavení

1. Přejděte na **Správa organizace** > **Organizace** > **Právnické osoby** a vyberte **DEMF**.
2. Na pevné záložce **Adresy** zkontrolujte, že pole **Země/oblast** je nastaveno na **DEU (Německo)**.
3. Přejděte na **Daň** > **Nastavení** > **Zahraniční obchod** > **Parametry zahraničního obchodu**.
4. Na kartě **Intrastat** na záložce s náhledem **Obecné** v poli **Kód** **transakce** vyberte **11**.
5. Na záložce s náhledem **Hierarchie komoditních kódů** ověřte, že je pole **Hierarchie kategorií** nastaveno na **Intrastat**.
6. Přejděte do části **Závazky** > **Dodavatelé** > **Všichni dodavatelé**.
7. V mřížce vyberte **DE-001**.
8. Na záložce s náhledem **Adresa** vyberte **Upravit**.
9. V dialogovém okně **Upravit adresu** v poli **Země/oblast** vyberte **ITA**.
10. Zvolte **OK** a zavřete dialogové okno.

#### <a name="create-a-unit-of-measure"></a>Vytvoření měrné jednotky

1. Přejděte do nabídky **Správa organizace** > **Nastavení** > **Jednotky** > **Jednotky**.
2. V podokně akcí zvolte **Nový**.
3. V poli **Jednotka** zadejte název měrné jednotky. V tomto příkladu zadejte **GRM**.
4. Na rychlé kartě **Všeobecné** v části **Klasifikace** v poli **Třída jednotky** vyberte vlastnost, kterou jednotka měří. V tomto příkladu vyberte **Hmotnost**.
5. V poli **Systém jednotek** vyberte měrný systém, ke kterému jednotka patří. Například vyberte **Metrické jednotky**.

#### <a name="set-up-unit-conversions"></a>Nastavení převodů jednotek

1. Přejděte do nabídky **Správa organizace** > **Nastavení** > **Jednotky** > **Převody jednotek**.
2. Na kartě **Převody mezi třídami** vyberte **Nový**.
3. V dialogovém okně **Převod jednotky** v poli **Produkt** vyberte **F00007**.
4. V poli **Z jednotky** pak vyberte možnost **ea**.
5. V poli **Na jednotku** pak vyberte možnost **GRM**.
6. Ověřte, zda je konverzní poměr **1 = 1**.
7. Vyberte **OK**.
8. Přejděte na **Řízení informací o produktech** > **Produkty** > **Uvolněné produkty**.
9. V mřížce vyberte **F00007**.
10. Na záložce s náhledem **Správa zásob** v sekci **Zásoby** v poli **Jednotka** vyberte **GRM**.
11. V podokně akcí vyberte **Uložit**.

#### <a name="set-up-product-information"></a>Nastavení Informací o produktu

1. Přejděte na **Řízení informací o produktech** > **Produkty** > **Uvolněné produkty**.
2. V mřížce vyberte **F00007**.
3. Na záložce s náhledem **Zahraniční obchod** v sekci **Intrastat** v poli **Komodita** vyberte **920 20 34**.
4. V podokně akcí vyberte **Uložit**.

#### <a name="assign-the-additional-unit-to-an-intrastate-commodity-code"></a>Přiřazení další jednotky kódu komodity Intrastat

1. Přejděte do nabídky **Řízení informací o produktech** > **Nastavení** > **Kategorie a atributy** > **Hierarchie kategorií**.
2. V seznamu vyberte **Intrastat**.
3. V mřížce vyberte **Reproduktor**.
4. Na pevné záložce **Zahraniční obchod** v poli **Další jednotky** vyberte **GRM**.
5. V podokně akcí vyberte **Uložit**.

   Více informací viz [Správa měrných jednotek](../../supply-chain/pim/tasks/manage-unit-measure.md).

#### <a name="create-a-purchase-order"></a>Vytvoření nákupní objednávky

1. Přejděte na **Závazky** > **Nákupní objednávky** > **Všechny nákupní objednávky**.
2. V podokně akcí zvolte **Nový**.
3. V dialogovém okně **Vytvoření nákupní objednávky** v poli **Účet dodavatele** vyberte **DE-001**.
4. Vyberte **OK**.
5. Na kartě **Záhlaví** na pevné záložce **Zahraniční** **obchod** ověřte, že je pole **Kód transakce** nastaveno na **11**.
6. Na kartě **Řádky** na záložce s náhledem **Řádky nákupní objednávky** v poli **Číslo položky** vyberte **F00007**. Poté do pole **Množství** zadejte **10**.
7. Na záložce s náhledem **Podrobnosti řádku** na kartě **Zahraniční obchod** v části **Zahraniční obchod** zkontrolujte, zda jsou automaticky nastavena pole **Kód transakce** a **Komodita**.
8. V podokně akcí na kartě **Nákup** ve skupině **Akce** zvolte **Potvrdit**.
9. V podokně akcí na kartě **Faktura** ve skupině **Generovat** zvolte **Faktura**.
10. V podokně akcí vyberte **Výchozí od**. V poli **Výchozí množství pro řádky** vyberte **Objednané množství**. Pak vyberte **OK**.
11. Na záložce s náhledem **Záhlaví faktury dodavatele** v sekci **Identifikace faktury** v poli **Číslo** zadejte **VE-0010**.
12. V sekci **Termíny faktur** v poli **Datum faktury** vyberte **5. 10. 2021** (5. října 2021).
13. Chcete-li zaúčtovat fakturu, vyberte **Zaúčtovat** z akčního podokna.

#### <a name="transfer-the-vendor-invoice-to-the-intrastat-journal"></a>Přeneste fakturu dodavatele do deníku Intrastat

1. Přejděte na **Daň** > **Deklarace** > **Zahraniční obchod** > **Intrastat**.
2. V podokně akcí zvolte **Převod**.
3. V dialogovém okně **Intrastat (přenos)** nastavte možnost **Faktura dodavatele** na **Ano**.
4. Vyberte **OK** pro přenesení transakcí a zkontrolujte deník Intrastat.

   ![Řádek, který představuje nákupní objednávku na stránce Intrastat](media/intrastat_overview_5.png)

5. Zkontrolujte kartu **Všeobecné** pro nákupní objednávku. Všimněte si, že pole **Množství dalších jednotek** a **Další jednotka** v části **Jednotka** jsou nastavena automaticky.

   ![Podrobnosti o nákupní objednávce na kartě Obecné na stránce Intrastat](media/intrastat_overview_6.png)
   
## <a name="list-of-countryregion-specific-articles"></a>Seznam článků specifických pro zemi/oblast
V následující tabulce jsou uvedeny dostupné články intrastatu pro jednotlivé země/oblasti.

| Země/oblast          | Odkaz      |
|------------------|-----------|
| Rakousko          |[Rakouský Intrastat](emea-aut-intrastat.md)| 
| Belgie          |[Belgický Intrastat](emea-bel-intrastat.md)|
| Česká republika   |[Český Intrastat](emea-cze-intrastat.md)|
| Dánsko          |[Dánský Intrastat](emea-dnk-intrastat.md)|
| Estonsko          |[Estonský Intrastat](emea-est-intrastat.md)|
| Finsko          |[Intrastat pro Finsko](emea-fin-intrastat.md)|
| Francie           |[Francouzský Intrastat](emea-fra-intrastat.md)|
| Německo          |[Německý Intrastat](emea-deu-intrastat.md)|
| Maďarsko          |[Maďarský Intrastat](emea-hun-intrastat.md)|
| Itálie            |[Italský Intrastat](emea-ita-intrastat.md)|
| Lotyšsko           |[Lotyšský Intrastat](emea-lva-intrastat.md)|
| Litva        |[Intrastat pro Litvu](emea-ltu-intrastat.md)|
| Nizozemsko      |[Nizozemský Intrastat](emea-nl-intrastat.md)|
| Polsko           |[Intrastat - Polsko](emea-pol-intrastat.md)|
| Španělsko            |[Intrastat – Španělsko](emea-esp-intrastat.md)|
| Švédsko           |[Švédský Intrastat](emea-swe-intrastat.md)|


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

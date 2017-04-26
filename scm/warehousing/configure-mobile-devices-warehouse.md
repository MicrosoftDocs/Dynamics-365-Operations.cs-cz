---
title: "Nastavení mobilních zařízení pro práci, sklad"
description: "Tento článek popisuje způsob konfigurace položek nabídky, které pracovníci ve skladě mohou používat k práci z mobilního zařízení."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-01-22 07 - 59 - 32
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: WHSRFMenuItem
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 29941
ms.assetid: 6dff6313-dc6e-4f06-9c0c-dab24eefe4da
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: afa59439e06aad9d669eb352a9837a013f447249
ms.openlocfilehash: 34d7b246d74d1546b54494944903d160e31f7678
ms.lasthandoff: 03/31/2017


---

# <a name="set-up-mobile-devices-for-warehouse-work"></a>Nastavení mobilních zařízení pro práci, sklad

Tento článek popisuje způsob konfigurace položek nabídky, které pracovníci ve skladě mohou používat k práci z mobilního zařízení.

**Poznámka:** Tento článek se vztahuje k funkcím v modulu Řízení skladu. Nevztahuje se na funkce v modulu Řízení zásob. Položky nabídky, které se objevují v nabídkách mobilního zařízení pro sklad jsou nastaveny na stránce **Položky nabídky mobilního zařízení**. Vzhledem k tomu, že položky nabídky mohou být umístěny do různých nabídek, je snadné nakonfigurovat struktury nabídky tak, aby byly zveřejněny konkrétním uživatelům pouze určité typy činností. Můžete konfigurovat položky nabídky tak, aby prováděly následující úlohy:

-   Zpracování dotazu nebo provedení aktivity, jako je tisk štítku, generování registrační značky vozidla, spuštění výrobní zakázky nebo rychlé vyhledání informací o položkách ve skladovém místě.
-   Vytvořte práci, která se provede prostřednictvím jiného procesu. Například přijetím položky pro nákupní objednávku můžete vytvořit pracovní vyskladnění pro jiného pracovníka.
-   Provedení práce, která byla vytvořena jiným procesem (existující práce), jako je například vyskladnění, které bylo vytvořeno při přijetí položky pro nákupní objednávku.

Pokud chcete vytvořit položku nabídky pro aktivity nebo dotaz **režim** na **nepřímé**. Seznam **kód aktivity** možnosti pak jsou k dispozici, takže můžete vybrat typ dotazu nebo činnost, která je položka nabídky pro. Chcete-li vytvořit položku nabídky pro generování práce skladu, nastavte **režim** na **práce**. Seznam **pracovní proces vytváření** možnosti pak jsou k dispozici. Pokud chcete vytvořit položku nabídky ke zpracování existující skladové práce, nastavte pole **Režim** na **Práce** a nastavte možnost **Použít stávající práci** na **Ano**. **Poznámka:** další pole mohou být k dispozici pro položky nabídky, v závislosti na režimu, který vyberete pro nabídku zboží a zda položky nabídky slouží k provádění stávající práce. Informace o výběru dalších polí naleznete v části "Další položky Možnosti nabídky" dále v tomto článku.

## <a name="configure-menu-items-for-activities-and-inquiries"></a>Konfigurace položek nabídky pro aktivity a dotazy
Pokud pole **Režim** pro položku nabídky je nastaveno na **Nepřímé**, můžete vytvořit položku nabídky pro provádění hlavní aktivity nebo dotazu, který nevytváří práci. Příklady zahrnují opakovaný tisk popisků registrační značky vozidel a dotaz na položky ve skladovém místě. V následující tabulce jsou uvedeny možnosti, které jsou k dispozici.

| Možnost                      | Popis                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Žádné                        | Tato výchozí hodnota neumožňuje použití aktivity nebo dotazu.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| O aplikaci                       | Prohlédněte si informace o systému, jako je číslo verze, ID skladu nebo pracovník, který je aktuálně přihlášen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Změnit sklad            | Změňte sklad, kde je zaměstnanec přihlášen.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Dotaz na umístění            | Prohlédněte si informace o všech položkách a množství pro dané skladové místo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| Dotaz na registrační značku vozidla       | Prohlédněte si množství položek na registrační značce a umístění registrační značky.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Spustit výrobní zakázku      | Spusťte výrobní zakázku.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Výrobní odpad            | Zadejte množství odpadu, který byl vytvořen během výroby pro každý řádek kusovníku.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Poslední paleta výroby      | Uveďte, že byla vyrobena poslední paleta zboží pro výrobní zakázku, a že je nutné aktualizovat stav výrobní zakázky tak, aby byl **hlášen jako dokončený**. Stav surovin, které nebyly při výrobě spotřebovávají, se vrátí z kategorie **Vyskladněno** na **Na objednávce**, a položky se mohou vrátit mezi zásoby.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Dotaz na zboží                | Naskenujte položku a určete, kde se ve skladě nachází. Dotaz vrátí všechna umístění a množství pro skenovanou položku.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Znovu vytisknout štítek               | Znovu vytiskněte štítek registrační značky.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Sestavení registrační značky vozidla         | Vytvořte nadřazenou registrační značku kombinací více registračních značek ve stejném skladovém místě. Tato možnost je užitečná, pokud přesouváte více registračních značek současně. Poté, co je nadřazená registrační značka přesunuta, je nutné provést změnu registračních značek předtím, než je možné vybrat položky pro každou z registračních značek. **Tip:** Pro přesun nadřazené registrační značky je nutné použít mobilní zařízení konfigurováno pro vytváření přesouvané práce.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Seskupení registračních značek         | Změňte sestavení registrační značky tak, že bude možné vyzvednout položky ze sestavených registračních značek.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Přihlášení řidiče             | Pokud používáte aplikaci Správa přepravy, zaregistrujte naskenováním ID odchozího nákladu, ID události a ID dodávky skutečnost, že se dostavil řidič. Pro tuto možnost je zapotřebí přiřazení vytížení k události a nastavení stavu vytížení na **Naloženo**.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Odhlášení řidiče            | Zaregistrujte, že řidič ukončil svoji schůzku.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Vymazat mezipaměť číselných řad | Odstraňte čísla z číselné řady z mezipaměti pro pořadová čísla. Tuto aktivitu většinou provádí správce systému a řeší tak potíže při ukládání do mezipaměti během používání mobilních zařízení.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Změnit dispozici dávky    | Pracovníkovi povolte zadat dispoziční kód dávky pro položky a dávky. Tato volba aktualizuje dispoziční kód, který je určen pro dávku.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Zobrazit otevřený seznam úkolů      | Zobrazení seznamu dostupných prací pro určitého uživatele. Uživatel může vybrat práci, která se má provést, a bude do ní směrován. Tento seznam je určen pro tablety velikost obrazovky 7 palců nebo vyšší. Když vyberete tuto možnost, položky nabídky **Upravit dotaz** a **Seznam polí** budou povoleny. Stránka **Upravit dotaz** vám umožňuje nastavit kritéria pro práci, která se zobrazí v seznamu. Na stránce **Seznam polí** můžete vybrat pole, které se zobrazí v pracovním seznamu. Můžete například snížit počet polí, které jsou zobrazeny a urychlit tak uživateli výběr nejvhodnější pracovní položky. Na pevné záložce **Obecné** v poli **Záznamy na stránku** můžete také vybrat, kolik pracovních záznamů na stránce se zobrazí. Pokud je vybrána možnost **Povolit uživatelům filtrovat práci podle typu transakce**, bude pracovní seznam zahrnovat ovládací prvek **Filtr práce**, který uživatel může použít pro filtrování podle typu transakce. Uživateli se zobrazí jen práce v pracovním seznamu, u které mají oprávnění k přístupu. Je nutné zkontrolovat, zda mají oprávnění pro jednu nebo více uživatelem směrovaných položek v nabídce, které podporují konkrétní typy pracovních tříd, ke kterým by měli mít přístup. Oprávnění se také ověřují při pokusu uživatele o provedení práce ze seznamu. |

## <a name="configure-menu-items-to-create-work-for-another-worker-or-process"></a>Konfigurace položek nastavení k vytvoření práce pro jiného pracovníka nebo proces
Po provedení počáteční akce pro mobilním zařízení můžete nastavit položku nabídky, která vytvoří práci pro jiného pracovníka. Pokud například jeden pracovník používá mobilního zařízení pro příjem položky, pro jiného zaměstnance se vytvoří pracovní vyskladnění. K nastavení položky nabídky, která vytvoří práci, vyberte na stránce **Položky nabídky mobilního zařízení** v poli **Režim** možnost **Práce**. V následující tabulce jsou možnosti v poli **Proces vytvoření práce** uspořádány podle typu pořadí pracovních činností.

<table>
<tbody>
<tr>
<th>Typ pořadí pracovních činností</th>
<th>Možnost</th>
<th>Popis</th>
</tr>
<tr>
<td rowspan="8">Nákupní objednávka</td>
<td>Přijetí řádku nákupní objednávky</td>
<td>Zaregistrujte příjem množství zboží za použití čísla nákupní objednávky a čísla řádku nákupní objednávky a vytvořte vyskladnění pro dalšího pracovníka.</td>
</tr>
<tr>
<td>Přijetí řádku nákupní objednávky a odložení</td>
<td>Zaregistrujte příjem množství zboží za použití čísla nákupní objednávky a čísla řádku nákupní objednávky a položky vyskladněte. Obě akce provede stejný pracovník.</td>
</tr>
<tr>
<td>Přijetí položky nákupní objednávky</td>
<td>Zaregistrujte příjem množství zboží registrací čísla nákupní objednávky a čísla položky do nákupní objednávky a vytvořte vyskladnění pro dalšího pracovníka.</td>
</tr>
<tr>
<td>Přijetí zboží nákupní objednávky a odložení</td>
<td>Zaregistrujte příjem množství zboží v nákupní objednávce za použití registrace čísla nákupní objednávky a čísla položky a položku vyskladněte. Obě akce provede stejný pracovník.</td>
</tr>
<tr>
<td>Přijetí registrační značky</td>
<td>Přijměte příchozí vytížení za pomoci ID registrační značky.</td>
</tr>
<tr>
<td>Přijetí a odložení poznávací značky</td>
<td>Přijměte a vyskladněte příchozí vytížení za pomoci ID registrační značky.</td>
</tr>
<tr>
<td>Přijetí položky nákladu</td>
<td>Zaregistrujte příjem množství pro vytížení pomocí ID vytížení a vytvořte pracovní vyskladnění pro jiného zaměstnance. Číslo položky a dimenze produktu neodpovídají příjmu z řádků nákupní objednávky.</td>
</tr>
<tr>
<td>Přijetí a odložení položky nákladu</td>
<td>Zaregistrujte příjem vytížení pomocí ID vytížení a položky vyskladněte. Číslo položky a dimenze produktu neodpovídají příjmu z řádků nákupní objednávky. Obě akce provede stejný pracovník.</td>
</tr>
<tr>
<td>Vratka</td>
<td>Příjem vratky</td>
<td>Zaregistrujte příjem množství zboží registrací čísla vrácené položky a vytvořte pracovní vyskladnění pro jiného zaměstnance.</td>
</tr>
<tr>
<td>Přijatá a odložená vratka</td>
<td>Zaregistrujte příjem množství zboží registrací čísla vrácené položky a položky vyskladněte. Obě akce provede stejný pracovník.</td>
</tr>
<tr>
<td>Objednávka převozu</td>
<td>Příjem zboží převodního příkazu</td>
<td>Zaregistrujte příjem množství zboží a vytvořte pracovní vyskladnění pro jiného zaměstnance.

<strong>Poznámka:</strong> Tuto možnost použijte pouze v případě, že položky byly dodány ze skladu, který není v rámci správy skladu povolen.</td>
</tr>
<tr>
<td>Přijetí a odložení zboží převodního příkazu</td>
<td>Zaregistrujte příjem množství zboží a položky vyskladněte. Obě akce provede stejný pracovník.

<strong>Poznámka:</strong> Tuto možnost použijte pouze v případě, že položky byly dodány ze skladu, který není v rámci správy skladu povolen.</td>
</tr>
<tr>
<td>Příjem řádku převodního příkazu</td>
<td>Zaregistrujte příjem množství zboží a vytvořte pracovní vyskladnění pro jiného zaměstnance.</td>
</tr>
<tr>
<td>Převést řádek nákupní objednávky a odložení</td>
<td>Zaregistrujte příjem množství zboží a položky vyskladněte. Obě akce provede stejný pracovník.</td>
</tr>
<tr>
<td>Výroba</td>
<td>Ohlásit jako dokončené</td>
<td>Zaregistrujte množství dokončených položek, které byly v rámci výroby dokončeny a vytvořte vyskladnění pro jiného pracovníka. Počet může odpovídat části nebo celému množství, které bylo naplánováno pro výrobu.</td>
</tr>
<tr>
<td>Ohlásit jako dokončené a odložit</td>
<td>Zaregistrujte množství dokončených položek, které byly v rámci výroby dokončeny a položky vyskladněte. Počet může odpovídat části nebo celému množství, které bylo naplánováno pro výrobu. Obě akce provede stejný pracovník.</td>
</tr>
<tr>
<td>Kanban</td>
<td>Označuje, že Kanban byl dokončen a vytvoří pracovní vyskladnění pro jiného zaměstnance.</td>
</tr>
<tr>
<td>Kanban – odložení</td>
<td>Označte dokončení Kanbanu a položky vyskladněte. Obě akce provede stejný pracovník.</td>
</tr>
<tr>
<td>Zásoby</td>
<td>Pohyb</td>
<td>Zaregistrujte, že byly položky přeneseny z jednoho místa na jiné. Pracovník určí umístění, ze kterého a do kterého byly položky přeneseny.</td>
</tr>
<tr>
<td>Karanténa</td>
<td>Změňte stav zásob na skladě v rámci registrační značky nebo umístění a upravte tak poškozené či chybějící skladové položky nedostupné.</td>
</tr>
<tr>
<td>Pohyb podle šablony</td>
<td>Přesunete položky z jednoho místa na jiné částečně automatizovaným postupem. Pracovník vybere skladové místo, ze kterého budou položky přesunuty, a aplikace Microsoft Dynamics 365 for Operations použije směrnice skladového místa pro určení místa, kam budou položky přeneseny.</td>
</tr>
<tr>
<td>Převod skladu</td>
<td>Zaregistrujte, že byly položky převedeny z jednoho skladu do jiného. Tato možnost vyžaduje, aby mohl pracovník provádět práce v obou skladech.

<strong>Poznámka:</strong> Tato položka nabídky vyžaduje výchozí deník převodu zásob s polem <strong>Využití dokladu</strong> nastaveným na <strong>Zaúčtování</strong>.</td>
</tr>
<tr>
<td>Načtení registrační značky</td>
<td>Tuto možnost použijte při prvotním nastavení skladu. Naskenujte všechny registrační značky ve všech skladových místech ve skladu. Skladové místo musí být řízeno registrační značkou. Tuto možnost nelze použít, pokud <strong>sériové číslo</strong> nebo <strong>číslo dávky</strong> je uvedeno nad <strong>skladovým místem</strong> v hierarchii rezervací zásob.</td>
</tr>
<tr>
<td>Cyklická inventura</td>
<td>Příchozí úprava</td>
<td>Navyšte množství zboží v rámci zásob. Zadejte umístění, registrační značku, položku, množství, měrnou jednotku a stav.</td>
</tr>
<tr>
<td>Odchozí úprava</td>
<td>Snižte množství zboží v rámci zásob. Zadejte umístění, registrační značku, položku, množství, měrnou jednotku a stav zásob.</td>
</tr>
<tr>
<td>Místní cyklická inventura</td>
<td>Počáteční počet ve skladovém místě. Pracovník musí provést inventuru všech položek ve skladovém místě. Pokud je po inventuře výsledek menší, než jaké je očekávané množství, je toho množství považováno za chybějící.</td>
</tr>
</tbody>
</table>

## <a name="configure-menu-items-to-process-existing-work"></a>Konfigurace položek nabídky ke zpracování existující práce
Kromě nastavení položek nabídky pro vytvoření skladové práce můžete nastavit položky nabídky pro zpracování práce, která již byla vytvořena. Nastavte pole **Režim** na **Práce** a vyberte možnost **Použít stávající práci**. Další možnosti pak budou k dispozici na **Obecné** kartu. Můžete řídit přístup k položce nabídky tak, že přiřadíte jednu nebo více tříd práce na **práce třídy** s náhledem. Pracovní třídy definují práci, kterou položka nabídky může zpracovat. Pracovní třídu lze také použít pro přidělení přístupu k určitým uživatelským rolím nebo samostatnému zpracování pro různé typy operací. V následující tabulce jsou popsány možnosti, které jsou k dispozici.

<table>




<thead>
<tr class="header">
<th>Možnost</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Žádné</td>
<td>Tato výchozí hodnota práci nezpracuje.</td>
</tr>
<tr class="even">
<td>Řízeno systémem</td>
<td>365 Microsoft Dynamics pro operace určuje druh práce, který je přiřazen pracovník a pracovník vykonává práci v uvedeném pořadí. Když vyberete tuto možnost, klepněte <strong>systém řízené práce</strong> v podokně Akce otevřete <strong>systém řízené pořadí řazení</strong> stránku, kde můžete nastavit kritéria pro práci řazení. Kritéria řazení řídí pořadí, ve kterém pracovník vykonává práci v. Můžete přidat tolik kritérií, jak požadujete.</td>
</tr>
<tr class="odd">
<td>Řízeno uživatelem</td>
<td>Pracovník vybere práci určenou k provedení a pořadí, ve kterém se bude provádět.</td>
</tr>
<tr class="even">
<td>Seskupení uživatelů</td>
<td>Pracovník ručně práci seskupí. Tato možnost je například užitečná, když pracovník chce vybrat více položek ve skladovém místě současně. Po dokončení výdeje všech požadovaných položek může pracovník tyto položky vyskladnit.</td>
</tr>
<tr class="odd">
<td>Systémové seskupení</td>
<td>Aplikace Microsoft Dynamics 365 for Operations seskupí práci pro pracovníka na základě zadaného pole. Například výdej bude seskupen, jakmile pracovník naskenuje ID dodávky, ID vytížení nebo jinou hodnotu, kterou lze propojit každá pracovní položka. Pokud tuto možnost vyberete, budou k dispozici následující pole:
<ul>
<li><strong>Pole systémového seskupení</strong> - vyberte pole, které pracovník naskenuje pro seskupení práce.</li>
<li><strong>Popisek systémového seskupení</strong> - zadejte text, který informuje pracovníka o tom, co při seskupení práce naskenovat.</li>
</ul></td>
</tr>
<tr class="even">
<td>Ověřený uživatel přesměrován</td>
<td>Pracovník vybere práci určenou k vykonání, když je práci přiřazeno větší množství, jako např. při vytížení nebo dodávce. Pracovník určuje pořadí, ve kterém jsou vybrány položky v. Pokud tuto možnost vyberete, budou k dispozici následující pole:
<ul>
<li><strong>Pole Ověřený uživatel přesměrován</strong> – vyberte pole, které pracovník naskenuje pro seskupení práce.</li>
<li><strong>Štítek Ověřený uživatel přesměrován</strong> – zadejte text, který informuje o tom, jakou práci naskenovat při seskupení práce výdeje podle systému.</li>
</ul>
Tato možnost je užitečná například po připravení více palet k nákladu. Pokud jste označili <strong>LoadId</strong> v poli <strong>Ověřený uživatel přesměrován</strong>, pracovník může vybrat libovolnou paletu, která je přidružena k nákladu. Pracovník obdrží chybovou zprávu, pokud naskenuje položku, která není přidružena k nákladu.</td>
</tr>
<tr class="odd">
<td>Výdej seskupení</td>
<td>Pracovník seskupí práci do seskupení. Seskupení umožní pracovníkům vyskladnit položky z jednoho místa v rámci několika pracovních objednávek současně.</td>
</tr>
<tr class="even">
<td>Seskupení cyklické inventury</td>
<td>Pracovník vybere zónu, fond práce nebo umístění a aplikace Microsoft Dynamics 365 for Operations přiřadí práci na základě tohoto výběru. Pokud vyberete tuto možnost, můžete také klepnout na tlačítko <strong>Cyklická inventura</strong> v podokně Akce a zadat další informace ke zobrazení nebo také určit počet opakování inventury, které pracovník musí provést v případě rozdílu v množství.</td>
</tr>
</tbody>
</table>

## <a name="additional-menu-item-options"></a>Další možnosti pro položky nabídky
Další možnosti položek nabídky jsou k dispozici na stránce **Položky nabídky mobilního zařízení**. Možnosti se liší v závislosti na tom, pro který proces konfigurujete položku nabídky. 

Následující tabulka obsahuje popis těchto možností.

<table>




<thead>
<tr class="header">
<th>Pole</th>
<th>Popis</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Umožnit rozdělení práce</td>
<td>Výběrem této možnosti umožníte uživatelům nakládat zboží v rámci pracovní zakázky do více než jedné cílové registrační značky. Tato možnost je užitečná například v případě, že je cílová registrační značka zaplněna a pracovník musí zbývající položky přidat k jiné registrační značce. Pracovník může kliknout na možnost <strong>Plno</strong>, určit tak zaplnění registrační značky a zastavit příjem práce pro tuto značku. Zobrazí se skladové místo pro vyskladněné položky a již dokončená práce výdeje bude přesunuta do nového pořadí pracovních činností. Zbývající práce výdeje pro cílovou registrační značku zůstane v původním pořadí pracovních činností.</td>
</tr>
<tr class="even">
<td>Ukotvení</td>
<td>Výběrem této možnosti můžete povolit pracovníkům určit umístění, které přepíše navrhovaná místa pro dodávku nebo nakládku. Všechna zbývající práce výdeje bude přesměrována na nové umístění. Tato možnost je užitečná například v případě, kdy se zaměstnanec chystá na vložení zboží v rámci objednávky 1 do přechodného skladového místa v překladišti 1, což ale není možné, protože předchozí vytížení zatím neopustilo skladové místo. Namísto čekání pro Dock 1 pracovní místo k dispozici, pracovník můžete rozhodnout použít pracovní místo pro Dock 2. V tomto případě pracovník přepíše navrhované pracovní umístění. Skladové místo pro všechny zbývající položky v rámci pracovní objednávky se aktualizuje a použije jako přechodné skladové místo 2. překladiště. Pokud vyberete tuto možnost, je nutné nastavit pole <strong>Ukotvil</strong>.</td>
</tr>
<tr class="odd">
<td>Ukotvil</td>
<td>Pokud používáte ukotvení, je třeba zadat, zda si přejete k ukotvení použít dodávku nebo náklad.</td>
</tr>
<tr class="even">
<td>ID šablony auditu</td>
<td>Vyberte šablonu auditu práce, kterou přerušíte pracovní proces pro tuto položku nabídky tak, aby bylo možné provést jinou operaci. Pokud je tedy například tato položka nabídky určena pro vstupní práci, šablona auditu může vyžadovat, aby pracovník ověřil teplotu v dodacím kontejneru. Místo, ve kterém je proces přerušen, je zadáno v šabloně auditu. Tento bod může být například při zahájení nebo dokončení práce, nebo když se změní jeho stav.</td>
</tr>
<tr class="odd">
<td>ID profilu seskupení</td>
<td>Vyberte profil seskupení sloužící k výdeji seskupení. Profil seskupení obsahuje nastavení, jako například, zda chcete vytvořit seskupení automaticky, názvy pozic nebo počet pracovních jednotek, které lze přiřadit, kdy má dojít ke změně seskupení na jednotlivé jednotky, nebo zda je zapotřebí ověřování. Toto pole je dostupné, pouze když je v poli <strong>Řídí</strong> vybraná možnost <strong>Výdej seskupení</strong>.</td>
</tr>
<tr class="even">
<td>Počítat nejprve celkové množství zboží</td>
<td>Výběrem této možnosti můžete požadovat po pracovníkovi, aby během inventury nejprve ověřil celkové množství. Pokud bude zjištěn rozdíl, pracovník musí poskytnout další informace, jako je například číslo registrační značky, číslo dávky, sériová čísla apod.</td>
</tr>
<tr class="odd">
<td>Vytvořit přesun</td>
<td>Výběrem této možnosti povolíte pracovníkovi vytvoření práce pro přesun, aniž by bylo nutné tuto práci provést okamžitě. Tato možnost je například užitečná, pokud kontrola kvality již byla dokončena, a kontrolor chce položku přesunout z oblasti kontroly kvality.</td>
</tr>
<tr class="even">
<td>Kód předpisu</td>
<td>Pokud chcete použít konkrétní směrnici skladového místa, vyberte kód směrnice, který je přiřazen ke směrnici skladového místa. Toto pole je k dispozici při vytváření práce a pokud je proces vytváření práce ve stavu <strong>Pohyb podle šablony</strong>.</td>
</tr>
<tr class="odd">
<td>Zakázat prahové hodnoty cyklické inventury</td>
<td>Vyberte tuto možnost, chcete-li ignorovat prahové hodnoty cyklické inventury. Pokud vyberete tuto možnost, nedojde k vytvoření cyklické inventury při překročení prahové hodnoty.</td>
</tr>
<tr class="even">
<td>Zobrazit dispoziční kód dávky</td>
<td>Chcete-li zobrazit dispoziční kódy dávky, vyberte tuto možnost. Můžete například zobrazit dispoziční kódy dávky během přijetí vrácené dávky. To umožní pracovníkům vyhodnocení stavu nebo kvality dávky a vybrat příslušný kód. Pravidla pro dispoziční kód dávky určují, zda dávka bude k dispozici i pro jiné procesy ve skladu. Pokud nevyberete tuto možnost, použije se jeden z následujících kódů dispozice dávky:
<ul>
<li>Pokud obdržíte nové číslo dávky, použije se výchozí dispoziční kód dávky zadaný pro skupinu modelů zboží.</li>
<li>Použije se dispoziční kód dávky, který je již přiřazen k dávce.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Zobrazit dispoziční kód</td>
<td>Chcete-li zobrazit dispoziční kódy, vyberte tuto možnost. Můžete například zobrazit dispoziční kódy během přijetí vráceného zboží. To umožní pracovníkům vyhodnocení stavu nebo kvality zboží a vybrat příslušný kód. Pravidla pro dispoziční kód určují, zda položky budou k dispozici i pro jiné procesy ve skladu.</td>
</tr>
<tr class="even">
<td>Zobrazit stav zásob</td>
<td>Výběrem této možnosti zobrazíte stav položek ze zásob. Další informace naleznete v tématu <a href="/inventory/inventory-statuses.md">Výhody používání stavů zásob</a>. Tato možnost je k dispozici pro všechny položky nabídky, které používají stávající práci (s výjimkou cyklické inventury).</td>
</tr>
<tr class="odd">
<td>Zobrazit přehled obrazovky výdeje</td>
<td>Výběrem této možnosti zobrazíte souhrn práce výdeje pro vybrané pořadí pracovních činností. Souhrn se zobrazí až po zpracování prvního řádku v rámci pořadí pracovních činností.</td>
</tr>
<tr class="even">
<td>Generovat poznávací značku</td>
<td>Výběrem této možnosti můžete vygenerovat jedinečnou registrační značku na základě zvolené číselné řady. Lze například vygenerovat číslo registrační značky pro položky přijaté v rámci nákupních objednávek.</td>
</tr>
<tr class="odd">
<td>Odložená skupina</td>
<td>Výběrem této možnosti můžete seskupit pracovní vyskladnění. Tato možnost je k dispozici, pokud byla práce seskupena pracovníkem nebo v aplikaci Microsoft Dynamics 365 for Operations. Pokud pracovník dokončí všechny práce výdeje ve skupině, ve stejné skupině se vytvoří pracovní vyskladnění.</td>
</tr>
<tr class="even">
<td>Typy úprav zásob</td>
<td>Vyberte typ úpravy zásob, který určuje použitý deník inventury zásob při zaúčtování množství úprav vyrovnání a také to, zda chcete odstranit rezervace. Toto pole je k dispozici pouze v případě procesů pro vytvoření práce <strong>Příchozí úprava</strong> nebo <strong>Odchozí úprava</strong>.</td>
</tr>
<tr class="odd">
<td>Přepsat číslo dávky</td>
<td>Výběrem této možnosti povolíte pracovníkům, kteří nahlásí množství pro výrobní zakázky za dokončené, aby mohli zadat číslo dávky, které se liší od čísla dávky přiřazené k výrobní zakázce.</td>
</tr>
<tr class="even">
<td>Přepsat cílovou registrační značku vozidla</td>
<td>Výběrem možnosti můžete povolit pracovníkům zadat cílové číslo registrační značky, které se liší od navrhované cílové registrační značky. Tuto možnost použijte, když se první výdej v rámci pracovní zakázky týká celého množství položky v registrační značce. Tato možnost je například užitečná při opakovaném použití palety.</td>
</tr>
<tr class="odd">
<td>Vyskladnit a zabalit</td>
<td>Výběrem této možnosti povolíte pracovníkům kombinovat práci pro prodejní objednávku nebo vytížení do podoby jedné pracovní položky. Pracovník může práci provést pouze v případě prodejní objednávky nebo vytížení. Tato možnost je například užitečná v případě, kdy je nutno navýšit množství pro prodejní objednávku po vytvoření vytížení, dodávky a práce pro prodejní objednávku. Tato možnost je k dispozici, když položka nabídky používá existující práci, a práce je řízena uživatelem nebo systémem.</td>
</tr>
<tr class="even">
<td>Žádné</td>
<td>Označte, pokud pracovník musí ve skladovém místě vyskladnit nejprve nejstarší dávku. Existují tyto možnosti:
<ul>
<li><strong>Poznámka</strong> – Pracovník může ve skladovém místě vyskladnit jakoukoli dávku. Pracovník neobdrží žádnou zprávu.</li>
<li><strong>Varovat</strong> – Pracovník můžete ve skladovém místě vyskladnit jakoukoli dávku, ale pokud není dávka nejstarší, zobrazí se mu varovná zpráva.</li>
<li><strong>Vynutit</strong> – Pracovník musí ve skladovém místě vyskladnit nejstarší dávku. Pracovník obdrží chybovou zprávu, pokud dávka není nejstarší dávkou. <strong>Poznámka:</strong> Tato možnost je relevantní pouze v případě, kdy je v hierarchii rezervace přiřazené k položce <strong>Číslo dávky</strong> nižší než <strong>Umístění</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Tisk etikety</td>
<td>Výběrem této možnosti povolíte pracovníkům vytisknout štítky registračních značek.</td>
</tr>
<tr class="even">
<td>Pole systémového seskupení</td>
<td>Vyberte pole, které určuje způsob, jak aplikace Microsoft Dynamics 365 for Operations seskupí práci výdeje pro pracovníka. Pokud například vyberete pole <strong>ShipmentId</strong>, pracovník naskenuje ID dodávky pro seskupení práce výdeje. Všechna práce pro dodávku bude přiřazena pracovníkovi. Toto pole vyžaduje, abyste vytvořili položku nabídky pro stávající práci, která je seskupena podle systému. Musíte také zadat text do pole <strong>Popisek systémového seskupení</strong> a informovat tak pracovníka o tom, co naskenovat.</td>
</tr>
<tr class="odd">
<td>Popisek systémového seskupení</td>
<td>Zadejte text, který informuje o tom, jakou práci naskenovat při seskupení práce výdeje v aplikaci Microsoft Dynamics 365 for Operations. Používáte-li například pole <strong>ShipmentId</strong> pro seskupení práce výdeje podle dodávky, měli byste do pole zadat <strong>ID dodávky</strong>. Toto pole vyžaduje, abyste vytvořili položku nabídky pro stávající práci, která je seskupena podle systému. Je nutné zaškrtnout pole definující seskupení v poli <strong>Pole systémového seskupení</strong>.</td>
</tr>
<tr class="even">
<td>Použít výchozí data</td>
<td>Vyberte tuto možnost, chcete-li zpřístupnit tlačítko <strong>Výchozí data</strong> v podokně Akce umožňující zvolit pole a zobrazit data, která pracovník obvykle potřebuje ve své každodenní práci. Tato možnost je například užitečná, když pracovník často provádí vyskladnění položek ze stejného místa. Můžete vybrat pole <strong>Z umístění</strong> a zobrazit standardně skladové místo.</td>
</tr>
<tr class="odd">
<td>Pole Ověřený uživatel přesměrován</td>
<td>Vyberte pole, které pracovník naskenuje pro seskupení práce. Pokud vyberete například možnost <strong>LoadId</strong>, pracovník může vyskladnit jakoukoli práci, která je přidružena k vybranému nákladu. Musíte také zadat text do pole <strong>Štítek Ověřený uživatel přesměrován</strong> a informovat tak pracovníka o tom, co naskenovat.</td>
</tr>
<tr class="even">
<td>Štítek Ověřený uživatel přesměrován</td>
<td>Zadejte text, který informuje o tom, jakou práci naskenovat při seskupení práce výdeje podle ověřeného pole definovaného uživatelem. Používáte-li například pole <strong>LoadId</strong> pro seskupení práce výdeje podle vytížení, měli byste do pole zadat <strong>ID vytížení</strong>.</td>
</tr>
<tr class="odd">
<td>Kód šablony práce</td>
<td>Vyberte šablonu práce, která v procesu vytvoří práci. Například pokud obdržíte zboží pro nákupní objednávku, zaskladnění práce bude vygenerován na základě šablony práce. Pokud nevyberete šablonu práce, 365 Microsoft Dynamics pro operace přiřadí šablonu na základě kritérií dotazu. Další informace týkající se šablon práce naleznete v tématu <a href="control-warehouse-location-directives.md">Řízení práce ve skladu pomocí šablon práce a směrnic umístění</a>.</td>
</tr>
</tbody>
</table>

## <a name="require-workers-to-confirm-the-product-location-or-quantity-when-they-pick-items"></a>Požadovat po zaměstnancích potvrzení výrobku, umístění a množství při vyskladňování zboží
Můžete nastavit potvrzení práce vyžadující po pracovníkovi, aby při práci ve skladu pomocí mobilního zařízení zaregistroval skladové místo nebo množství. Potvrzení práce pomáhá zajistit, aby byl pracovník na správném skladovém místě, nebo aby zpracoval správné množství položek. Můžete také povolit aplikaci Microsoft Dynamics 365 for Operations automaticky potvrdit registraci pracovníka. Pokud zapnete automatické potvrzení, nelze současně požadovat potvrzení skladového místa nebo množství. Pracovní potvrzení bude také zahrnovat produkty a varianty produktů. Kromě toho můžete zaregistrovat potvrzení naskenováním čárového kódu. Pro potvrzení produktů a variant produktů je nutné zadat ID produktu nebo varianty produktu. Může se jednat o ID produktu, ID vyhledávání produktu, externí ID, GTIN nebo čárový kód. Po zadání ID nebo naskenování čárového kódu se v mobilním zařízení zobrazí dimenze pro varianty produktu. 

Následující tabulka popisuje různé typy práce, se kterým můžete použít potvrzení práce.

| Možnost                 | Popis                                                                |
|------------------------|----------------------------------------------------------------------------|
| Vybrat                   | Vyžadování potvrzení při vyskladnění položek.                                |
| Vložit                    | Vyžadování potvrzení při distribuci položek do skladového místa.                     |
| Inventura               | Vyžadování potvrzení při cyklické inventuře.                                |
| Množství úprav            | Vyžadování potvrzení při úpravě množství zásob.               |
| Vlastní                 | Vyžadování potvrzení pro vlastní práce.                                      |
| Karanténa             | Vyžadování potvrzení při přesunutí položek do karantény.                   |
| Sestavení registrační značky vozidla | Vyžadování potvrzení při konsolidaci položek k sestavení registrační značky. |
| Tisk                  | Vyžadování potvrzení při tisku štítků registračních značek.                |
| Změna stavu          | Vyžadování potvrzení při změně stavu zásob.              |

**Poznámka:** Můžete požádat o potvrzení produktu pouze pro výdej a vložení typů práce.

<a name="see-also"></a>Viz také
--------

[Nastavení displeje mobilního zařízení skladu](change-warehouse-mobile-device-displays.md)

[Nastavit položku nabídky mobilního zařízení pro dokončení práce typ nákupní objednávky (úkol guide)](https://ax.help.dynamics.com/en/wiki/set-up-a-mobile-device-menu-item-for-completing-work-of-type-purchase-order/)

[Nastavit položku nabídky mobilního zařízení k registraci přijatého zboží (úkol guide)](https://ax.help.dynamics.com/en/wiki/set-up-a-mobile-device-menu-item-to-register-received-items/)



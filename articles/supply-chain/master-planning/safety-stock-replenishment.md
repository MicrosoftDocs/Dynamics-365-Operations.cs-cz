---
title: Splnění rezervních zásob položek
description: Toto téma popisuje splnění rezervních zásob a nastavení množství rezervních zásob pro položky.
author: roxanadiaconu
ms.date: 11/27/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqSafetyKey, ReqItemTableSetup, ReqItemJournalName, ReqItemTable, EcoResProductDetailsExtended, ReqSafetyKeyDefaultDataWizard
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: kamaybac
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 89783eec7c6dea663b97ba50b72b4ee499d6044443bbb7e8df29ebdd16bc6c97
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6748756"
---
# <a name="safety-stock-fulfillment-for-items"></a>Splnění rezervních zásob položek

[!include [banner](../includes/banner.md)]

Rezervní zásoby označuje dodatečné množství položky uložené ve skladu za účelem snížení rizika, že položka nebude na skladě. Rezervní zásoby se používají jako vyrovnávací zásoby v případě příchozích prodejních objednávek, kdy dodavatel nemůže doručit další položky ke splnění požadovaného data expedice odběrateli. Při použití rezervních zásob pro splnění prodejní objednávky bude snížena rezervní zásoba. Můžete použít hlavní plánování k automatickému vyrovnání zpět na úroveň rezervních zásob.    

## <a name="set-up-safety-stock-levels-for-items"></a>Nastavení úrovní rezervních zásob pro položky

Rezervní zásoby jsou nastaveny jako součást disponibility položky na stránce **Disponibilita položky** pod možnostmi **Uvolněné produkty** > **Plán** > **Disponibilita**.

V poli **Minimum** zadejte úroveň rezervních zásob, které chcete pro položku udržet. Hodnota je vyjádřena ve skladových jednotkách. Ponecháte-li toto pole prázdné, bude výchozí hodnotou nula. Toto pole bude dostupné, vyberete-li ze seznamu **Kód disponibility** možnost **Období**, **Požadavek** nebo **Min/Max**. Limit úrovně skladu se vztahuje na dostupné zásoby, což znamená, že rezervace a označení mohou spustit doplnění rezervních zásob dříve, než přejde fyzické množství pod zadanou minimální úrovně.

> [!NOTE]
> Nejprve je nutné definovat všechny ostatní plánované dimenze disponibility a teprve poté lze definovat pole **Minimum**. To zabraňuje použití neplatného záznamu během hlavního plánování. K takové situaci může dojít například tehdy, pokud je skupina dimenzí rozšířena o další plánovanou dimenzi disponibility, pro kterou nejsou dosud definovány hodnoty minimálního a maximálního skladového množství.

Pomocí klíčů minima se můžete přizpůsobit sezónním výkyvům v poptávce. V období mimo sezónu můžete například snížit minimální úroveň zásob položky a v následujících měsících ji postupně zvyšovat. Klíč minima vytvoříte přechodem na možnosti **Hlavní plánování** > **Nastavení** > **Disponibilita** > **Klíče minima/maxima**. Pro přizpůsobení úrovně rezervních zásob podle sezónnosti určíte klíč minima v poli **Klíč minima** na stránce **Disponibilita položky**. 

## <a name="example-minimum-key"></a>Příklad: Klíč minima
Pokud chcete nastavit klíč minima, který odpovídá za zvýšenou sezónní poptávku během letních a jarních měsíců, přejděte na **Hlavní plánování** > **Nastavení** > **Disponibilita** > **Klíče minima/maxima** a proveďte následující kroky.

1. Vytvořte 12 řádků a přiřaďte číslo od 1 do 12 řádkům v poli **Změna**.
2. V poli **Jednotka** pak vyberte možnost **Měsíce**.
3. Do pole **Koeficient** zadejte hodnoty popsané v následující tabulce.

|Spojnicový|Zadejte tuto hodnotu|Výsledek|
|---|---|---|
|1–3|1|Minimální zásoby jsou založeny na nastavení pro měsíce leden až březen na stránce **Disponibilita položky**.|
|4-5|2|Hodnota minimálních zásob bude pro měsíce duben až květen vynásobena koeficientem 2.|
|6-8|2,5|Hodnota minimálních zásob bude pro měsíce červen až srpen vynásobena koeficientem 2,5.|
|9-12|1|Pro hodnotu minimálních zásob bude pro měsíce září až prosinec opět použito nastavení na stránce **Disponibilita položky**.|

Pokud je kód disponibility **Min/Max**, je také možné určit **Maximální** skladové množství, které chcete udržovat pro položku. Hodnota je rovněž vyjádřena ve skladových jednotkách. Pokud předpokládané dostupné zásoby klesnou pod minimální množství, vytvoří hlavní plánování plánovanou objednávku pro plnění všech otevřených požadavků a doplní zásoby na určené maximální množství. Stejně jako když nastavujete **Minimum**, je nutné definovat všechny ostatní plánované dimenze disponibility a teprve poté lze definovat hodnotu pole **Maximum**.

## <a name="example-minmax-coverage-code"></a>Příklad: Kód disponibility Min/Max
Minimální množství je 10 a maximální množství je 15. Aktuální zásoby na skladě jsou 4. Z toho vyplývá požadavek na minimální množství 6. Protože je však maximální množství 15 kusů, hlavní plánování vytvoří plánovanou objednávku na 11 položek.

Pro položky, které následují po sezónních požadavcích, můžete udržovat odlišné maximální úrovně. Proto je třeba definovat **Klíče maxima** přechodem na možnosti **Hlavní plánování** > **Nastavení** > **Disponibilita** > **Klíče minima/maxima**. Vyplňte pole **Klíč maxima** na stránce **Disponibilita položky**. Informace o úrovních rezervních zásob definované pomocí klíčů minima na kartě **Min/Max** můžete zobrazit na stránce **Disponibilita položky**. Je nutné, abyste se ujistili, že po určitou dobu budou minimální a maximální hodnoty synchronizovány.

## <a name="safety-stock-fulfillment"></a>Splnění rezervních zásob 

Parametr **Splnit minimum** umožňuje výběr data nebo časového období, pro které musí úroveň zásob splňovat množství uvedené v poli **Minimum**. Toto pole bude dostupné, vyberete-li ze seznamu **Kód disponibility** možnost **Období**, **Požadavek** nebo **Min/Max**.

Pokud jsou použity **Klíče minima**, zvolte zaškrtávací políčko **Období minima** pro splnění minimální úrovně zásob pro všechna období nastavená v klíči minima. Pokud odškrtnete políčko, bude minimální úroveň zásob splněna pouze pro aktuální období.

Následující scénář zobrazuje fungování tohoto parametru a rozdíly mezi jeho hodnotami.

> [!NOTE]
> Pro všechny ilustrace v tomto tématu představuje osa X zásoby, osa Y představuje dny, pruhy představují úroveň zásob, šipky představují transakce, jako například řádky prodejní objednávky, řádky nákupní objednávky nebo plánované objednávky.

[![Běžný scénář plnění pojistných zásob.](./media/Scenario1.png)](./media/Scenario1.png)
Parametr **Minimum splnění** může mít následující hodnoty:
### <a name="todays-date"></a>Dnešní datum 
Určené minimální množství je dosaženo v den spuštění hlavního plánování. Systém se pokusí naplnit limit rezervních zásob co nejdříve, i v případě, že to může být nereálné z důvodu doby realizace. 
[![Požadavek k dnešnímu dni.](./media/TodayReq.png)](./media/TodayReq.png)
Plánovaná objednávka P1 je vytvořena pro dnešní den, aby doplnila dostupné zásoby nad úroveň rezervních zásob k tomuto datu. Řádky prodejní objednávky S1 až S3 nadále snižují úroveň zásob. Plánované objednávky P2 až P4 jsou vygenerovány hlavním plánováním tak, aby se úroveň skladu vrátila na rezervní limit po každém požadavku prodejní objednávky.
Při použití kódu disponibility **Požadavek** se vytvoří více plánovaných objednávek. Vždy je vhodné použít buď disponibilitu **Období** nebo **Min/Max** pro často poptávané položky a materiály za účelem seskupení doplnění. Následující obrázek znázorňuje příklad kódu disponibility **Období**.
[![Období. Dnešní datum.](./media/TodayPeriod.png)](./media/TodayPeriod.png)
Následující obrázek znázorňuje příklad kódu disponibility **Min/max**.
[![MinMax. Dnešní datum.](./media/TodayMinMax.png)](./media/TodayMinMax.png)
### <a name="todays-date--procurement-time"></a>Dnešní datum a čas pořízení 
Určené minimální množství je dosaženo v den spuštění hlavního plánování plus doba realizace nákupu nebo výroby. Tento čas zahrnuje případnou bezpečné marže. Existuje-li pro položku obchodní smlouva a současně je zaškrtnuto políčko **Najít obchodní dohody** na stránce **Parametry hlavního plánování**, nebude brána v úvahu doba realizace dodávky uvedená v obchodní smlouvě. Doba realizace je převzata z položky nebo z nastavení disponibility položky.
Tento režim plnění vytvoří plány s menším zpožděním a s méně plánovanými objednávkami, bez ohledu na skupinu disponibility nastavenou pro položku. Následující obrázek znázorňuje výstup plánu, pokud je kód disponibility **Požadavek** nebo **Období**.  
[![Požadavek. Období Dnešní datum a doba realizace.](./media/TodayPLTReq.png)](./media/TodayPLTReq.png)
Následující obrázek znázorňuje výstup plánu, pokud je kód disponibility **Min./max.**  
[![MinMax. Dnešní datum a doba realizace.](./media/TodayPLTMinMax.png)](./media/TodayPLTMinMax.png)
### <a name="first-issue"></a>První výdej 
Zadané minimální množství je dosaženo v den přechodu dostupných zásob pod minimální úroveň, jak je uvedeno na následujícím obrázku. I v případě, že jsou dostupné zásoby pod minimální úrovni k datu, kdy bude spuštěno hlavní plánování, **První vydání** se ho nepokusí pokrýt, dokud nepřijde další požadavek.
Následující obrázek znázorňuje příklad kódu disponibility **Požadavek**.
[![Plánování položky s kódem disponibility **Požadavek** a plněním **První vydání**.](./media/FirstIssueReq.png)](./media/FirstIssueReq.png)
Následující obrázek znázorňuje příklad kódu disponibility **Období**.
[![Plánování položky s kódem disponibility **Období** a plněním **První vydání**.](./media/FirstIssuePeriod.png)](./media/FirstIssuePeriod.png)
Následující obrázek znázorňuje příklad kódu disponibility **Min/max**.
[![Plánování položky s kódem disponibility **MinMax** a plněním **První vydání**.](./media/FirstIssueMinMax.png)](./media/FirstIssueMinMax.png)
V den spuštění hlavního plánování, pokud jsou dostupné zásoby již pod limitem rezervních zásob, spustí **Dnešní datum** a **Dnešní datum a čas pořízení** doplnění okamžitě. **První vydání** počká na položku, dokud nedojde k další výdejové transakci, jako je například prodejní objednávka a požadavek na řádek kusovníku, a poté spustí doplnění v den této transakce. V den spuštění hlavního plánování, pokud nejsou dostupné zásoby pod limitem rezervních zásob, možnosti **Dnešní datum** a **První vydání** poskytnou přesně stejný výsledek, jako je znázorněno na obrázku níže. 

[![NotUnderLimit.](./media/ReqFirstIssue.png)](./media/ReqFirstIssue.png)
V den spuštění hlavního plánování, pokud nejsou dostupné zásoby pod limitem rezervních zásob, možnost **Dnešní datum a čas pořízení** poskytne následující výsledek, protože odloží plnění až do konce doby realizace pořízení.
![Plánování položky s kódem disponibility **Požadavek** a plněním **První vydání**.](./media/ReqTodayLT.png)
### <a name="coverage-time-fence"></a>Ochranná doba disponibility
Nastavené minimální množství je dosaženo během časového období uvedeného v poli **Ochranná doba disponibility**. Tato možnost je užitečná, když hlavní plánování neumožňuje použití dostupných zásob pro skutečné objednávky, jako jsou například prodejní objednávky nebo převody, při pokusu o udržení úrovně rezervních zásob. V dalších verzích však tento způsob doplnění nebude již zapotřebí a tato možnost bude zastaralá.
## <a name="plan-safety-stock-replenishment-for-first-expired-first-out-fefo-items"></a>Plánování doplnění rezervních zásob pro položky FEFO
Kdykoli v čase se pro rezervní zásoby použije příjem na sklad s nejpozdějším datem vypršení, aby se umožnilo splnění skutečné poptávky, jako jsou řádky prodejní objednávky nebo kusovníku, v FEFO pořadí.
Abychom si vysvětlili, jak to funguje, předpokládejme následující situaci.
[![FEFOScenario.](./media/FEFOScenario.png)](./media/FEFOScenario.png)
Při spuštění plánování se pokryje první prodejní objednávka ze stávajících zásob na skladě a další nákupní objednávka pro zbývající množství.
[![FEFO1.](./media/FEFO1.png)](./media/FEFO1.png)
Vytvoří se plánovaná objednávka, aby se zajistilo, že jsou dostupné zásoby doplněny zpět na limit rezervních zásob.
[![FEFO2.](./media/FEFO2.png)](./media/FEFO2.png)
Při plánování druhé prodejní se použije pro pokrytí tohoto množství dříve vytvořená plánovaná objednávka pokrývající limit rezervních zásob. Z tohoto důvodu se rezervní zásoby stále vrací.
[![FEFO3.](./media/FEFO3.png)](./media/FEFO3.png)
Nakonec se vytvoří jiná plánovaná objednávka k pokrytí rezervních zásob.
[![FEFO4.](./media/FEFO4.png)](./media/FEFO4.png)
Všechny dávky vyprší odpovídajícím způsobem a plánované objednávky budou vytvořeny k doplnění rezervních zásob po jejich vypršení.

## <a name="how-master-planning-handles-the-safety-stock-constraint"></a>Jak hlavní plánování zachází s omezením rezervních zásob

Rezervní zásoby jsou sledovány v systému jako typ požadavku, stejně jako prodejní řádky nebo požadavky na kusovníku. Řádek požadavku na rezervní zásoby můžete vidět na stránce **Požadavky netto**, pokud odstraníte výchozí filtr ve sloupci **Typ požadavku**.

Plnění transakce požadavku na rezervní zásoby se sníží priorita, pokud systém zjistí, že to způsobí zpoždění v plnění skutečné poptávky, jako jsou prodejní řádky, řádky kusovníku, požadavky na převody nebo řádky prognózy poptávky. V opačném případě se ujistěte se, že dostupné zásoby jsou nad množstvím rezervních zásob a mají stejnou prioritu jako ostatní typy poptávky. To zajišťuje, že pro skutečné transakce nebude docházet ke zpoždění, a pomáhá předcházet přeplnění nebo předčasnému doplnění rezervních zásob.

Ve fázi disponibility hlavního plánování již doplnění rezervních zásob nemá sníženou prioritu. Zásoby na skladě lze použít před jakýmikoliv jinými typy poptávky. Během výpočtu zpoždění se přidá nová logika k procházení opožděnými prodejními řádky, požadavky na řádek kusovníku a všemi ostatními typy poptávky, za účelem určení, zda mohou být doručeny včas, za předpokladu použití rezervních zásob. Pokud systém identifikuje, že použití rezervních zásob může minimalizovat zpoždění, řádky prodeje nebo řádky kusovníku nahradí jejich počáteční disponibilitu rezervními zásobami a systém místo toho spustí doplnění rezervních zásob.

Pokud pro výpočet zpoždění není nastaven plán nebo položka, bude mít omezení rezervních zásob stejnou prioritu jako ostatní typy poptávky. To znamená, že existuje rezerva zásob na skladě a dalších dostupných zásob před jinými typy poptávky.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
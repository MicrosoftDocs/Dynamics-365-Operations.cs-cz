---
title: Splnění rezervních zásob položek
description: Toto téma popisuje splnění rezervních zásob a nastavení množství rezervních zásob pro položky.
author: thethehelga
ms.date: 8/23/2021
ms.topic: article
ms.search.form: ReqSafetyKey, ReqItemTableSetup, ReqItemJournalName, ReqItemTable, EcoResProductDetailsExtended, ReqSafetyKeyDefaultDataWizard
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-oldolg
ms.dyn365.ops.version: 7.2999999999999998
ms.search.validFrom: 2017-12-31
ms.openlocfilehash: 28f902c589cd80f1c34dc2758232548309db9aca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474621"
---
# <a name="safety-stock-fulfillment-for-items"></a>Splnění rezervních zásob položek

[!include [banner](../includes/banner.md)]

Rezervní zásoby označuje dodatečné množství položky uložené ve skladu za účelem snížení rizika, že položka nebude na skladě. Rezervní zásoby se používají jako vyrovnávací zásoby v případě příchozích prodejních objednávek, kdy dodavatel nemůže doručit další položky ke splnění požadovaného data expedice odběrateli. Při použití rezervních zásob pro splnění prodejní objednávky bude snížena rezervní zásoba. Můžete použít hlavní plánování k automatickému vyrovnání zpět na úroveň rezervních zásob.

## <a name="set-up-safety-stock-levels-for-items"></a>Nastavení úrovní rezervních zásob pro položky

Rezervní zásoby jsou nastaveny jako součást disponibility položky na stránce **Disponibilita položky** pod možnostmi **Uvolněné produkty \> Plán \> Disponibilita**.

V poli **Minimum** zadejte úroveň rezervních zásob, které chcete pro položku udržet. Hodnota je vyjádřena ve skladových jednotkách. Ponecháte-li toto pole prázdné, bude výchozí hodnotou nula. Toto pole bude dostupné, vyberete-li ze seznamu **Kód disponibility** možnost **Období**, **Požadavek** nebo **Min/Max**. Limit úrovně skladu se vztahuje na dostupné zásoby, což znamená, že rezervace a označení mohou spustit doplnění rezervních zásob dříve, než přejde fyzické množství pod zadanou minimální úrovně.

> [!NOTE]
> Nejprve je nutné definovat všechny ostatní plánované dimenze disponibility a teprve poté lze definovat pole **Minimum**. To zabraňuje použití neplatného záznamu během hlavního plánování. K takové situaci může dojít například tehdy, pokud je skupina dimenzí rozšířena o další plánovanou dimenzi disponibility, pro kterou nejsou dosud definovány hodnoty minimálního a maximálního skladového množství.

Pomocí klíčů minima se můžete přizpůsobit sezónním výkyvům v poptávce. V období mimo sezónu můžete například snížit minimální úroveň zásob položky a v následujících měsících ji postupně zvyšovat. Klíč minima vytvoříte přechodem na možnosti **Hlavní plánování \> Nastavení \> Disponibilita \> Klíče minima/maxima**. Pro přizpůsobení úrovně rezervních zásob podle sezónnosti určíte klíč minima v poli **Klíč minima** na stránce **Disponibilita položky**.

## <a name="example-minimum-key"></a>Příklad: Klíč minima

Následující postup je příkladem, který ukazuje, jak nastavit minimální klíč, který odpovídá zvýšené sezónní poptávce během jarních a letních měsíců.

1. Přejděte na **Hlavní plánování \> Nastavení \> Disponibilita \> Minimální/maximální klíče**.
1. Vyberte možnost **Nová** k vytvoření minimálního/maximálního klíče.
1. Do pole **Minimální nebo maximální klíč** zadejte identifikátor klíče. Do pole **Název** zadejte název klíče.
1. Nastavte možnosti **Použít datum účinnosti** na *Ano* a nechte pole **Datum účinnosti** prázdné, aby byl klíč platný od prvního dne aktuálního roku.

    > [!NOTE]
    > Kombinace nastavení **Použít datum účinnosti** a **Datum účinnosti** definuje datum, od kterého je klíč platný.
    >
    > - Když je možnost **Použít datum účinnosti** nastavena na *Ne*, klíč je platný od aktuálního data nebo systémového data.
    > - Když je možnost **Použít datum účinnosti** nastavena na *Ano*, klíč je platný od data definovaného v poli **Datum účinnosti**.

1. V části **Období** vytvořte 12 řádků a nastavte pro ně následující hodnoty:

    - **Změna** - Každému řádku přiřaďte jedinečné číslo od 1 do 12. Toto pole označuje přírůstkovou změnu jednotky času, která je definována polem **Jednotka**.
    - **Jednotka** - Vyberte *Měsíce* pro každý řádek.
    - **Od data**, **Do data**, a **Měsíc** - Tato pole se automaticky nastavují na základě nastavení **Změna** a **Jednotka**. Měsíční období začíná prvním dnem aktuálního roku.
    - Do pole **Faktor** zadejte hodnoty popsané v následující tabulce. Toto pole definuje faktor, kterým chcete vynásobit minimální zásoby.

        | Řádek (změna) | Koeficient | Výsledek |
        |---|---|---|
        | 1–3 | 1 | Minimální zásoby jsou založeny na nastavení pro měsíce leden až březen na stránce **Disponibilita položky**. |
        | 4–5 | 2 | Hodnota minimálních zásob bude pro měsíce duben až květen vynásobena koeficientem 2. |
        | 6–8 | 2.5 | Hodnota minimálních zásob bude pro měsíce červen až srpen vynásobena koeficientem 2,5. |
        | 9–12 | 1 | Pro hodnotu minimálních zásob bude pro měsíce září až prosinec opět použito nastavení na stránce **Disponibilita položky**. |

    Vaše nastavení by se nyní mělo podobat nastavení na následujícím obrázku.

    ![Minimální nebo maximální období klíčů.](media/min-max-key-periods.png "Minimální nebo maximální období klíčů")

> [!NOTE]
> Můžete také použít průvodce k vytvoření a nastavení klíče minima/maxima. Na stránce **Minimální nebo maximální klíče** v podokně akcí vyberte **Průvodce** k otevření průvodce **Minimální/maximální klíče**. Průvodce vás krok za krokem provede procesem vytváření a nastavování minima/maxima.

Pokud je kód disponibility *Min/Max*, je také možné určit maximální skladové množství, které chcete udržovat pro položku. Hodnota je rovněž vyjádřena ve skladových jednotkách. Pokud předpokládané dostupné zásoby klesnou pod minimální množství, vytvoří hlavní plánování plánovanou objednávku pro plnění všech otevřených požadavků a doplní zásoby na určené maximální množství. Stejně jako když nastavujete minimální skladové množství, je nutné definovat všechny ostatní plánované dimenze disponibility a teprve poté lze definovat hodnotu pole **Maximum**.

## <a name="example-minmax-coverage-code"></a>Příklad: Kód disponibility Min/Max

Minimální množství je 10 a maximální množství je 15. Aktuální zásoby na skladě jsou 4. Z toho vyplývá požadavek na minimální množství 6. Protože je však maximální množství 15 kusů, hlavní plánování vytvoří plánovanou objednávku na 11 položek.

Pro položky, které následují po sezónních požadavcích, můžete udržovat odlišné maximální úrovně. Proto je třeba definovat **Klíče maxima** přechodem na možnosti **Hlavní plánování \> Nastavení \> Disponibilita \> Klíče minima/maxima**. Vyplňte pole **Klíč maxima** na stránce **Disponibilita položky**. Informace o úrovních rezervních zásob definované pomocí klíčů minima na kartě **Min/Max** můžete zobrazit na stránce **Disponibilita položky**. Je nutné, abyste se ujistili, že po určitou dobu budou minimální a maximální hodnoty synchronizovány.

## <a name="safety-stock-fulfillment"></a>Splnění rezervních zásob

Parametr **Splnit minimum** umožňuje výběr data nebo časového období, pro které musí úroveň zásob splňovat množství uvedené v poli **Minimum**. Toto pole bude dostupné, vyberete-li ze seznamu **Kód disponibility** možnost **Období**, **Požadavek** nebo **Min/Max**.

Pokud jsou použity **Klíče minima**, zvolte zaškrtávací políčko **Období minima** pro splnění minimální úrovně zásob pro všechna období nastavená v klíči minima. Pokud odškrtnete políčko, bude minimální úroveň zásob splněna pouze pro aktuální období.

Následující scénář zobrazuje fungování tohoto parametru a rozdíly mezi jeho hodnotami.

> [!NOTE]
> Pro všechny ilustrace v tomto tématu představuje osa X zásoby, osa Y představuje dny, pruhy představují úroveň zásob, šipky představují transakce, jako například řádky prodejní objednávky, řádky nákupní objednávky nebo plánované objednávky.

[![Běžný scénář plnění pojistných zásob.](media/Scenario1.png)](media/Scenario1.png)

Parametr **Minimum splnění** může mít následující hodnoty:

### <a name="todays-date"></a>Dnešní datum

Určené minimální množství je dosaženo v den spuštění hlavního plánování. Systém se pokusí naplnit limit rezervních zásob co nejdříve, i v případě, že to může být nereálné z důvodu doby realizace.

[![Požadavek k dnešnímu dni.](media/TodayReq.png)](media/TodayReq.png)

Plánovaná objednávka P1 je vytvořena pro dnešní den, aby doplnila dostupné zásoby nad úroveň rezervních zásob k tomuto datu. Řádky prodejní objednávky S1 až S3 nadále snižují úroveň zásob. Plánované objednávky P2 až P4 jsou vygenerovány hlavním plánováním tak, aby se úroveň skladu vrátila na rezervní limit po každém požadavku prodejní objednávky.

Při použití kódu disponibility **Požadavek** se vytvoří více plánovaných objednávek. Vždy je vhodné použít buď disponibilitu **Období** nebo **Min/Max** pro často poptávané položky a materiály za účelem seskupení doplnění. Následující obrázek znázorňuje příklad kódu disponibility **Období**.

[![Období. Dnešní datum.](media/TodayPeriod.png)](media/TodayPeriod.png)

Následující obrázek znázorňuje příklad kódu disponibility **Min/max**.

[![Min/Max. Dnešní datum.](media/TodayMinMax.png)](media/TodayMinMax.png)

### <a name="todays-date--procurement-time"></a>Dnešní datum a čas pořízení

Určené minimální množství je dosaženo v den spuštění hlavního plánování plus doba realizace nákupu nebo výroby. Tento čas zahrnuje případnou bezpečné marže. Existuje-li pro položku obchodní smlouva a současně je zaškrtnuto políčko **Najít obchodní dohody** na stránce **Parametry hlavního plánování**, nebude brána v úvahu doba realizace dodávky uvedená v obchodní smlouvě. Doba realizace je převzata z položky nebo z nastavení disponibility položky.

Tento režim plnění vytvoří plány s menším zpožděním a s méně plánovanými objednávkami, bez ohledu na skupinu disponibility nastavenou pro položku.

Následující obrázek znázorňuje výstup plánu, pokud je kód disponibility **Požadavek** nebo **Období**.

[![Požadavek. Období Dnešní datum a doba realizace.](media/TodayPLTReq.png)](media/TodayPLTReq.png)

Následující obrázek znázorňuje výstup plánu, pokud je kód disponibility **Min./max.**

[![Min/Max. Dnešní datum a doba realizace.](media/TodayPLTMinMax.png)](media/TodayPLTMinMax.png)

### <a name="first-issue"></a>První výdej

Zadané minimální množství je dosaženo v den přechodu dostupných zásob pod minimální úroveň, jak je uvedeno na následujícím obrázku. I v případě, že jsou dostupné zásoby pod minimální úrovni k datu, kdy bude spuštěno hlavní plánování, **První vydání** se ho nepokusí pokrýt, dokud nepřijde další požadavek.

Následující obrázek znázorňuje příklad kódu disponibility **Požadavek**.

[![Plánování položky s kódem disponibility Požadavek a plněním První vydání.](media/FirstIssueReq.png)](media/FirstIssueReq.png)

Následující obrázek znázorňuje příklad kódu disponibility **Období**.

[![Plánování položky s kódem disponibility Období a plněním První vydání.](media/FirstIssuePeriod.png)](media/FirstIssuePeriod.png)

Následující obrázek znázorňuje příklad kódu disponibility **Min/max**.

[![Plánování položky s kódem disponibility MinMax a plněním První vydání.](media/FirstIssueMinMax.png)](media/FirstIssueMinMax.png)

V den spuštění hlavního plánování, pokud jsou dostupné zásoby již pod limitem rezervních zásob, spustí **Dnešní datum** a **Dnešní datum a čas pořízení** doplnění okamžitě. **První vydání** počká na položku, dokud nedojde k další výdejové transakci, jako je například prodejní objednávka a požadavek na řádek kusovníku, a poté spustí doplnění v den této transakce.

V den spuštění hlavního plánování, pokud nejsou dostupné zásoby pod limitem rezervních zásob, možnosti **Dnešní datum** a **První vydání** poskytnou přesně stejný výsledek, jako je znázorněno na následujícím obrázku.

[![Není pod limitem.](media/ReqFirstIssue.png)](media/ReqFirstIssue.png)

V den spuštění hlavního plánování, pokud nejsou dostupné zásoby pod limitem rezervních zásob, možnost **Dnešní datum a čas pořízení** poskytne následující výsledek, protože odloží plnění až do konce doby realizace pořízení.

![Plnění odloženo na konec dodací lhůty.](media/ReqTodayLT.png)

### <a name="coverage-time-fence"></a>Ochranná doba disponibility

Nastavené minimální množství je dosaženo během časového období uvedeného v poli **Ochranná doba disponibility**. Tato možnost je užitečná, když hlavní plánování neumožňuje použití dostupných zásob pro skutečné objednávky, jako jsou například prodejní objednávky nebo převody, při pokusu o udržení úrovně rezervních zásob. V dalších verzích však tento způsob doplnění nebude již zapotřebí a tato možnost bude zastaralá.

## <a name="plan-safety-stock-replenishment-for-first-expired-first-out-fefo-items"></a>Plánování doplnění rezervních zásob pro položky FEFO

Kdykoli v čase se pro rezervní zásoby použije příjem na sklad s nejpozdějším datem vypršení, aby se umožnilo splnění skutečné poptávky, jako jsou řádky prodejní objednávky nebo kusovníku, v FEFO pořadí.

Abychom si vysvětlili, jak to funguje, předpokládejme následující situaci.

[![Scénář FEFO.](media/FEFOScenario.png)](media/FEFOScenario.png)

Při spuštění plánování se pokryje první prodejní objednávka ze stávajících zásob na skladě a další nákupní objednávka pro zbývající množství.

[![FEFO 1.](media/FEFO1.png)](media/FEFO1.png)

Vytvoří se plánovaná objednávka, aby se zajistilo, že jsou dostupné zásoby doplněny zpět na limit rezervních zásob.

[![FEFO 2.](media/FEFO2.png)](media/FEFO2.png)

Při plánování druhé prodejní se použije pro pokrytí tohoto množství dříve vytvořená plánovaná objednávka pokrývající limit rezervních zásob. Z tohoto důvodu se rezervní zásoby stále vrací.

[![FEFO 3.](media/FEFO3.png)](media/FEFO3.png)

Nakonec se vytvoří jiná plánovaná objednávka k pokrytí rezervních zásob.

[![FEFO 4.](media/FEFO4.png)](media/FEFO4.png)

Všechny dávky vyprší odpovídajícím způsobem a plánované objednávky budou vytvořeny k doplnění rezervních zásob po jejich vypršení.

## <a name="how-master-planning-handles-the-safety-stock-constraint"></a>Jak hlavní plánování zachází s omezením rezervních zásob

Rezervní zásoby jsou sledovány v systému jako typ požadavku, stejně jako prodejní řádky nebo požadavky na kusovníku. Řádek požadavku na rezervní zásoby můžete vidět na stránce **Požadavky netto**, pokud odstraníte výchozí filtr ve sloupci **Typ požadavku**.

Plnění transakce požadavku na rezervní zásoby se sníží priorita, pokud systém zjistí, že to způsobí zpoždění v plnění skutečné poptávky, jako jsou prodejní řádky, řádky kusovníku, požadavky na převody nebo řádky prognózy poptávky. V opačném případě se ujistěte se, že dostupné zásoby jsou nad množstvím rezervních zásob a mají stejnou prioritu jako ostatní typy poptávky. To zajišťuje, že pro skutečné transakce nebude docházet ke zpoždění, a pomáhá předcházet přeplnění nebo předčasnému doplnění rezervních zásob.

Ve fázi disponibility hlavního plánování již doplnění rezervních zásob nemá sníženou prioritu. Zásoby na skladě lze použít před jakýmikoliv jinými typy poptávky. Během výpočtu zpoždění se přidá nová logika k procházení opožděnými prodejními řádky, požadavky na řádek kusovníku a všemi ostatními typy poptávky, za účelem určení, zda mohou být doručeny včas, za předpokladu použití rezervních zásob. Pokud systém identifikuje, že použití rezervních zásob může minimalizovat zpoždění, řádky prodeje nebo řádky kusovníku nahradí jejich počáteční disponibilitu rezervními zásobami a systém místo toho spustí doplnění rezervních zásob.

Pokud pro výpočet zpoždění není nastaven plán nebo položka, bude mít omezení rezervních zásob stejnou prioritu jako ostatní typy poptávky. To znamená, že existuje rezerva zásob na skladě a dalších dostupných zásob před jinými typy poptávky.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

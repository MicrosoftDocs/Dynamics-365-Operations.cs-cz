---
title: Profil a úrovně vyrovnávacích zásob
description: Tento článek poskytuje informace o profilech a úrovních vyrovnávacích zásob, které určují minimální a maximální úrovně zásob, které by měly být zachovány pro každý bod oddělení.
author: t-benebo
ms.date: 06/30/2022
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ReqItemDecoupledLeadTime
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2022-06-30
ms.dyn365.ops.version: 10.0.28
ms.openlocfilehash: d254b949d31d0b15141646503c64760062b77fc7
ms.sourcegitcommit: 3e04f7e4bc0c29c936dc177d5fa11761a58e9a02
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 10/18/2022
ms.locfileid: "9689137"
---
# <a name="buffer-profile-and-levels"></a>Profil a úrovně vyrovnávacích zásob

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]
<!-- KFM: Preview until further notice -->

Poté, co určíte své body oddělení (klíčové položky, které budete strategicky držet na skladě), se musíte rozhodnout, kolik zásob (vyrovnávacích zásob) si u každého z nich ponecháte. Tento úkol je druhým krokem plánování zdrojů materiálů řízených poptávkou (DDMRP).

## <a name="buffer-levels-and-zones"></a>Úrovně a zóny vyrovnávacích zásob

V DDMRP je každé vyrovnávací zásoby definovány pomocí tří hodnot: minimální množství, maximální množství a bod pro objednání. Tyto hodnoty vytvářejí tři rozdílové zóny, které jsou označeny následujícími barevnými kódy:

- **Červená zóna** – Oblast pod minimálním množstvím. Minimální množství je také označováno jako „top of red“ a vaše plánovací strategie by měla být navržena tak, aby bylo zajištěno, že zásoby budou vždy nad tímto bodem.
- **Žlutá zóna** – Oblast mezi minimálním množstvím a bodem pro objednání. Bod pro objednání je také označován jako „top of yellow“. Po dosažení tohoto bodu by měl systém provést objednávku.
- **Zelená zóna** – Oblast mezi bodem pro objednání a maximálním množstvím. Maximální množství je také označováno jako „top of green“. Tento bod je maximální úroveň, na kterou bude zásoba doplněna.

Následující obrázek ukazuje tři barevné zóny a jejich vztah k minimálnímu množství, maximálnímu množství a bodu pro objednání.

![Úrovně a zóny vyrovnávacích zásob DDMRP.](media/ddmrp-buffer-levels.png "Úrovně a zóny vyrovnávacích zásob DDMRP")

## <a name="calculating-the-buffer-zones"></a>Výpočet zón vyrovnávacích zásob

Tato část vysvětluje, jak se počítá výška každé zóny vyrovnávacích zásob.

Žlutá zóna se obvykle počítá jako první. Tato zóna představuje množství, které spotřebujete od okamžiku objednání až do doručení objednávky. Jinými slovy, je to očekávaná spotřeba během doby doplňování. Vypočítává se pomocí následující rovnice:

- **Žlutá zóna** = *Průměrná denní spotřeba (ADU)* × *Oddělená dodací lhůta*

*Oddělená dodací lhůta* představuje čas potřebný k výrobě nebo příjmu položky, pokud jsou oddělovací body vždy na skladě. Obvykle je mnohem kratší než *kumulativní dodací lhůta*, která se tradičně používá v hlavním plánování. Správné nastavení vyrovnávacích zásob je klíčem k zajištění toho, že oddělovací body budou vždy skutečně na skladě, ale nebudou přeplněné.

Červená zóna je vypočítána pomocí následujících rovnic:

- **Červená základna** = *ADU* × *Oddělená dodací lhůta* × *Koeficient dodací doby*
- **Červená bezpečnost** = *Červená základna* × *Koeficient variability*
- **Červená zóna** = *Červená základna* + *Červená bezpečnost*

Zelená zóna se vypočítá jako maximální výsledek následujících tří rovnic:

- *Minimální množství objednávky*
- *ADU* × *Objednávkový cyklus*
- *ADU* × *Oddělená dodací lhůta* × *Koeficient dodací doby*

## <a name="calculating-average-daily-usage"></a>Výpočet průměrného denního využití

Systém používá jeden ze tří přístupů k výpočtu množství, které za den zkonzumujete:

- **Průměrná denní spotřeba (minulost)** – Tento přístup je založen na skutečné minulé spotřebě.
- **Průměrná denní spotřeba (budoucnost)** – Tento přístup je založen na předpovídané budoucí spotřebě.
- **Průměrné denní použití (smíšené)** – Tento přístup je založen na vážené kombinaci minulé a předpokládané spotřeby.

### <a name="average-daily-usage-past"></a>Průměrné denní využití (minulé)

Minulá ADU se vypočítá jako průměr sečtením množství, která se používají každý den po zadaný počet minulých dnů, a pak vydělením součtu počtem dní. Následující obrázek ukazuje, jak tento přístup funguje, když se výpočet dívá tři dny do minulosti.

![Graf průměrného denního využití (minulého).](media/ddmrp-adu-past.png "Graf průměrného denního využití (minulého)")

Na předchozím obrázku, pokud je dnes ráno 11. června, je ADU za předchozí tři dny (8., 9. a 10. června) 21.

- **ADU (minulé)** = (29 + 11 + 23) ÷ 3 = 21

Pro výpočet průměrného denního (minulého) použití se berou v úvahu následující transakce:

- Transakce, které snižují množství položky (v tabulce `inventtrans`, kde je množství menší než nula)
- Transakce se stavem *Na objednávce*, *Rezervováno objednáno*, *Vyhrazeno fyzicky*, *Vychystáno*, *Odečteno* nebo *Prodáno*
- Transakce datované v rámci zvoleného zpětného období (průměrné denní využití za minulé období)
- Jiné transakce než práce ve skladu, karanténa, prodejní nabídky nebo výpisy (`WHSWork`, `WHSQuarantine`, `SalesQuotation` nebo `Statement`)
- Transakce jiné než převodní deníky, které jsou v rámci stejné dimenze pokrytí

### <a name="average-daily-usage-forward"></a>Průměrná denní spotřeba (budoucí)

U nového produktu možná nemáte žádné údaje o minulé spotřebě. Proto můžete místo toho použít předpokládanou ADU do budoucna (například na základě předpokládané poptávky). Následující obrázek ukazuje, jak tento přístup funguje, když se výpočet dívá tři dny do budoucnosti (včetně dneška).

![Graf průměrné denní spotřeby (budoucí).](media/ddmrp-adu-forward.png "Graf průměrné denní spotřeby (budoucí)")

Na předchozím obrázku, pokud je dnes ráno 11. června, je ADU za následující tři dny (11., 12. a 13. června) 21,66.

- **ADU (budoucí)** = (18 + 18 + 29) ÷ 3 = 21,66

Pro výpočet průměrného denního (budoucího) použití se berou v úvahu následující transakce:

- Předpokládané transakce pro položku, kde je v hlavním plánu vybrána předpověď
- Transakce datované v rámci zvoleného budoucího období (průměrné denní využití za budoucí období)

### <a name="average-daily-usage-blended"></a>Průměrná denní spotřeba (smíšená)

Smíšené ADU kombinuje průměrnou minulou spotřebu a průměrnou budoucí spotřebu, jak ukazuje následující obrázek.

![Graf průměrné denní spotřeby (smíšené).](media/ddmrp-adu-blended.png "Graf průměrné denní spotřeby (smíšené)")

Na předchozím obrázku, pokud je dnes ráno 11. června, je smíšená ADU za předchozí a následující tři dny (8.–13. června) 21,33.

- **Smíšená ADU** = (*minulá ADU* + *budoucí ADU*) ÷ 2<br>= (21 + 21,66) ÷ 2<br>= 21,33

## <a name="buffer-calculation-factors"></a>Koeficienty výpočtu vyrovnávacích zásob

Pro každou položku můžete definovat dva koeficienty, které upraví, jak velká má být červená a zelená zóna. Tímto způsobem můžete kompenzovat očekávanou dodací lhůtu a variabilitu poptávky.

![Koeficienty dodací doby a variability.](media/ddmrp-zone-factors.png "Koeficienty dodací doby a variability")

Prvním koeficientem je *koeficient dodací doby*. Hodnota je desetinná hodnota od 0 do 1. Čím delší je doba dodání, tím nižší by měla být hodnota. Demand Driven Institute doporučuje následující rozsahy:

- **Dlouhá doba dodání:** 0,20–0,40
- **Střední dodací doba:** 0,41–0,60
- **Krátká dodací doba:** 0,61–1,00

Druhým koeficientem je *koeficient variability*. Hodnota je desetinná hodnota od 0 do 1. Čím vyšší je variabilita poptávky, tím nižší by měla být hodnota. Demand Driven Institute doporučuje následující rozsahy:

- **Nízká variabilita:** 0,20–0,40
- **Střední variabilita:** 0,41–0,60
- **Vysoká variabilita:** 0,61–1,00

## <a name="buffer-calculation-examples"></a>Příklady výpočtů vyrovnávacích zásob

Tento příklad pokračuje v příkladu výroby polštáře, který je uveden v [Umístění zásob](ddmrp-inventory-positioning.md). V tomto příkladu jste vybrali body oddělení, které zkrátily dobu přípravy z 21 dnů na pět dnů, jak ukazuje následující obrázek.

![Příklad oddělené doby realizace.](media/ddmrp-bom-decoupled-lead-time-example.png "Příklad oddělené doby realizace")

V tomto příkladu předpokládejme, že ADU byla vypočtena jako 23 kusů a jak ukazuje předchozí obrázek, oddělená doba realizace je pět dní. Pomocí těchto hodnot můžete vypočítat žlutou zónu pomocí následující rovnice:

- **Žlutá zóna** = *ADU* × *Oddělená doba realizace* = 115

![Příklad výpočtu žluté zóny.](media/ddmrp-example-calc-yellow.png "Příklad výpočtu žluté zóny")

Výpočet červené zóny se podobá výpočtu žluté zóny, ale je doplněn o variabilitu a dodací lhůtu. V tomto příkladu předpokládejme, že jste zaznamenali střední dodací dobu (koeficient = 0,50) a vysokou variabilitu poptávky (koeficient = 0,8). Použitím těchto hodnot spolu se složkami z rovnice žluté zóny můžete vypočítat červenou zónu pomocí následujících rovnic:

- **Červená základna** = *ADU* × *Oddělená dodací lhůta* × *Koeficient dodací doby* = 57,5
- **Červená bezpečnost** = *Červená základna* × *Koeficient variability* = 46
- **Červená zóna** = *Červená základna* + *Červená bezpečnost* = 103,5

Systém zaokrouhlí červenou zónu na 104 kusů (ks), protože kusy se počítají v celých číslech.

![Příklad výpočtu červené zóny.](media/ddmrp-example-calc-red.png "Příklad výpočtu červené zóny")

Výpočet zelené zóny také zahrnuje komponenty z rovnice žluté zóny, ale umožňuje minimální velikost objednávky, cyklus objednávky a koeficient dodací lhůty. Pro tento příklad předpokládejme, že neexistuje žádný objednávkový cyklus (proto nemáte žádné časové omezení ohledně toho, jak často objednáváte), a minimální objednací množství je 10 kusů. Zelená zóna se pak vypočítá jako maximální výsledek následujících tří rovnic:

- *Minimální množství objednávky* = 10
- *ADU* × *Objednávkový cyklus* = 0
- *ADU* × *Oddělená dodací lhůta* × *Koeficient dodací doby* = 57,5

Systém zaokrouhlí zelenou zónu na 58 kusů (ks), protože kusy se počítají v celých číslech.

![Příklad výpočtu zelené zóny.](media/ddmrp-example-calc-green.png "Příklad výpočtu zelené zóny")

Následující obrázek shrnuje tyto výsledky výpočtu zóny pomocí grafiky trychtýře, která se často používá v DDMRP.

![Shrnutí výsledků výpočtu zóny.](media/ddmrp-example-calc-summary.png "Shrnutí výsledků výpočtu zóny")

## <a name="dynamic-adjustments"></a><a name="dynamic-adjustments"></a>Dynamická vyrovnání

Dynamická vyrovnání umožňují použít *koeficient vyrovnání poptávky* v období vysoké nebo nízké poptávky. Tento koeficient násobí ADU ve všech výpočtech za zvolené období. Vyrovnávací zóny se pak postupně upravují. Tento koeficient obvykle použijete po vygenerování počátečních hodnot vyrovnávacích zásob, abyste je mohli doladit v průběhu času a v reakci na měnící se podmínky. Tento úkol je třetím krokem DDMRP.

Například může být větší poptávka po polštářovém produktu v srpnu, když lidé odjíždějí na dovolenou. Očekává se proto, že prodeje budou vyšší. V tomto případě můžete změnit hodnotu **Koeficient vyrovnání poptávky** pro produkt na *1,5* za všechny týdny v srpnu.

Tímto způsobem můžete vypočítat hodnoty vyrovnávacích zásob v průběhu času a poté je upravit na základě více než jen informací, které systém má. V plné implementaci DDMRP budete každý den pomocí dávkové úlohy vypočítávat nové hodnoty vyrovnávacích zásob a automaticky je přijímat. Poté spustíte plánování jako dávkovou úlohu a každý den budete kontrolovat plánované objednávky, abyste doplnili zásoby.

## <a name="implement-buffers-in-supply-chain-management"></a>Implementace vyrovnávacích zásob v Supply Chain Management

Tato část popisuje, jak implementovat strategii vyrovnávací zóny v Microsoft Dynamics 365 Supply Chain Management. Předpokládá se, že jste již provedli analýzy a výpočty popsané v první polovině tohoto článku.

### <a name="set-up-buffers-for-a-decoupling-point-item"></a><a name="set-up-buffers"></a>Nastavení vyrovnávacích zásob pro položku bodu oddělení

Chcete-li nastavit hodnoty vyrovnávací paměti pro bod oddělení, postupujte podle těchto kroků.

1. Přejděte na **Řízení informací o produktech \> Produkty \> Uvolněné produkty**.
1. Vyberte uvolněnou položku, která je nastavena jako bod oddělení. (Další informace naleznete v tématu [Umístění zásob](ddmrp-inventory-positioning.md).)
1. V podokně akcí na kartě **Plánování** vyberte **Disponibilita položky**.
1. Na stránce **Disponibilita položky** vyberte záznam disponibility položky, který vytvoří bod oddělení. (Tento záznam zobrazí název skupiny disponibility, která je nastavena tak, aby vytvořila body oddělení.)
1. Zvolte kartu **Obecné**.
1. Pokud chcete, aby systém přepočítával hodnoty vyrovnávacích zásob každý den nebo každý týden na základě vaší historie prodeje, prognóz a nastavení skupiny disponibility, postupujte takto:

    1. Nastavte možnost **Hodnoty vyrovnávacích zásob v průběhu času** na *Ano*.
    1. Okno se zprávou vás upozorní, že vaše ruční nastavení vyrovnávacích zásob (**Minimální**, **Bod objednání** a **Maximum**) bude resetováno, pokud budete pokračovat. Výběrem možnosti **Ano** zachováte nové nastavení.

    Případně, pokud dáváte přednost výpočtu nebo zadání nastavení vyrovnávacích zásob pouze jednou, postupujte takto:

    1. Nastavte možnost **Hodnoty vyrovnávacích zásob v průběhu času** na *Ne*.
    1. Nastavte pole **Minimum**, **Bod objednání** a **Maximum** na hodnoty vyrovnávacích zásob, které jste pro položku vypočítali, jak je popsáno dříve v tomto článku.

1. Nastavením následujících polí dokončíte nastavení výpočtů DDMRP pro položku:

    - **Objednací cyklus** – Zadejte počet dní, které musí uplynout mezi nákupními objednávkami pro položku. Nastavte hodnotu na *0* (nula), pokud neexistují žádná omezení objednávky. Toto pole ovlivňuje vyrovnávací zásoby maximálního množství, jak bylo popsáno dříve v tomto článku.
    - **Průměrná denní spotřeba** – Volitelně můžete zadat odhadovaný ADU pro položku. Toto pole je určeno pouze pro informaci. Obvykle se hodnota automaticky vypočítá jako součást výpočtů vyrovnávacích zásob.
    - **Práh špičky objednávky** – Zadejte minimální počet denních prodejů položky, které se kvalifikují jako nárůst prodeje (neobvykle vysoká poptávka). Systém toto pole využívá ke zvýšení doobjednávacího množství plánovaných zakázek v obdobích vysoké poptávky. Více informací získáte v části [Plánování řízené poptávkou](ddmrp-planning.md).

### <a name="calculate-or-enter-decoupled-lead-times"></a><a name="calc-lead-time"></a>Výpočet nebo zadání oddělených dob realizace

U položek, u kterých se rozhodnete, že systému povolíte [automaticky vypočítat vyrovnávací zóny](#set-up-buffers), postupujte podle těchto kroků pro výpočet nebo zadání oddělených dodacích lhůt pro položku bodu oddělení.

1. Otevřete stránku **Disponibilita položky** pro vaši položku bodu oddělení. (Další informace viz [Nastavení vyrovnávacích zásob pro položku bodu oddělení](#set-up-buffers).)
1. Vyberte záznam disponibility položky, který vytvoří bod oddělení.
1. Vyberte kartu **Hodnoty vyrovnávacích zásob**.
1. Pokud nejsou v mřížce zobrazeny žádné časové úseky, v podokně akcí na kartě **Hodnoty vyrovnávacích zásob** vyberte **Přidat časová období**. Systém vyplní mřížku řádky pro každé denní nebo týdenní časové období, v závislosti na tom, zda je pole **Minimální, maximální a období pro opětovné objednání** pro [skupinu disponibility](ddmrp-inventory-positioning.md) nastaveno na *Denně* nebo *Týdně*. Systém přidá dostatek řádků, aby dosáhl časové hranice, která je určena pro skupinu disponibility přiřazenou k položce.
1. Vyberte časové období, pro které chcete vypočítat oddělenou dobu realizace. (Toto časové období je obvykle období, které zahrnuje dnešní datum.)
1. V podokně akcí na kartě **Hodnoty vyrovnávacích zásob** vyberte **Vypočítat oddělenou dobu realizace**.
1. V dialogovém okně **Vypočítat oddělenou dobu realizace** nastavte následující pole:

    - **Kusovník** – Vyberte kusovník (BOM), na kterém chcete spustit výpočet.
    - **Datum** – Vyberte datum, na kterém chcete spustit výpočet. Sada dostupných kusovníků bude filtrována tak, aby se zobrazily pouze kusovníky, které jsou aktivní pro vybrané datum.
    - **Množství** – Zadejte množství produktu, pro které chcete výpočet provést. Sada dostupných kusovníků bude filtrována tak, aby se zobrazily pouze kusovníky, které platí pro zadané množství.

1. Vyberte **OK** pro spuštění výpočtu a uzavření dialogového okna **Vypočítat oddělenou dobu realizace**. Sloupec **Oddělená doba realizace** pro zvolené časové období nyní zobrazuje vypočtenou hodnotu.

### <a name="calculate-or-enter-average-daily-usage"></a><a name="calc-adu"></a>Výpočet nebo zadání průměrného denního využití

U položek, u kterých se rozhodnete, že systému povolíte [automaticky vypočítat vyrovnávací zóny](#set-up-buffers), postupujte podle těchto kroků pro výpočet nebo zadání ADU pro položku bodu oddělení.

1. Otevřete stránku **Disponibilita položky** pro vaši položku bodu oddělení. (Další informace viz [Nastavení vyrovnávacích zásob pro položku bodu oddělení](#set-up-buffers).)
1. Vyberte záznam disponibility položky, který vytvoří bod oddělení.
1. Vyberte kartu **Hodnoty vyrovnávacích zásob**.
1. Pokud nejsou v mřížce zobrazeny žádné časové úseky, v podokně akcí na kartě **Hodnoty vyrovnávacích zásob** vyberte **Přidat časová období**. Systém vyplní mřížku řádky pro každé denní nebo týdenní časové období, v závislosti na tom, zda je pole **Minimální, maximální a období pro opětovné objednání** pro [skupinu disponibility](ddmrp-inventory-positioning.md) nastaveno na *Denně* nebo *Týdně*. Kromě toho výchozí hodnoty pro pole **Koeficient dodací doby** a **Koeficient variability** jsou převzata ze skupiny disponibility. Tyto hodnoty můžete upravit pro každý řádek podle potřeby.
1. Vyberte časové období, kde chcete vypočítat ADU.
1. V podokně akcí na kartě **Hodnoty vyrovnávacích zásob** vyberte **Vypočítat průměrnou denní spotřebu**. Systém se snaží shromáždit data, která jsou potřebná pro výpočet ADU, jak je definován pro [skupinu disponibility](ddmrp-inventory-positioning.md).
1. Proveďte jeden z následujících kroků:

    - Pokud jsou požadovaná data k dispozici, výsledky výpočtů jsou přidány do sloupce **Průměrná denní spotřeba**. V tomto případě není vyžadována žádná akce.
    - Pokud požadovaná data nejsou k dispozici, automaticky se nepřidají žádné hodnoty. V tomto případě ručně zadejte odhadované hodnoty pro každý řádek, kde plánujete vypočítat hodnoty vyrovnávacích zásob.

### <a name="calculate-and-apply-buffer-values"></a>Výpočet a použití hodnot vyrovnávacích zásob

U položek, u kterých se rozhodnete, že systému povolíte [automaticky vypočítat vyrovnávací zóny](#set-up-buffers), můžete následujícím postupem ručně aktivovat výpočet hodnot vyrovnávacích zásob.

1. Pro příslušnou položku bodu oddělení, [nakonfigurujte výpočet vyrovnávacích zásob](#set-up-buffers), [vypočítejte nebo zadejte oddělené doby realizace](#calc-lead-time) a [vypočítejte nebo zadejte průměrnou denní spotřebu](#calc-adu) pro všechna relevantní časová období, jak bylo popsáno dříve v tomto článku.
1. Otevřete stránku **Disponibilita položky** pro vaši položku bodu oddělení.
1. Vyberte kartu **Hodnoty vyrovnávacích zásob**, která by již měla zobrazovat seznam časových období.
1. Vyberte časové období, kde chcete vypočítat hodnoty vyrovnávacích zásob. (Toto časové období bude obvykle období, které zahrnuje dnešek.) Řádek, který vyberete, již musí mít nenulové hodnoty ve sloupcích **Průměrná denní spotřeba** a **Oddělená doba realizace**.
1. Upravte pole **Koeficient vyrovnání poptávky** pro jeden nebo více řádků podle potřeby. Systém použije tento koeficient na hodnotu **Průměrná denní spotřeba** ve všech výpočtech vyrovnávacích zásob, kde je tato hodnota použita. Tento koeficient vám umožňuje přizpůsobit se tomu, jak poptávka kolísá podle data (například pro dovolené nebo sezónní položky).
1. V podokně akcí na kartě **Hodnoty vyrovnávacích zásob** vyberte **Vypočítat minimální, maximální množství a množství bodu objednání**. Systém vypočítá a vyplní sloupce **Vypočtené min.**, **Vypočítaný bod objednání** a **Vypočtené max.** v mřížce na stránce **Disponibilita položky**.
1. Po dokončení kontroly vypočítaných hodnot je musíte použít. Jinak nebudou mít žádný účinek. Když použijete výpočet pro jeden nebo více řádků, hodnoty z polí **Vypočtené min**, **Vypočítaný bod objednání** a **Vypočítané max.** se zkopírují do sloupců **Min.**, **Bod objednání** a **Max.** V podokně akcí na kartě **Hodnoty vyrovnávacích zásob** ve skupině **Provést akci** vyberte jedno z následujících tlačítek:

    - **Přijmout všechny výpočty** – Použijte všechny vypočítané hodnoty v mřížce.
    - **Přijmout výpočty pro vybrané řádky** – Použít vypočítané hodnoty pouze pro vybrané řádky.
    - **Zahodit všechny výpočty** – Zrušit všechny vypočítané hodnoty pro minimální množství, maximální množství a body objednání v mřížce.
    - **Zahodit výpočty pro vybrané řádky** – Zrušit všechny vypočítané hodnoty pro minimální množství, maximální množství a body objednání pro vybrané řádky.

### <a name="schedule-automatic-buffer-value-calculations"></a>Naplánování automatických výpočtů hodnot vyrovnávací paměti

Po úplném nastavení DDMRP a potvrzení, že fungují podle očekávání, budete pravděpodobně chtít nastavit dávkovou úlohu pro pravidelné přepočítávání ADU a souvisejících hodnot vyrovnávacích zásob podle potřeby na základě údajů o skutečné spotřebě nebo aktualizovaných prognóz. Tento postup se vztahuje pouze na položky, u kterých se rozhodnete, že systému povolíte [automaticky vypočítat vaše vyrovnávací zóny](#set-up-buffers).

Chcete-li naplánovat automatické výpočty hodnoty vyrovnávacích zásob, postupujte podle těchto kroků.

1. Přejděte na nabídku **Hlavní plánování \> Hlavní plánování \> DDMRP \> Vypočítat hodnoty vyrovnávacích zásob**.
1. V dialogovém okně **Vypočítat hodnoty vyrovnávacích zásob** nastavte následující pole:

    - **Vypočítat průměrnou denní spotřebu** – Nastavte tuto možnost na *Ano* pro přepočet ADU položek bodu oddělení při každém spuštění úlohy. Nastavte na *Ne*, pokud chcete tento výpočet přeskočit. Obvykle byste měli nastavit tuto možnost na *Ano*.
    - **Vypočítat oddělený dodací čas** – Nastavte tuto možnost na *Ano* pro přepočet oddělené doby realizace při každém spuštění úlohy. Nastavte na *Ne*, pokud chcete tento výpočet přeskočit. Obvykle byste měli nastavit tuto možnost na *Ano*.
    - **Vypočítat hodnoty vyrovnávacích zásob** – Nastavte tuto možnost na *Ano* pro přepočet hodnot vyrovnávacích zásob při každém spuštění úlohy. Nastavte na *Ne*, pokud chcete tento výpočet přeskočit. Obvykle byste měli nastavit tuto možnost na *Ano*.
    - **Přijmout výpočet pro min., max. a bod objednání** – Nastavte tuto možnost na *Ano* pro automatické schválení a použití přepočítané hodnoty vyrovnávacích zásob při každém spuštění úlohy. Nastavte na *Ne* pro ponechání přepočtené hodnoty nepoužité. V tomto případě se přepočítané hodnoty neprojeví, pokud je někdo později ručně nepoužije ze stránky **Disponibilita položky** jednotlivých produktů. Obvykle byste měli nastavit tuto možnost na *Ano*.
    - **Hlavní plán** – Vyberte hlavní plán, který obsahuje položky, které budou ovlivněny výpočtem. Výpočet bude platit pro všechny položky ve filtru plánu, který bude dále omezen nastavením **Filtr** v tomto dialogovém okně.

1. Chcete-li omezit sadu záznamů, na kterých má tato dávková úloha běžet, vyberte **Filtr** na záložce **Záznamy, které mají být zahrnuty**, aby se otevřelo dialogové okno **Dotaz**. Toto dialogové okno funguje stejně u jiných typů [prací na pozadí](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) v Supply Chain Management.
1. Na pevné záložce **Spustit na pozadí** určete, jak, kdy a jak často se mají provádět vybrané výpočty pro vybrané položky. Pole fungují stejně jako u jiných typů [prací na pozadí](../../../fin-ops-core/dev-itpro/sysadmin/batch-processing-overview.md) v Supply Chain Management.
1. Výběrem **OK** přidejte novou úlohu do fronty dávek k vykonání.

### <a name="review-and-recalculate-decoupled-lead-times-for-all-items"></a>Zkontrolujte a přepočítejte oddělené dodací lhůty pro všechny položky

Chcete-li zkontrolovat a přepočítat všechny oddělené dodací lhůty, které jsou k dispozici ve vaší právnické osobě (společnosti), postupujte podle těchto kroků.

1. Přejděte na nabídku **Hlavní plánování \> Hlavní plánování \> DDMRP \> Oddělená doba realizace**.
1. Na stránce **Oddělená doba realizace** procházejte a filtrujte seznam podle potřeby, abyste našli informace, které hledáte. Chcete-li zobrazit ještě více informací o položce, vyberte její odkaz ve sloupci **Číslo položky**.
1. Chcete-li přepočítat oddělenou dobu realizace pro jakoukoli položku, vyberte položku a poté vyberte **Vypočítat oddělenou dobu realizace** v podokně akcí. Zobrazí se dialogové okno **Vypočítat oddělenou dobu realizace**. Toto dialogové okno funguje stejně jako když [vypočítáte oddělené doby realizace](#calc-lead-time) pro stejnou položku na stránce **Disponibilita položky**.

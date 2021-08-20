---
title: Záporné dny a dynamické záporné dny
description: Toto téma obsahuje informace o záporných dnech a dynamických záporných dnech a o tom, jak je lze použít k usnadnění vašeho podnikání.
author: ChristianRytt
ms.date: 05/25/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2019-06-07
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d5e86cc8abd4de1e23b1a7f7217bbb1fd5ea966b988a879e663b6f393e0d1204
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756960"
---
# <a name="negative-days-and-dynamic-negative-days"></a>Záporné dny a dynamické záporné dny

[!include [banner](../includes/banner.md)]

Toto téma obsahuje informace o záporných dnech a dynamických záporných dnech a o tom, jak je lze použít k usnadnění vašeho podnikání. *Ochranná doba záporných dnů* představuje počet dní, které jste ochotni čekat před objednáním nového doplnění v případě záporného množství zásob.

V tomto tématu se dozvíte následující operace:

- Jak jsou vytvářeny plánované objednávky
- Korelace mezi ochrannou dobou záporných dnů a dobou realizace položky
- Jak je vypočtena ochranná doba dynamických záporných dnů a jakým způsobem je doba realizace položky připočítána do výpočtu
- Jak interpretovat [návrhy pro zlepšení doby spuštění plánování požadavků na materiál (MRP) (hlavní plánování)](https://blogs.msdn.com/b/axmfg/archive/2015/01/02/checklist-for-improving-mrp-performance-part-2-how-to-setup-planning-parameters.aspx) souvisejícími se zápornými dny

V tomto tématu jsou použity tři hypotetické scénáře, které vám pomohou těmto informacím porozumět. Rozdíl mezi scénáři je bod, ve kterém se získává poptávka: před, během nebo po období realizace položky.

## <a name="scenario-1-you-get-demand-before-the-items-lead-time-period"></a>Scénář 1: Dostanete poptávku před obdobím realizace položky

Poptávku můžete dostat buď relativně brzy v době realizace položky nebo těsně předtím, než období realizace začne. Zde je příklad tohoto scénáře:

- Položka DemoProduct má 6denní období realizace.
- V den nula (1. ledna) je úroveň zásob pro položku DemoProduct 0 (nula).
- V den nula (1. ledna) dostanete prodejní objednávku na množství 10 položky DemoProduct.
- V den sedm (8. ledna) existuje nákupní objednávka na množství 10 položky DemoProduct.

Následující obrázek znázorňuje grafické zobrazení tohoto scénáře.

![Grafické zobrazení scénáře 1.](./media/negative-days-1.jpg)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Případ A: záporné dny jsou menší než doba realizace položky

Nastavíte-li záporné dny na číslo, které je menší než doba realizace položky, MRP vyhledá příjemky pro položku DemoProduct v ochranném období záporných dnů. Protože nenalezne žádné příjemky, vytvoří MRP novou plánovanou nákupní objednávku. Tato plánovaná objednávka je okamžitě odložena o šest dní (doba realizace). Bude tedy doručena 7. ledna. Existující nákupní objednávka dostane zprávu akce **Zrušit**, protože vytvoření nové plánované nákupní objednávky ji učinilo nadbytečnou.

Následující obrázek znázorňuje snímek obrazovky tohoto případu.

![Snímek obrazovky případu A pro scénář 1.](./media/negative-days-2.png)

Následující obrázek znázorňuje grafické zobrazení toho, co se stane v tomto případě.

![Grafické zobrazení případu A pro scénář 1.](./media/negative-days-3.png)

Pokud zvažujete výkonnost MRP a nechcete být nervózní, tento případ není ideální. MRP musí vytvořit novou plánovanou objednávku a musí spočítat zpoždění a akce. Tyto úkoly jsou časově náročné. Tento případ také přidá do plánu další dvě transakce. Na druhé straně je prodejní objednávka odložena pouze o šest dní, nikoli o sedm dní.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Případ B: záporné dny jsou větší než doba realizace položky

Chcete-li zlepšit výkonnost MRP, můžete nastavit záporné dny na číslo, které je vyšší než doba realizace položky. Protože v tomto scénáři nemůžete obdržet dodávku v době realizace, můžete hledat příjemky tak dlouho, dokud toto hledání dává smysl. Ačkoliv operační čas pro MRP bude kratší, měli byste sledovat další zpoždění objednávek.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Případ C: Automatická korelace doby realizace položky na ochrannou dobu záporných dnů

Pro automatickou korelaci doby realizace položky na ochrannou dobu záporných dnů použijte dynamické záporné dny. Chcete-li použít dynamické záporné dny, přejděte na **Hlavní plánování \> Nastavení \> Parametry hlavního plánování** a poté na kartě **Obecné** v části **Disponibilita** nastavte možnost **Použít dynamické záporné dny** na **Ano**. MRP poté vyhledá příjemky v ochranné době dynamických záporných dnů. Ochranná doba se vypočte podle následujícího vzorce:

Ochranná doba dynamických záporných dnů = doba realizace nákupu + ochranná doba záporných dnů + (aktuální datum – datum požadavku)

(Pokud výchozí typ objednávky položky DemoProduct je **Výroba** nebo **Převod**, doba realizace je dobou realizace **skladu** .)

Když se použijí dynamické záporné dny, je ochranná doba, po kterou se MRP dívá na příjemky, 6 + 2 + 0 = 8 dní. MRP vyhledá existující nákupní objednávku a naváže na ní prodejní objednávku. Nejsou vytvořeny žádné nové plánované objednávky. Operační čas pro MRP je tedy kratší. Následující obrázek zobrazuje čisté požadavky pro položku DemoProduct.

![Čisté požadavky pro případ C scénáře 1.](./media/negative-days-4.png)

Následující obrázek znázorňuje grafické zobrazení toho, co se stane v tomto případě.

![Grafické zobrazení případu C pro scénář 1.](./media/negative-days-5.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Případ D: Použití pouze dynamických záporných dnů

Pokud nastavíte záporné dny na **0** (nula) a použijete ochrannou dobu pouze dynamických záporných dní, bude ochranná doba dynamických záporných dnů 6 + 0 + 0 = 6 dní. V tomto případě je výsledek stejný jako výsledek pro případ A tohoto scénáře. MRP musí vytvořit novou plánovanou objednávku a musí spočítat zpoždění a akce. Tyto úkoly jsou časově náročné a mohou být také frustrující. Máte také dvě další transakce, které je třeba zpracovat. Vzhledem k tomu, že poptávka nemůže být splněna včas pro doručení položky, tento případ přidá do plánu zbytečné komplikace.

Následující obrázek znázorňuje snímek obrazovky tohoto případu.

![Snímek obrazovky případu D pro scénář 1.](./media/negative-days-6.png)

Následující obrázek znázorňuje grafické zobrazení toho, co se stane v tomto případě.

![Grafické zobrazení případu D pro scénář 1.](./media/negative-days-7.png)

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Případ E: Použití záporných dnů, které jsou větší než doba realizace položky a ochranná doba dynamických záporných dnů.

Nastavíte-li záporné dny na číslo, které je větší než doba realizace položky, a pokud používáte také ochrannou dobu dynamických záporných dnů, bude ochranná doba dynamických záporných dnů 6 + 6 + 0 = 12 dní. Tento přístup může vytvořit velmi dlouhou ochranou dobu, ve které musí MRP hledat výsledky. Informace o tom, jak souvisí případ E s situací, kdy je nutné nastavit negativní dny na dlouhou ochrannou dobu, naleznete v části [Závěr](#conclusion) tohoto tématu.

## <a name="scenario-2-you-get-demand-during-the-items-lead-time-period"></a>Scénář 2: Dostanete poptávku během období realizace položky

V průběhu doby realizace položky můžete obdržet poptávku. Zde je příklad tohoto scénáře:

- Položka DemoProduct má 6denní období realizace. 
- V den nula (1. ledna) je úroveň zásob pro položku DemoProduct 0 (nula).
- Ve čtvrtém dni (5. ledna), který spadá do doby realizace položky, získáte prodejní objednávku na množství 10 položky DemoProduct.
- V den sedm (8. ledna) existuje nákupní objednávka na množství 10 položky DemoProduct.

Následující obrázek znázorňuje grafické zobrazení tohoto scénáře.

![Grafické zobrazení scénáře 2.](./media/negative-days-8.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Případ A: záporné dny jsou menší než doba realizace položky

Nastavíte-li záporné dny na číslo, které je menší než doba realizace položky, MRP vyhledá příjemky pro položku DemoProduct v ochranném období záporných dnů. Vzhledem k tomu, že se nenaleznou žádné příjemky, vytvoří MRP novou plánovanou nákupní objednávku, která jako datum objednávky použije aktuální datum. Tato plánovaná objednávka je okamžitě odložena o šest dní (doba realizace). Bude tedy doručena 7. ledna. Existující nákupní objednávka dostane zprávu akce **Zrušit**, protože vytvoření nové plánované nákupní objednávky ji učinilo nadbytečnou.

Následující obrázek znázorňuje snímek obrazovky tohoto případu.

![Snímek obrazovky případu A pro scénář 2.](./media/negative-days-9.png)

Následující obrázek znázorňuje grafické zobrazení toho, co se stane v tomto případě.

![Grafické zobrazení případu A pro scénář 2.](./media/negative-days-10.png)

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Případ B: záporné dny jsou větší než doba realizace položky

Tento případ se podobá případu B pro scénář 1. Pokud nastavíte záporné dny na číslo, které je větší než doba realizace položky, nezískáte novou plánovanou objednávku. Prodejní objednávka je připojena k existující nákupní objednávce.

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Případ C: Automatická korelace doby realizace položky na ochrannou dobu záporných dnů

Tento případ se podobá případu C pro scénář 1, protože dynamické záporné dny fungují stejně jako v tomto případě. Ochranná doba dynamických záporných dnů je nyní 6 + 2 – 4 = 4 dny. Použijete-li tento přístup, vyhledá MRP existující nákupní objednávku a připojí k ní prodejní objednávku. Vzhledem k tomu, že nejsou vytvořeny žádné nové plánované objednávky, je doba zpracování MRP kratší.

Následující obrázek znázorňuje snímek obrazovky tohoto případu.

![Snímek obrazovky případu C pro scénář 2.](./media/negative-days-11.png)

Následující obrázek znázorňuje grafické zobrazení toho, co se stane v tomto případě.

![Grafické zobrazení případu C pro scénář 2.](./media/negative-days-12.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Případ D: Použití pouze dynamických záporných dnů

Pokud nastavíte záporné dny na **0** (nula) a použijete ochrannou dobu pouze dynamických záporných dní, bude ochranná doba dynamických záporných dnů 6 + 0 - 4 = 2 dny. V tomto případě je výsledek stejný jako výsledek pro případ A tohoto scénáře. Pro grafické zobrazení toho, co se děje, se podívejte na případ A v tomto scénáři.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Případ E: Použití záporných dnů, které jsou větší než doba realizace položky a ochranná doba dynamických záporných dnů.

Nastavíte-li záporné dny na číslo, které je větší než doba realizace položky, a pokud používáte také ochrannou dobu dynamických záporných dnů, bude ochranná doba dynamických záporných dnů 6 + 6 - 4 = 8 dní. Tento přístup může vytvořit velmi dlouhou ochranou dobu, ve které musí MRP hledat výsledky. Informace o tom, jak souvisí případ E s situací, kdy je nutné nastavit negativní dny na dlouhou ochrannou dobu, naleznete v části [Závěr](#conclusion) tohoto tématu.

## <a name="scenario-3-you-get-demand-after-the-items-lead-time-period"></a>Scénář 3: Dostanete poptávku po období realizace položky

Můžete dostat poptávku po období realizace položky. Zde je příklad tohoto scénáře:

- Položka DemoProduct má 6denní období realizace.
- V den nula (1. ledna) jsou zásoby pro položku DemoProduct 0 (nula).
- V den sedm (8. ledna), který spadá mimo dobu realizace položky, získáte prodejní objednávku na množství 10 položky DemoProduct.
- V den deset (11. ledna) existuje nákupní objednávka na množství 10 položky DemoProduct.

Následující obrázek znázorňuje grafické zobrazení tohoto scénáře.

![Grafické zobrazení scénáře 3.](./media/negative-days-13.png)

### <a name="case-a-negative-days-are-less-than-the-items-lead-time"></a>Případ A: záporné dny jsou menší než doba realizace položky

Nastavíte-li záporné dny na číslo, které je menší než doba realizace položky, MRP se dívá dva dny dopředu před datum požadavku prodejní objednávky. Protože nenalezne nic, vytvoří MRP novou plánovanou nákupní objednávku na 2. ledna. Tato plánovaná nákupní objednávka bude expedována právě včas ke splnění poptávky prodejní objednávky. Existující nákupní objednávka získá zprávu akce **Zrušit**, protože není povinná.

Následující obrázek znázorňuje snímek obrazovky tohoto případu.

![Snímek obrazovky případu A pro scénář 3.](./media/negative-days-14.png)

Následující obrázek znázorňuje grafické zobrazení toho, co se stane v tomto případě.

![Grafické zobrazení případu A pro scénář 3.](./media/negative-days-15.png)

> [!NOTE]
> V předchozím snímku obrazovky je datum požadavku nákupní objednávky 12. ledna. Vzhledem k tomu, že snímek obrazovky byl pořízený v roce 2015, kdy 11. ledna byla neděle, MRP přesunul datum požadavku na následující pracovní den, což bylo pondělí 12. ledna. Nákupní objednávka má však datum dodání 11. ledna.

### <a name="case-b-negative-days-are-more-than-the-items-lead-time"></a>Případ B: záporné dny jsou větší než doba realizace položky

Pokud nastavíte záporné dny na číslo, které je větší než doba realizace položky, nezískáte novou plánovanou objednávku. Prodejní objednávka je navázána proti existující nákupní objednávce. Prodejní objednávka je proto zpožděná. Pokud vytvoříte plánovanou objednávku, můžete prodejní objednávku dodat včas.

Následující obrázek znázorňuje snímek obrazovky tohoto případu.

![Snímek obrazovky případu B pro scénář 3.](./media/negative-days-16.png)

Následující obrázek znázorňuje grafické zobrazení toho, co se stane v tomto případě.

![Grafické zobrazení případu B pro scénář 3.](./media/negative-days-17.png)

### <a name="case-c-automatically-correlate-the-items-lead-time-to-the-negative-days-time-fence"></a>Případ C: Automatická korelace doby realizace položky na ochrannou dobu záporných dnů

Tento případ se podobá případu C pro scénář 1, protože dynamické záporné dny fungují stejně, pokud ne lépe, jako v případě B tohoto scénáře.

Ochranná doba dynamických záporných dnů je nyní 6 + 2 – 7 = 1 den. V tomto případě však systém stále ještě nebere v úvahu záporné dny realizace (2), protože MRP považuje maximální hodnotu mezi dobou realizace záporných dnů a dobou realizace dynamických záporných dnů. Proto je v tomto případě výsledek stejný jako výsledek pro případ A tohoto scénáře.

Následující obrázek znázorňuje grafické zobrazení toho, co se stane v tomto případě.

![Grafické zobrazení případu C pro scénář 3.](./media/negative-days-18.png)

### <a name="case-d-use-only-dynamic-negative-days"></a>Případ D: Použití pouze dynamických záporných dnů

Pokud nastavíte záporné dny na **0** (nula) a použijete ochrannou dobu pouze dynamických záporných dní, bude ochranná doba dynamických záporných dnů 6 + 0 - 7 = - 1 den. V takovém případě systém stále bere v úvahu dobu realizace záporných dnů (2). Proto je v tomto případě výsledek stejný jako výsledek pro případ A tohoto scénáře a má všechny stejné nedostatky. Pro grafické zobrazení toho, co se děje, se podívejte na případ A ve scénáři 2.

### <a name="case-e-use-both-negative-days-that-are-more-than-the-items-lead-time-and-the-dynamic-negative-days-time-fence"></a>Případ E: Použití záporných dnů, které jsou větší než doba realizace položky a ochranná doba dynamických záporných dnů.

Tento případ je stejný jako případ E pro scénáře 1 a 2. Má v podstatě stejné výhody a nedostatky.

## <a name="conclusion"></a>Závěr

Tři scénáře v tomto tématu ukazují, že je vhodné nastavit záporné dny na číslo, které je větší než doba realizace položek ve skupině disponibility. Je také vhodné používat pouze dynamické záporné dny a nastavit záporné dny na počet dní, které jste ochotni čekat před objednáním nového doplnění v případě, že máte záporný sklad (jinými slovy, počet dní, o které jste ochotni dále zpozdit poptávku). Kromě toho by položky ve stejné skupině disponibility měly mít podobné doby realizace.

Nastavíte-li záporné dny na **0** (nula) a nepoužijete záporné dynamické dny, MRP vždy vytvoří novou plánovanou objednávku, která má splnit poptávku. V této situaci je důležité, abyste pracovali se zprávami akce pro ujištění, že se nebudou hromadit zásoby.

Záporné dny můžete chtít nastavit na dlouhou ochrannou dobu a poté pracovat se zprávami akce. Tento přístup přináší dobré výsledky plánování, ale je také trochu pomalejší. Rovněž může být obtížnější analýza, protože je nutné provést analýzu a použít zprávy akce. Následuje příklad:

- Položka DemoProduct má 6denní období realizace.
- V den nula (1. ledna) jsou zásoby pro položku DemoProduct 0 (nula).
- V den nula (1. ledna) dostanete prodejní objednávku na množství 10 položky DemoProduct.
- V den devět (10. ledna) dostanete prodejní objednávku na množství 10 položky DemoProduct.
- V den jedenáct (12. ledna) existuje nákupní objednávka na množství 10 položky DemoProduct.
- Záporné dny jsou nastaveny na **20**, což je mnohem více, než doba realizace položky.

Následující obrázek znázorňuje grafické zobrazení toho, co se stane.

![Grafická revize příkladu.](./media/negative-days-19.png)

MRP vytváří následující výsledky.

![Příklad výsledků 1.](./media/negative-days-20.png)

Na předchozím snímku obrazovky je datum požadavku prodejní objednávky 9. ledna namísto 10. ledna. Vzhledem k tomu, že snímek obrazovky byl pořízený v roce 2015, kdy 10. ledna byla sobota, datum požadavku objednávky by mělo být předchozí pracovní den, což byl pátek 9. ledna.

MRP vytvoří plánovanou nákupní objednávku pro splnění poptávky, kterou požaduje první prodejní objednávka, ale dále doporučuje zrušit plánovanou objednávku, protože můžete posunout stávající nákupní objednávku a zvýšit její množství.

Výsledky nejsou nesprávné, ale operační doba pro MRP může být delší, protože MRP musí vytvářet všechna zpoždění a návrhy. Dále může plánovač vyžadovat více času pro pochopení výsledků MRP. Nejdůležitější v tomto případě je to, aby plánovač porozuměl zprávám akce a používal je.

Pokud snížíte záporné dny na číslo, které je bližší k době realizace položky, a použijete dynamické záporné dny, vytvoří modul MRP následující výsledky.

![Příklad výsledků 2.](./media/negative-days-21.png)

MRP vytvoří plánovanou objednávku, která je připojena k první prodejní objednávce. Poté bude podle očekávání druhá prodejní objednávka navázána proti existující nákupní objednávce na základě nastavení záporných dnů. Tento výsledek plánování je také správný a operační doba pro MRP může být kratší. V takovém případě není důležité chápat a vědět, jak pracovat se zprávami akce.

Chcete-li zaručit, že budou zadány správné hodnoty pro váš podnik, musíte myslet jak na funkčnost, tak na operační čas MRP. Proto může při určování optimálních hodnot být zapotřebí trochu zkoušení.

## <a name="see-also"></a>Viz také

Další diskuze naleznete v původním příspěvku blogu [Více o (dynamických) záporných dnech](/archive/blogs/axmfg/more-about-dynamic-negative-days).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

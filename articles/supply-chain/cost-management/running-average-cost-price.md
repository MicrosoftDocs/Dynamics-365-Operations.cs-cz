---
title: Průběžná průměrná nákladová cena
description: Proces uzávěrky skladu v aplikaci vyrovná výdejové transakce příjmovými transakcemi podle metody oceňování zásob, která je vybraná ve skupině modelu zboží. Před spuštěním uzávěrky skladu však systém vypočítá průběžnou průměrnou nákladovou cenu, která obvykle slouží k účtování výdejových transakcí.
author: AndersGirke
ms.date: 02/02/2022
ms.topic: article
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 871b3ffce45848f95d132eff3fd327295bc5084c
ms.sourcegitcommit: fefe93f3f44d8aa0b7e6d54cc4a3e5eca6e64feb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2022
ms.locfileid: "8092182"
---
# <a name="running-average-cost-price"></a>Průběžná průměrná nákladová cena

[!include [banner](../includes/banner.md)]

Proces uzávěrky skladu v aplikaci vyrovná výdejové transakce příjmovými transakcemi podle metody oceňování zásob, která je vybraná ve skupině modelu zboží. Před spuštěním uzávěrky skladu však systém vypočítá průběžnou průměrnou nákladovou cenu, která obvykle slouží k účtování výdejových transakcí.

Systém odhaduje průběžnou průměrnou nákladovou cenu pro položku pomocí následujícího vzorce:

Odhadovaná cena = (fyzická částka + finanční částka) ÷ (fyzické množství + finanční množství)

## <a name="default-item-cost"></a>Výchozí náklady na zboží

Výchozí náklady na zboží pro vydaný produkt mohou být na stránce **Podrobnosti o uvolněném produktu** konfigurovány jedním ze dvou způsobů:

- Standardní náklady vytvoříte výběrem možnosti **Cena položky** ve skupině **Nastavení** na kartě **Správa nákladů** v podokně akcí. Pokud použijete tuto metodu, musíte použít standardní verzi pro účtování nákladů a náklady musejí být aktivovány.
- Definujte výchozí cenu položky pro uvolněný produkt zadáním hodnoty do pole **Cena** na záložce **Správa nákladů**.

Kromě zadání nebo vytvoření ceny můžete zapnout zaškrtávací políčko **Použít nejnovější nákladovou cenu** na záložce **Správa nákladů** ve stránce **Podrobnosti o uvolněném produktu**. V tomto případě systém automaticky aktualizuje pole **Cena** při zaúčtování finanční aktualizace. Pokud například zaúčtujete fakturu nákupní objednávky, pole bude nastaveno na nákupní cenu z této faktury.

Pokud máte nákladovou cenu v aktivní verzi ocenění a zadáte cenu na záložce **Správa nákladů**, systém použije cenu z verze aktivní kalkulace předtím, než použije cenu definovanou na záložce **Správa nákladů**.

## <a name="using-the-running-average-cost-price"></a>Použití průběžné průměrné nákladové ceny

Následující tabulka uvádí případy, kdy systém účtuje skladové transakce na základě průběžné průměrné nákladové ceny, a kdy používá nákladovou cenu definovanou v hlavním záznamu položky.

| Podmínka | Systém používá odhadovanou průběžnou průměrnou nákladovou cenu | Systém používá výchozí nákladovou cenu položky |
| --- | --- | --- |
| Dělenec\* i dělitel\*\* jsou kladné. | Ano | Číslo |
| Dělenec\*, dělitel\*\*, nebo oba jsou záporné. | Ne | Ano |
| Dělenec\*\* má hodnotu 0 (nula). | Ne | Ano |

\* Čitatel = (fyzická částka + finanční částka)  
\*\* Jmenovatel = (fyzické množství + finanční množství)

> [!NOTE]
> Pokud pro položku není vybrána možnost **Zahrnovat fyzickou hodnotu**, systém použije hodnotu 0 (nula) pro fyzickou částku i fyzické množství. Informace o této možnosti naleznete v tématu [Zahrnout fyzickou hodnotu](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Vyhnutí se cenovému nadhodnocení

Ve výjimečných případech systém ohodnotí několik výdejů dříve, než obdrží dostatečné množství příjmů, které slouží jako základ ceny. Tento scénář může způsobit výrazně nadhodnocené odhady průběžné průměrné nákladové ceny. Existují však postupy, pomocí kterých můžete problému nadhodnocení ceny zabránit nebo zmírnit dopady problému, pokud k němu dojde.

**Scénář:** Dojde k následujícím transakcím u položky, pro kterou jste vybrali možnost **Zahrnout fyzickou hodnotu**:

1. Finančně obdržíte množství 100 za 100,00 USD.
2. Finančně vydáte množství 200.
3. Fyzicky obdržíte množství 101 za 202,00 USD.

Pokud zobrazíte odhadovanou průběžnou průměrnou nákladovou cenu pro položku, očekáváte položkovou cenu 1,51 USD. Místo toho najdete odhadovaný průběžný průměr 102,00 USD, který je založen na následujícím vzorci:

Odhadovaná cena = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102

K tomuto zvýšení ceny dochází proto, že když je v kroku 2 finančně vydáno 200 položek, systém musí ocenit 100 položek, než bude mít nějaké odpovídající příjmy. Tato situace způsobí záporný sklad. Systém poté podle očekávání odhadne cenu položky na 1,00 USD. Nicméně při obdržení odpovídajících 100 příjmů je jednotková cena každé položky 2,00 USD.

> [!NOTE]
> I když výdeje vytvoří záporný sklad, úroveň zásob je při výpočtu ceny výdeje kladná. Proto je používána průběžná průměrná nákladová cena namísto ceny hlavní položky. V tomto okamžiku systém obsahuje vyrovnání skladové hodnoty ve výši 100,00 USD. Ačkoliv toto vyrovnání bylo sestaveno z více než 100 kusů, tak kde došlo k posunu každého kusu ve výši 1,00 USD, máte nyní k dispozici pouze jeden kus ve skladu. Proto bude přidělen k tomuto jednomu kusu protiúčet 100,00 USD. Výsledkem je výrazně nadhodnocená odhadovaná nákladová cena.
>
> Pro porovnání si povšimněte, že v případě otočení pořadí kroků 2 a 3 ve výše uvedeném příkladu dojde k vydání 200 položek při ceně položky 1,51 USD a zbude jedna položka, také o ceně 1,51 USD. Vzhledem k tomu, že k tomuto scénáři cenového nadhodnocení může dojít při negativní hodnotě skladu, je obtížné předejít následujícím případům:
>
> - Je nutné odhadnout cenu výdeje na základě hodnoty a množství položek na skladě.
> - Je nutné upravit hodnotu a množství položek na skladě při výdejích a příjmech.
> - Obchodní model umožňuje odesílání nebo oceňování více kusů, než kolik jich máte.
> - Je nutné přijmout libovolnou obdrženou hodnotu a množství.

Použití následujících postupů však pomáhá zabránit negativním množstvím, která umožňují scénář cenového nadhodnocení, pokud obchodní model tyto postupy povoluje:

- Pokud vyberete možnost **Zahrnovat fyzickou hodnotu** pro určitou položku, vypněte zaškrtávací políčko **Záporný fyzický sklad** na stránce **Skupiny modelů položek**.
- Pokud **ne** vyberete možnost **Zahrnovat fyzickou hodnotu** pro určitou položku, zrušte označení možnosti **Záporný finanční sklad** na stránce **Skupiny modelů položek**.

Dále mějte dále na paměti, že maximální vyrovnání hodnoty fyzických zásob je omezeno počtem fyzických transakcí a rozdílem mezi fyzickými a finančními cenami. Dokud jsou všechny fyzické transakce dodatečně finančně aktualizovány, fyzická hodnota nemůže stoupnout na extrémní úroveň. A konečně, efekt nadhodnocení se dále výrazně snižuje v případě, že je kumulované vyrovnání rozprostřeno na více kusů na skladě namísto jednoho kusu.

## <a name="avoid-a-zero-cost-price-on-issues"></a>Jak se vyhnout nulovým nákladům u výdejů

Když není vybrána možnost **Zahrnout fyzickou hodnotu** ve stránce **Skupina modelů položek**, může mít výdej ze zásob nulovou cenu, pokud v zásobách nejsou žádné finančně aktualizované příjmy. Abyste se této situaci vyhnuli, předpokládejme následující možnosti:

- Vyberte možnost **Zahrnout fyzickou hodnotu** na stránce **Skupina modelů položek**. Tato možnost zabrání nulové nákladové ceně u výdeje za předpokladu, že je příjemka fyzicky aktualizována. Pokud nepovolíte záporné fyzické zásoby, výdeje vypočítají průběžný průměr z fyzicky aktualizovaných transakcí.
- Vytvořte výchozí nákladovou cenu položky aktivací verze ocenění, která má standardní náklady, nebo zadejte cenu na záložce **Správa nákladů** ve stránce **Podrobnosti o uvolněném produktu**. Tato možnost je nejlepší, když není vybrána možnost **Zahrnout fyzickou hodnotu** na stránce **Skupina modelů položek**, protože systém bude mít vždy k dispozici záložní cenu.
- Vyberte možnost **Použít nejnovější nákladovou cenu** na záložce **Správa nákladů** ve stránce **Podrobnosti o uvolněném produktu**. Tato možnost aktualizuje hodnotu pole **Cena** pokaždé, když finančně aktualizujete příjemku. Pokud vyberete tuto možnost, ale nezadáte výchozí cenu nebo neaktivujete cenu ve standardní verzi nákladů, stále můžete mít nulové náklady u výdeje.

Pokud máte výdejové transakce, které mají nulové náklady, proces *Závěrka a úprava zásob* opraví nákladovou cenu vytvořením úpravy po finanční aktualizaci příjemek. Mějte na paměti, že finanční období, kdy dojde k této aktualizaci, se může lišit od finančního období, kdy byly položky fyzicky přijaty nebo vydány.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

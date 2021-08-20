---
title: Průběžná průměrná nákladová cena
description: Proces uzávěrky skladu v aplikaci vyrovná výdejové transakce příjmovými transakcemi podle metody oceňování zásob, která je vybraná ve skupině modelu zboží. Před spuštěním uzávěrky skladu však systém vypočítá průběžnou průměrnou nákladovou cenu, která obvykle slouží k účtování výdejových transakcí.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventModelGroup, InventOnhandItem, InventTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79003
ms.assetid: adc3f245-dc9d-4327-88fb-6a579194a5fe
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab90c8e57d831fbbfe0b4a6f6814ca0ab5182a7ccc0436ca5a11526b72f9da30
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/05/2021
ms.locfileid: "6781578"
---
# <a name="running-average-cost-price"></a>Průběžná průměrná nákladová cena

[!include [banner](../includes/banner.md)]

Proces uzávěrky skladu v aplikaci vyrovná výdejové transakce příjmovými transakcemi podle metody oceňování zásob, která je vybraná ve skupině modelu zboží. Před spuštěním uzávěrky skladu však systém vypočítá průběžnou průměrnou nákladovou cenu, která obvykle slouží k účtování výdejových transakcí.

Systém odhaduje průběžnou průměrnou nákladovou cenu pro položku pomocí následujícího vzorce: 

Odhadovaná cena = (fyzická částka + finanční částka) ÷ (fyzické množství + finanční množství)

## <a name="using-the-running-average-cost-price"></a>Použití průběžné průměrné nákladové ceny
Následující tabulka uvádí případy, kdy systém účtuje skladové transakce na základě průběžné průměrné nákladové ceny, a kdy používá nákladovou cenu definovanou v hlavním záznamu položky.

| Podmínka                                               | Systém používá odhadovanou průběžnou průměrnou nákladovou cenu | Systém používá nákladovou cenu, která je definovaná v hlavním záznamu položky |
|---------------------------------------------------------|----------------------------------------------------------|-------------------------------------------------------------------|
| Dělenec\* i dělitel\*\* jsou kladné.  | Ano                                                      | Žádný                                                                |
| Dělenec\*, dělitel\*\*, nebo oba jsou záporné. | Žádný                                                       | Ano                                                               |
| Dělenec\*\* má hodnotu 0 (nula).                        | Žádný                                                       | Ano                                                               |

\* Dělenec = (fyzická částka + finanční částka) \*\* Dělitel = (fyzické množství + finanční množství) 

**Poznámka:** Pokud pro položku není vybrána možnost **Zahrnovat fyzickou hodnotu**, systém použije hodnotu 0 (nula) pro fyzickou částku i fyzické množství. Informace o této možnosti naleznete v tématu [Zahrnout fyzickou hodnotu](include-physical-value.md).

## <a name="avoiding-pricing-amplification"></a>Vyhnutí se cenovému nadhodnocení
Ve výjimečných případech systém ohodnotí několik výdejů dříve, než obdrží dostatečné množství příjmů, které slouží jako základ ceny. Tento scénář může způsobit výrazně nadhodnocené odhady průběžné průměrné nákladové ceny. Existují však postupy, pomocí kterých můžete problému nadhodnocení ceny zabránit nebo zmírnit dopady problému, pokud k němu dojde. **Scénář** Dojde k následujícím transakcím u položky, pro kterou jste vybrali možnost **Zahrnout fyzickou hodnotu**:

1.  Finančně obdržíte množství 100 za 100,00 USD.
2.  Finančně vydáte množství 200.
3.  Fyzicky obdržíte množství 101 za 202,00 USD.

Pokud zobrazíte odhadovanou průběžnou průměrnou nákladovou cenu pro položku, očekáváte položkovou cenu 1,51 USD. Místo toho najdete přibližný průběžný průměr 102,00 USD, který vychází z následujícího vzorce: Odhadovaná cena = \[202 + (-100)\] ÷ \[101 + (-100)\] = 102 ÷ 1 = 102 K tomuto nadhodnocení oceňování dochází proto, že při finančním výdeji 200 položek v kroku 2 musí systém ocenit 100 těchto položek dříve, než obdrží odpovídající příjmy. Tato situace způsobí záporný sklad. Systém poté podle očekávání odhadne cenu položky na 1,00 USD. Nicméně při obdržení odpovídajících 100 příjmů je jednotková cena každé položky 2,00 USD. 

**Poznámka:** I když výdeje vytvoří záporný sklad, úroveň zásob je při výpočtu ceny výdeje kladná. Proto je používána průběžná průměrná nákladová cena namísto ceny hlavní položky. V tomto okamžiku systém obsahuje vyrovnání skladové hodnoty ve výši 100,00 USD. Ačkoliv toto vyrovnání bylo sestaveno z více než 100 kusů, tak kde došlo k posunu každého kusu ve výši 1,00 USD, je nyní k dispozici pouze jeden kusu ve skladu. Proto bude přidělen k tomuto jednomu kusu protiúčet 100,00 USD. Výsledkem je výrazně nadhodnocená odhadovaná nákladová cena. 

**Poznámka:** Pro porovnání si povšimněte, že v případě otočení pořadí kroků 2 a 3 ve výše uvedeném příkladu dojde k vydání 200 položek při ceně položky 1,51 USD a zbude jedna položka, také o ceně 1.51 USD. Vzhledem k tomu, že k tomuto scénáři cenového nadhodnocení může dojít při negativní hodnotě skladu, je obtížné předejít následujícím případům:

-   Je nutné odhadnout cenu výdeje na základě hodnoty a množství položek na skladě.
-   Je nutné upravit hodnotu a množství položek na skladě při výdejích a příjmech.
-   Obchodní model umožňuje odesílání nebo oceňování více kusů, než kolik jich máte.
-   Je nutné přijmout libovolnou obdrženou hodnotu a množství.

Použití následujících postupů však pomáhá zabránit negativním množstvím, která umožňují scénář cenového nadhodnocení, pokud obchodní model tyto postupy povoluje:

-   Pokud vyberete možnost **Zahrnovat fyzickou hodnotu** pro určitou položku, zrušte označení pole **Záporný fyzický sklad** na stránce **Skupiny modelů položek**.
-   Pokud *ne* vyberete možnost **Zahrnovat fyzickou hodnotu** pro určitou položku, zrušte označení možnosti **Záporný finanční sklad** na stránce **Skupiny modelů položek**.

Dále mějte dále na paměti, že maximální vyrovnání hodnoty fyzických zásob je omezeno počtem fyzických transakcí a rozdílem mezi fyzickými a finančními cenami. Dokud jsou všechny fyzické transakce dodatečně finančně aktualizovány, fyzická hodnota nemůže stoupnout na extrémní úroveň. A konečně, efekt nadhodnocení se dále výrazně snižuje v případě, že je kumulované vyrovnání rozprostřeno na více kusů na skladě namísto jednoho kusu.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
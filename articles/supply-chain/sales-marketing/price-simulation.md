---
title: Simulace ceny
description: Tento článek obsahuje informace o simulaci cen pro nabídky. Simulace cen umožňuje vyhodnotit vliv srážek na budoucí prodejní ceny v průběhu nabídky, a to před potvrzením konkrétní ceny.
author: omulvad
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesQuotationPriceSimulation, SalesQuotationsTableLookup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 12254
ms.assetid: 92be7c85-73cf-4f77-833c-d37ce779a031
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1d2c6bf3d13f11482ab31d71e804144d0c5f54db
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807793"
---
# <a name="price-simulation"></a>Simulace ceny

[!include [banner](../includes/banner.md)]

Tento článek obsahuje informace o simulaci cen pro nabídky. Simulace cen umožňuje vyhodnotit vliv srážek na budoucí prodejní ceny v průběhu nabídky, a to před potvrzením konkrétní ceny.

V rámci simulace ceny pro určitou nabídku je zobrazena nová celková částka vycházející z navržené nové ceny. V rámci simulace ceny může být zobrazena také nová částka pro konkrétní řádek vytvořený jako stávající nabídka. Můžete zadat simulaci ceny a použít ji později. Případně můžete použít původní nabídku bez simulace ceny a provést další změny v průběhu prodejního procesu s vašim odběratelem.  

Simulace ceny nezmění cenu v nabídce. Pokud je simulace ceny použita na celou nabídku je s ní v záhlaví nabídky nakládáno jako se speciální slevou. Vztahuje-li se simulace ceny na konkrétní položky, je s ní nakládáno jako se speciální slevou na řádcích nabídky. Prodejní jednotková cena na vytvořeném řádku nabídky se při použití simulace ceny nezmění. Namísto toho je použita procentuální hodnota slevy, která odpovídá snížení ceny řádku nabídky. Při použití simulace ceny jsou jednotková prodejní cena a procentuální hodnota slevy přeneseny na řádek nabídky nebo do záhlaví nabídky.  

>[Poznámka!] Při provádění simulace ceny je k vytvoření simulace použita pouze aktuální prodejní měna. Pokud však zobrazíte součty nabídky, zobrazí se kombinace měny společnosti a prodejní měny.  

Doplňkové položky, které jsou přidány na řádky nabídky, mohou aktivovat řádkové slevy nebo víceřádkové slevy. Také mohou aktivovat celkové slevy, které změní příspěvkové marže a příspěvkové poměry na řádcích nabídky nebo celou slevu.  

Chcete-li sledovat účinek úprav cen pro cíle nabídky, můžete také spustit více simulací cen. Při spuštění těchto simulací lze přizpůsobit celkovou cenu nabídky nebo cenu jednoho nebo několika konkrétních řádků nabídky a poté použít simulaci ceny, která s největší pravděpodobností usnadní uzavření prodeje.  

Při vytvoření nabídky lze nastavit výstrahu. Zde je přehled některých způsobů, kdy je vhodné použít výstrahu:

-   Výstrahy vás informují o stavu nabídek v organizaci.
-   Výstrahy mohou aktivovat revizi konkrétní nabídky nebo vás mohou informovat o překročení limitů slevy.

## <a name="price-simulation-and-discounts"></a>Simulace ceny a slevy
Aby byl zajištěn správný výpočet slev a cen, je nutné dbát při spuštění simulace ceny u nabídky se slevami velké pozornosti. Vzhledem k tomu, že simulace cen jsou u aktivního řádku nabídky či u celé nabídky považovány za speciální slevy, je nutné sledovat rozdíly ve slevách.

### <a name="types-of-discounts-in-trade-agreements"></a>Typy slev v obchodních smlouvách

Obchodní slevy v aplikaci Supply Chain Management mohou mít čtyři typy slev. Tyto slevy mohou být nastaveny pro různé položky, zákazníky či cenové skupiny a mohou být omezeny datem. Při spuštění cenové simulace je nutné brát ohled na obchodní smlouvy, aby nedošlo k chybnému výpočtu. U obchodních smluv jsou k dispozici tyto čtyři typy slev:

-   **Prodejní cena** – pro položky lze zadat zvláštní prodejní ceny. Při vytváření řádků nabídky program vyhledá správnou prodejní cenu pro určitou položku a převede ji do řádků nabídky. Obchodní smlouva s tímto typem slevy tedy neovlivní simulaci ceny. Prodejní cena, která je použita na řádku nabídky, odpovídá obchodní smlouvě.
-   **Řádková sleva** – v závislosti na objednaném množství jsou určeny speciální slevy pro položky. Částky na řádku jsou obvykle sníženy o řádkovou slevu ještě před spuštěním simulace ceny. Obchodní smlouva s tímto typem slevy tedy ovlivní simulaci ceny.
-   **Víceřádková sleva** – v případě, že součet množství přesahuje definovaný limit, předdefinovaná kombinace objednaných položek aktivuje slevu na celou objednávku. Částky na řádku jsou obvykle sníženy o řádkovou slevu ještě před spuštěním simulace ceny. Obchodní smlouva s tímto typem slevy tedy ovlivní simulaci ceny.
-   **Celková sleva** – v případě, že součet částek přesahuje definovaný limit, předdefinované objednané položky aktivují slevu na celou objednávku. Celková sleva je generována podle řádků nabídky. Nicméně vzhledem k tomu, že na celou nabídku je použita celková sleva, sníží se celková částka nabídky. Obchodní smlouva s tímto typem slevy tedy ovlivní simulaci ceny.

### <a name="quotation-lines-and-trade-agreements"></a>Řádky nabídky a obchodní smlouvy

Řádková sleva se automaticky vypočítá při vytvoření nebo úpravě řádku nabídky. Pro položku je na základě obchodní smlouvy zjištěna odpovídající prodejní cena.

## <a name="price-simulation-examples"></a>Příklad simulace ceny
Následující příklady používají simulaci ceny pro záhlaví nabídky a položky jednoho řádku.

### <a name="price-simulation-for-quotation-headers"></a>Simulace ceny pro záhlaví nabídky

Vytvoříte nabídku s následujícími řádky:

-   10 jednotek položky BR-12 (nákladová cena je 9,52 USD za jednotku a prodejní cena je 15,32 USD za jednotku).
-   12 jednotek položky BR-14 (nákladová cena je 7,48 USD za jednotku a prodejní cena je 13,75 USD za jednotku).

Následující tabulka zobrazuje řádky nabídky.

|    &nbsp;                  | Výpočet                          | Výsledek   |
|----------------------------|--------------------------------------|----------|
| Prod. množství             | 10 jednotek + 12 jednotek                  | 22 jednotek |
| Prodejní hodnota v USD         | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Nákladová hodnota v USD          | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Příspěvková marže v USD | 318,20 – 184,96                      | 133,24   |
| Příspěvkový poměr         | (\[318,20 – 184,96\] ÷ 318,20) × 100 | 41,87 %   |

Spusťte simulaci ceny a uplatněte 15procentní celkovou slevu pro celou nabídku nebo záhlaví nabídky. Následující tabulka ukazuje nové součty nabídky po spuštění simulace ceny.

|     &nbsp;                                           | Výpočet                               | Výsledek   |
|------------------------------------------------------|-------------------------------------------|----------|
| Prod. množství                                       | 10 jednotek + 12 jednotek                       | 22 jednotek |
| Původní prodejní hodnota v USD                               | (10 × 15,32) + (12 × 13,75)               | 318,20   |
| Původní nákladová hodnota v USD                                | (10 × 9,52) + (12 × 7,48)                 | 184,96   |
| Původní příspěvková marže v USD                       | 318,20 – 184,96                           | 133,24   |
| Původní příspěvkový poměr                               | (\[318,20 – (10 × 9,52)\] ÷ 318,20) × 100 | 41,87 %   |
| Simulace ceny s 15procentní celkovou slevou v USD | (15 × 318,2) ÷ 100                        | 47,73    |
| Nová prodejní hodnota v USD                               | 318,20 – 47,73                            | 270,47   |
| Nová příspěvková marže v USD                       | 270,47 – 184,96                           | 85,51    |
| Nový příspěvkový poměr                               | \[(270,47 – 184,96) ÷ 270,47\] × 100      | 31,61 %   |

### <a name="price-simulation-for-single-line-items"></a>Simulace ceny pro jednořádkové zboží

Vytvoříte nabídku s následujícími řádky:

-   10 jednotek položky BR-12 (nákladová cena je 9,52 USD za jednotku a prodejní cena je 15,32 USD za jednotku).
-   12 jednotek položky BR-14 (nákladová cena je 7,48 USD za jednotku a prodejní cena je 13,75 USD za jednotku).

Následující tabulka zobrazuje řádky nabídky.

|      &nbsp;                          | Výpočet                          | Výsledek   |
|--------------------------------------|--------------------------------------|----------|
| Prod. množství                       | 10 jednotek + 12 jednotek                  | 22 jednotek |
| Prodejní hodnota v USD pro BR-12         | 10 × 15,32                           | 153,20   |
| Prodejní hodnota v USD pro BR-14         | 12 × 13,75                           | 165,00   |
| Nákladová hodnota v USD pro BR-12          | 10 × 9,52                            | 95,20    |
| Nákladová hodnota v USD pro BR-14          | 12 × 7,48                            | 89,76    |
| Příspěvková marže v USD pro BR-12 | 153,20 – 95,20                       | 58,00    |
| Příspěvková marže v USD pro BR-14 | 165,00 – 89,76                       | 75,24    |
| Příspěvkový poměr v USD pro BR-12  | \[(153,20 – 95,20) ÷ 153,20\] × 100  | 37,86    |
| Příspěvkový poměr v USD pro BR-14  | \[(165,00 – 89,76) ÷ 165,00\] × 100  | 45,60    |
| Celková prodejní hodnota v USD             | (10 × 15,32) + (12 × 13,75)          | 318,20   |
| Celková nákladová hodnota v USD              | (10 × 9,52) + (12 × 7,48)            | 184,96   |
| Celková příspěvková marže v USD     | 318,20 – 184,96                      | 133,24   |
| Celkový příspěvkový poměr             | \[(318,20 – 184,96) ÷ 318,20\] × 100 | 41,87 %   |

Spusťte simulaci ceny a uplatněte 10procentní celkovou slevu na jednotky BR-12. Následující tabulka ukazuje nové součty nabídky po spuštění simulace ceny pro jednořádkové zboží.

|    &nbsp;                                         | Výpočet                             | Výsledek   |
|---------------------------------------------------|-----------------------------------------|----------|
| Prod. množství                                    | 10 jednotek + 12 jednotek                     | 22 jednotek |
| Původní prodejní hodnota v USD pro BR-12                  | 10 × 15,32                              | 153,20   |
| Simulace ceny s 10procentní slevou na položku BR-12 | (10 × 153,2) ÷ 100                      | 15,32    |
| Nová prodejní hodnota v USD pro BR-12                  | (10 × 15,32) – 15,32                    | 137,88   |
| Prodejní hodnota v USD pro BR-14                      | 12 × 13,75                              | 165,00   |
| Nákladová hodnota v USD pro BR-12                       | 10 × 9,52                               | 95,20    |
| Nákladová hodnota v USD pro BR-14                       | 12 × 7,48                               | 89,76    |
| Nová příspěvková marže v USD pro BR-12          | 137,88 – 95,20                          | 42,68    |
| Příspěvková marže v USD pro BR-14              | 165,00 – 89,76                          | 75,24    |
| Nový příspěvkový poměr v USD pro BR-12           | \[(137,88 – 95,20) ÷ 137,88\] × 100     | 30,95    |
| Příspěvkový poměr v USD pro BR-14               | \[(165,00 – 89,76) ÷ 165,00\] × 100     | 45,60    |
| Nová celková prodejní hodnota v USD                      | \[(10 × 15,32) – 15,32\] + (12 × 13,75) | 302,88   |
| Celková nákladová hodnota v USD                           | (10 × 9,52) + (12 × 7,48)               | 184,96   |
| Nová celková příspěvková marže v USD              | 302,88 – 184,96                         | 117,92   |
| Nový celkový příspěvkový poměr                      | \[(302,88 – 184,96) ÷ 302,88\] × 100    | 38,93 %   |

Simulace ceny ovlivňuje pouze řádek, pro který byla použita, a snižuje celkovou hodnotu pro daný řádek.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
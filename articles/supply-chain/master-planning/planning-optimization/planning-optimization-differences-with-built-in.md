---
title: Rozdíly mezi integrovaným hlavním plánováním a optimalizací plánování
description: Toto téma uvádí funkce, které Optimalizace plánování zatím nepodporuje a které nejsou uvedeny na stránce Analýza přizpůsobení optimalizace plánování.
author: ChristianRytt
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 575aef709a0ac3b0cf8150f1e816dac04c069814
ms.sourcegitcommit: ddcab9726e9dbcf3296cb0988b97a3ae7ccb3dfb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/08/2022
ms.locfileid: "8396492"
---
# <a name="differences-between-built-in-master-planning-and-planning-optimization"></a>Rozdíly mezi integrovaným hlavním plánováním a optimalizací plánování

[!include [banner](../../includes/banner.md)]

Výsledky optimalizace plánování se mohou lišit od výsledků z integrovaného hlavního plánovače. Rozdíly mohou být způsobeny chystanými funkcemi. Toto téma uvádí funkce, které Optimalizace plánování zatím nepodporuje a které nejsou uvedeny na stránce **[Analýza přizpůsobení optimalizace plánování](planning-optimization-fit-analysis.md)**.

| Funkce | Aktuální chování v optimalizaci plánování |
|---|---|
| Produkty se skutečnou hmotností | Produkty se skutečnou hmotností jsou považovány za obvyklé produkty.|
| Rozšiřitelné rozměry | Rozšiřitelné rozměry jsou u plánovaných objednávek prázdné, i když je zaškrtnuto políčko **Plán pokrytí podle dimenze** na stránce **Skupiny dimenzí úložiště** nebo **Skupiny sledovacích dimenzí**. |
| Filtrovaná výrobní spuštění | Podrobnosti viz [Plánování výroby - filtry](production-planning.md#filters). |
| Plánování prognóz | Plánování prognóz není podporováno. Doporučujeme použít hlavní plánování, kde je k hlavnímu plánu přiřazen model prognózy. |
| Číselné sekvence pro plánované objednávky | Posloupnosti čísel pro plánované objednávky nejsou podporovány. Plánovaná čísla objednávek jsou generována na straně služby. Plánované číslo objednávky je obvykle zobrazeno s 10 číslicemi, ale sekvence je ve skutečnosti postavena na 20 znacích, přičemž 10 číslic je přiděleno pro počet běhů plánování a dalších 10 číslic pro počet plánovaných objednávek. |
| Naplánujte kopírování, odstranění plánu a vyčištění verze plánu | <p>Následující položky jsou zakázány v **Hlavní plánování \> Hlavní plánování \> Udržujte plány** v navigačním podokně:</p><ul><li>Kopie plánu</li><li>Odstranit plán</li><li>Vyčištění verze plánu</li></ul> |
| Vratky | K vratkám se nepřihlíží. |
| Plánování souvisejících funkcí | Podrobnosti viz [Plánování s nekonečnou kapacitou](infinite-capacity-planning.md#limitations). |
| Plnění rezervních zásob | Optimalizace plánování vždy používá možnost *Dnešní datum a čas pořízení* pro pole **Zadat minimum** na stránce **Disponibilita položky**. To pomáhá předcházet nechtěným plánovaným objednávkám a dalším problémům, protože když není k dispozici čas pořízení pro pojistnou zásobu, budou plánované objednávky, které jsou vytvořeny pro aktuální nízké zásoby na skladě, vždy zpožděny kvůli době realizace. |
| Doložení pojistné zásoby a čisté požadavky | Typ požadavku *Pojistná zásoba* není zahrnut a není zobrazen na stránce **Čisté požadavky**. Pojistná zásoba nepředstavují poptávku a není s ní spojeno datum požadavku. Místo toho nastavuje omezení, kolik zásob musí být neustále přítomno. Nicméně hodnota pole **Minimální** je stále brána do úvahy při výpočtu plánovaných objednávek během hlavního plánování. Doporučujeme zkontrolovat sloupec **Akumulované množství** na stránce **Čisté požadavky**, abyste viděli, že tato hodnota byla vzata do úvahy. |
| Dopravní kalendáře | Hodnota ve sloupci **Přepravní kalendář** na stránce **Způsoby dodání** je ignorována. |
| Kód min/max pokrytí bez hodnot| Když u vestavěného plánovacího modulu použijete kód min/max pokrytí, kde nejsou nastaveny žádné minimální nebo maximální hodnoty, modul plánování považuje kód pokrytí za žádost a pro každou žádost vytvoří jednu objednávku. S optimalizací plánování systém vytvoří jednu objednávku denně, aby pokryl celou částku za daný den.  |

## <a name="additional-resources"></a>Další prostředky

- [Analýza přizpůsobení pro optimalizaci plánování](planning-optimization-fit-analysis.md)
- [Parametry, které optimalizace plánování nepoužívá](not-used-parameters.md)
- [Parametry data a času používané optimalizací plánování](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

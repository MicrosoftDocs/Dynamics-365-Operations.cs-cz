---
title: Rozdíly mezi Optimalizací plánování a zastaralým hlavním plánovacím modulem
description: Tento článek uvádí funkce, které Optimalizace plánování zatím nepodporuje a které nejsou uvedeny na stránce Analýza přizpůsobení optimalizace plánování.
author: t-benebo
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 6e1671a508b85a94ac9687af15e898d885ea94c1
ms.sourcegitcommit: 55e440e30490b2d36d86b22aa1263d5da97633aa
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/04/2022
ms.locfileid: "9745354"
---
# <a name="differences-between-planning-optimization-and-the-deprecated-master-planning-engine"></a>Rozdíly mezi Optimalizací plánování a zastaralým hlavním plánovacím modulem

[!include [banner](../../includes/banner.md)]

Výsledky optimalizace plánování se mohou lišit od výsledků ze zastaralého modulu hlavního plánování. Rozdíly mohou být způsobeny chystanými funkcemi. Tento článek uvádí funkce, které Optimalizace plánování zatím nepodporuje a které nejsou uvedeny na stránce **[Analýza přizpůsobení optimalizace plánování](planning-optimization-fit-analysis.md)**].

| Funkce | Aktuální chování v optimalizaci plánování |
|---|---|
| Produkty se skutečnou hmotností | Produkty se skutečnou hmotností jsou považovány za obvyklé produkty.|
| Rozšiřitelné rozměry | Optimalizace plánování nepodporuje rozšiřitelné dimenze. Pokud používáte optimalizaci plánování, rozšiřitelné dimenze jsou u plánovaných objednávek prázdné, i když je zaškrtnuto políčko **Plán pokrytí podle dimenze** na stránce **Skupiny dimenzí úložiště** nebo **Skupiny sledovacích dimenzí**. |
| Filtrovaná výrobní spuštění | Podrobnosti viz [Plánování výroby - filtry](production-planning.md#filters). |
| Plánování prognóz | Plánování prognóz není podporováno. Doporučujeme použít hlavní plánování, kde je k hlavnímu plánu přiřazen model prognózy. |
| Číselné sekvence pro plánované objednávky | Posloupnosti čísel pro plánované objednávky nejsou podporovány. Plánovaná čísla objednávek jsou generována na straně služby. Plánované číslo objednávky je obvykle zobrazeno s 10 číslicemi, ale sekvence je ve skutečnosti postavena na 20 znacích, přičemž 10 číslic je přiděleno pro počet běhů plánování a dalších 10 číslic pro počet plánovaných objednávek. |
| Naplánujte kopírování, odstranění plánu a vyčištění verze plánu | <p>Následující položky jsou zakázány v **Hlavní plánování \> Hlavní plánování \> Udržujte plány** v navigačním podokně:</p><ul><li>Kopie plánu</li><li>Odstranit plán</li><li>Vyčištění verze plánu</li></ul> |
| Vratky | K vratkám se nepřihlíží. |
| Plánování souvisejících funkcí | Podrobnosti viz [Plánování s nekonečnou kapacitou](infinite-capacity-planning.md#limitations). |
| Plnění rezervních zásob | Optimalizace plánování vždy používá možnost *Dnešní datum a čas pořízení* pro pole **Zadat minimum** na stránce **Disponibilita položky**. To pomáhá předcházet nechtěným plánovaným objednávkám a dalším problémům, protože když není k dispozici čas pořízení pro pojistnou zásobu, budou plánované objednávky, které jsou vytvořeny pro aktuální nízké zásoby na skladě, vždy zpožděny kvůli době realizace. |
| Doložení pojistné zásoby a čisté požadavky | Typ požadavku *Pojistná zásoba* není zahrnut a není zobrazen na stránce **Čisté požadavky**. Pojistná zásoba nepředstavují poptávku a není s ní spojeno datum požadavku. Místo toho nastavuje omezení, kolik zásob musí být neustále přítomno. Nicméně hodnota pole **Minimální** je stále brána do úvahy při výpočtu plánovaných objednávek během hlavního plánování. Doporučujeme zkontrolovat sloupec **Akumulované množství** na stránce **Čisté požadavky**, abyste viděli, že tato hodnota byla vzata do úvahy. Protože se doložení liší, mohou být navrženy různé akce. |
| Dopravní kalendáře | Hodnota ve sloupci **Přepravní kalendář** na stránce **Způsoby dodání** je ignorována. |
| Kód min/max pokrytí bez hodnot| Když u zastaralého hlavního plánovacího modulu použijete kód min/max pokrytí, kde nejsou nastaveny žádné minimální nebo maximální hodnoty, modul plánování považuje kód pokrytí za žádost a pro každou žádost vytvoří jednu objednávku. S optimalizací plánování systém vytvoří jednu objednávku denně, aby pokryl celou částku za daný den.  |
| Čisté požadavky a ručně vytvořené plánované objednávky | Se zastaralým hlavním plánovacím modulem se ručně vytvořené objednávky dodávek pro položku automaticky objeví mezi čistými požadavky na tuto položku. Například při vytváření nákupní objednávky z prodejní objednávky se nákupní objednávka objeví na stránce **Čisté požadavky**, aniž by vyžadovaly jakékoli předchozí akce. Je to proto, že zastaralý hlavní plánovací modul zaznamenává transakce zásob do tabulky `inventLogTTS` a ukazuje změny dynamických plánů na stránce **Čisté požadavky**. S optimalizací plánování se však ručně vytvořené objednávky neobjeví mezi čistými požadavky položky, dokud nebude spuštěna Optimalizace plánování (s plánem, který položku zahrnuje), nebo dokud nevyberete možnost **Aktualizace \> Hlavní plánování** v podokně akcí na stránce **Čisté požadavky**, která spustí hlavní plánování pro položku. Další informace o tom, jak pracovat se stránkou **Čisté požadavky**, najdete v tématu [Čisté požadavky a informace o doložení](net-requirements.md). |
| Přiřazení prostředku | Při práci s nekonečnou kapacitou přiřadí zastaralý modul hlavního plánování všechny plánované objednávky ke stejnému zdroji v dané skupině prostředků. Optimalizace plánování toto zlepšuje náhodným výběrem prostředků, takže různé výrobní zakázky mohou využívat různé prostředky. Chcete-li použít stejný prostředek pro všechny plánované objednávky, musíte tento prostředek zadat v trase. |
| Rozšířené datové typy (EDT) | Optimalizace plánování nepodporuje změny přesnosti EDT. To znamená, že tento proces není oficiálně podporován a není zaručeno, že bude fungovat. |
| Plnění rezervních zásob | Optimalizace plánování vždy používá **Zadat minimum** položky *Dnešní datum a čas pořízení*. To připraví systém na zjednodušené nastavení plánování v budoucnu a zajistí výsledek s akcemi. Není-li k dispozici doba pořízení pro pojistnou zásobu, plánované objednávky, které jsou vytvořeny pro nízké zásoby na skladě, budou vždy zpožděny kvůli době realizace. Toto chování může způsobit výrazný nedostatek informací a nežádoucí plánované objednávky. Doporučeným postupem je změna nastavení pro použití položky *Dnešní datum a čas pořízení*. Aktualizujte hlavní data, abyste se vyhnuli varování. |
| Kopírovat statický do dynamického plánu | Optimalizace plánování nekopíruje statické plánx do dynamických plánů bez ohledu na nastavení stránky **Parametry hlavního plánování**. Obecně platí, že tato operace je méně významná z důvodu rychlosti a úplného obnovení, které poskytuje optimalizace plánování. Pokud jsou použity dva nebo více plánů, je třeba pro každý plán spustit hlavní plánování. |

## <a name="additional-resources"></a>Další prostředky

- [Analýza přizpůsobení pro optimalizaci plánování](planning-optimization-fit-analysis.md)
- [Parametry, které optimalizace plánování nepoužívá](not-used-parameters.md)
- [Parametry data a času používané optimalizací plánování](date-time-used.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

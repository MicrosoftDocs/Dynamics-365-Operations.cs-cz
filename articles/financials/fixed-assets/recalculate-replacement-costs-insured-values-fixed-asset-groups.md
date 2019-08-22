---
title: Přepočet reprodukčních nákladů a pojistných částek pro skupiny dlouhodobého majetku
description: Tento článek vysvětluje postup aktualizace reprodukčních nákladů a pojistné částky pro dlouhodobý majetek.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3261
ms.assetid: b8876f83-8772-4f2a-b277-12724e2a0c44
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9dd04072b4845fe5df2a918b64ba1835ea584dd
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/01/2019
ms.locfileid: "1840234"
---
# <a name="recalculate-replacement-costs-and-insured-values-for-fixed-asset-groups"></a>Přepočet reprodukčních nákladů a pojistných částek pro skupiny dlouhodobého majetku

[!include [banner](../includes/banner.md)]

Tento článek vysvětluje postup aktualizace reprodukčních nákladů a pojistné částky pro dlouhodobý majetek.

Pravidelně byste měli být informováni, že došlo ke změně reprodukčních nákladů nebo nákladů na pojištění dlouhodobého majetku. Například vás správce může informovat o tom, že byla inflace za poslední rok je 3 %, a potřebujete tak zvýšit reprodukční náklady u všech položek majetku o 3 %. 

Ačkoli vena stránce **Dlouhodobý majetek** je možné upravit reprodukční náklady a pojistnou hodnotu jednotlivých položek majetku, výhodnější je použít stránku **Aktualizovat reprodukční náklady a pojistné částky**, která umožňuje aktualizovat tyto hodnoty pro celou skupinu majetku najednou. Tyto informace se týkají způsobu aktualizace hodnot pro skupiny dlouhodobého majetku nebo pro specifický majetek ve skupinách.

## <a name="how-values-are-updated"></a> Jak jsou hodnoty aktualizovány
Chcete-li přepočítat reprodukční náklady a pojistné částky pro skupiny dlouhodobého majetku, určete nejprve procentuální hodnotu, o kterou chcete upravit existující reprodukční náklady a pojistné hodnoty, a poté proveďte periodickou aktualizaci s cílem přímo přepočítat hodnoty. Procento lze zadat do polí **Koeficient reprodukčních nákladů** a **Koeficient pojistné částky** na stránce **Skupiny dlouhodobého majetku**. Ačkoli tyto koeficienty zadáváte pro skupinu majetku, můžete při použití stránky **Aktualizovat reprodukční náklady a pojistné částky** vybrat přepočet reprodukčních nákladů a pojistných částek pouze pro určité položky v rámci skupiny. 

Při přepočtu reprodukčních nákladů a pojistných částek majetku na stránce **Aktualizovat reprodukční náklady a pojistné částky** se používají následující vzorce:

-   \[(koeficient reprodukčních nákladů skupiny majetku / 100) + 1\] \* stávající reprodukční náklady majetku
-   \[(koeficient pojistné částky skupiny majetku / 100) + 1\] \* stávající pojistná částka majetku

> [!NOTE] 
> Použijete-li stránku **Aktualizovat reprodukční náklady a pojistné částky** a jsou tak aktualizovány reprodukční náklady i pojistné částky pro vybraný majetek, nelze vybrat a aktualizovat pouze tuto jednu hodnotu. Chcete-li ponechat jednu hodnotu stejnou a aktualizovat druhou hodnotu, zadejte 0 (nula) jako koeficient na stránce **Skupiny dlouhodobého majetku**. Je-li koeficient nulový nebo prázdný, bude výpočet při aktualizaci vynechán. Na účetní hodnotu a zůstatkovou účetní hodnotu majetku nemá periodická aktualizace žádný vliv. 

## <a name="how-to-use-a-date-to-select-which-items-to-update"></a> Jak použít datum k výběru aktualizovaných položek
Ve výchozím nastavení proces aktualizuje vybraný majetek, který nebyl aktualizován dnes, ale mohl být aktualizován v předchozích dnech. Například &lt; aktuální datum znamená "v minulosti." Datum na stránce **Aktualizovat reprodukční náklady a pojistné částky** můžete změnit kliknutím na tlačítko **Vybrat**. Zadané datum je porovnáno s datem poslední periodické aktualizace majetku (pole **Poslední periodická aktualizace nákladů/hodnoty** na stránce **Dlouhodobý majetek**). Po každé úspěšné aktualizaci reprodukčních nákladů nebo pojistné částky majetku se automaticky změní pole **Poslední periodická aktualizace nákladů/hodnoty** na aktuální datum. 

Příklad 

Včera jste aktualizovali reprodukční náklady pro skupiny majetku automobily, nábytek a budovy o 5 procent. Aktualizace těchto skupin majetku je nyní v pořádku. Jestliže chcete tento majetek vyloučit z dnešní aktualizace všech zbývajících položek majetku, zadejte do pole **Poslední periodická aktualizace nákladů/hodnoty** předvčerejší datum (&lt; včerejší datum), protože poslední aktualizace skupin **Automobily**, **Kancelářský nábytek** a **Budovy**  proběhla mimo zadané kritérium pro datum.

## <a name="cumulative-effect-of-each-update"></a> Kumulativní účinek každé aktualizace
Každá aktualizace má kumulativní účinek. Proto je plánování aktualizací nutné provádět opatrně. Když například v úterý zvýšíte všechny položky majetku o 3% a v pátek zvýšíte skupinu nábytku o 4%, dojde u kancelářského nábytku k celkovému zvýšení o 7,12 %.

## <a name="scenario"></a>Scénář
Manažer vám oznámí následující změny v dlouhodobém majetku:
-   Zvýšení reprodukčních nákladů u všech položek majetku s výjimkou počítačů o 3,25 %.
-   Zvýšení reprodukčních nákladů u nábytku o další 1 %.
-   Snížení reprodukčních nákladů a pojistných částek u všech počítačů o 10 %.

Lze provádět tyto změny:
1.  Na stránce **Skupiny dlouhodobého majetku** zadejte pro všechny skupiny majetku, s výjimkou skupiny **Kancelářský nábytek** a **Počítače** hodnotu 3,25 do pole **Koeficient reprodukčních nákladů** a do pole **Koeficient pojistné částky** zadejte hodnotu 0.
2.  Pro skupinu **Kancelářský nábytek** zadejte do pole **Koeficient reprodukčních nákladů** hodnotu 4,25 a do pole **Koeficient pojistné částky** zadejte hodnotu 0.
3.  Pro skupinu **Počítače** zadejte do pole **Koeficient reprodukčních nákladů hodnotu** -10 a do pole **Koeficient pojistné částky** zadejte hodnotu -10.
4.  Na stránce **Aktualizovat reprodukční náklady a pojistné částky** lze kliknutím na možnost **OK** spustit přepočet všech položek dlouhodobého majetku.

Následující den vám manažer oznámí, že počítače klesly o 8 % místo 10 %, takže je třeba opravit reprodukční náklady i pojistné částky. Chybu lze opravit dvěma způsoby:
-   Ručně změňte pole **Pojistná částka** a **Reprodukční náklady**na stránce **Dlouhodobý majetek** pro každý dlouhodobý majetek ve skupině dlouhodobého majetku **Počítače**. Vypočtěte a ručně zadejte hodnoty, jako byste snížili původní částku o 8 %. Pomocí této metody nelze nepoužívat stránku **Aktualizovat reprodukční náklady a pojistné částky**.
-   Zadejte reprodukční náklady a koeficienty pojistné částky pro skupinu **Počítače** v polích **Koeficient reprodukčních nákladů** a **Koeficient pojistné částky** na stránce **Skupiny dlouhodobého majetku**. Tím u majetku znovu nastavíte původní hodnotu (před 10% snížením) a potom provedete 8% snížení původní hodnoty. Poté použijte stránku **Aktualizovat reprodukční náklady a pojistné částky** k přepočítání hodnot v závislosti na faktorech, které jste zadali.

> [!NOTE]  
> Koeficient -10 nelze zrušit zadáním kladného koeficientu 10 (ani zadáním koeficientu 2, což by byl rozdíl mezi -10 a -8), protože výpočet částek by dopadl jinak než zamýšlíte. 






---
title: Odpisy dlouhodobého majetku
description: Tento článek podává přehled odpisu pro dlouhodobý majetek.
author: moaamer
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 3121
ms.assetid: 98ff891f-e0e2-4184-b618-28107a50851f
ms.search.form: AssetBonus, AssetBookTable
ms.openlocfilehash: 9761fc9846324d1c165274b72033e195bf4ea3e0
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275288"
---
# <a name="fixed-asset-depreciation"></a>Odpisy dlouhodobého majetku

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Tento článek podává přehled odpisu pro dlouhodobý majetek.

Odpis představuje periodickou transakci, která obvykle snižuje hodnotu dlouhodobého majetku v rozvaze a v knize zisků a ztrát účtována jako výdaj. Proto se hlavní účet obvykle použije pro odepsání pravidelného odpisu do rozvahy. Protiúčet je účtem v části zisků a ztrát účtové osnovy.

Od verze 10.0.24 volba konfigurace knihy majetku **Počítat kladné odpisy** na stránce **Knihy** umožňuje odpisu připsat na vrub dlouhodobého majetku, který je pořízen se zápornou účetní hodnotou (kredit).

## <a name="depreciation-adjustment"></a>Oprava odpisu
Obvykle je pouze oprava již zaúčtované transakce odpisu zaúčtována jako oprava odpisu. Proto se hlavní účet a protiúčet nastaví stejně jako účty pro odpis. Opravy odpisu lze provést u kladné i záporné částky, avšak funkce hlavního účtu (jako účet rozvahy) a protiúčtu (obvykle jako účet zisků a ztrát) zůstane stejná.

## <a name="extraordinary-depreciation"></a>Mimořádný odpis
Mimořádné odpisy fungují stejně jako základní. Proto se hlavní účet používá k zaúčtování částky odpisu do rozvahy a snížení hodnoty dlouhodobého majetku. Protiúčet je účet zisků a ztrát, kde je odpis, který se vypočítá pro fiskální období, účtován jako výdaj. 

Mimořádný odpis není závislý na základním odpisu. Pokud máte mimořádný odpis jako samostatný typ transakce, můžete mimořádný odpis zaúčtovat a vykazovat nezávisle na základním odpisu.

## <a name="special-depreciation-allowance"></a>Náhrada za zvláštní odpisy
Náhrady za zvláštní odpisy umožňují odepsat mimořádné částky odpisu během prvního roku, ve kterém se majetek začal používat a odepisovat. Náhrady za zvláštní odpisy musí být provedeny před veškerými jinými výpočty odpisů. Vzhledem k tomu, že náhrady za zvláštní odpisy jsou obvykle neznámé až do pozdější servisní životnosti dlouhodobého majetku, je nejvhodnější používat tento druh odpisů v knize, která nezaúčtovává do hlavní knihy. Můžete použít funkci Odstranit transakce, které nebyly zaúčtovány do hlavní knihy k odstranění historie transakcí pro tyto knihy. Pak lze odstranit historii odpisů pro knihu dlouhodobého majetku, zaúčtovat náhradu za zvláštní odpisy, když je známá, a zaúčtovat zbývající odpisovou transakci na rok. 

Lze vytvořit neomezený počet záznamů náhrady za zvláštní odpisy. Jakmile tyto záznamy přiřadíte ke knize odpisů skupiny majetku, použijí se i v knize odpisů majetku. 

Náhrada za zvláštní odpisy se zadává jako procento nebo pevná částka. Při zaúčtování návrhů na odpisy budou transakce náhrady za zvláštní odpisy zaúčtovány do knihy odpisů jako transakce, které jsou odděleny od odpisových transakcí.

## <a name="depreciation-calendars"></a>Odpisové kalendáře
Každá kniha má kalendář, který se použije při odpisu dlouhodobého majetku. Kniha ve výchozím nastavení použije fiskální kalendář hlavní knihy, pokud neuvedete kalendář knihy. Pokud profil odpisů přidružený ke knize používá fiskální rok odpisů, je nutné vybrat fiskální kalendář pro knihu. 

Můžete vytvořit sdílené kalendáře pomocí stránky **Fiskální kalendáře** v hlavní knize.

Další informace naleznete v tématu [Odpisové metody a způsoby odpisu](depreciation-methods-conventions.md).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]

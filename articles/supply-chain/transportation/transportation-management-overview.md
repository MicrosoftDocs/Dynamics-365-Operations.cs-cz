---
title: Přehled správy přepravy
description: Tento článek poskytuje přehled správy přepravy v aplikaci Supply Chain Management.
author: Weijiesa
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: TMSParameters,TMSRateRouteWorkbench, WHSLoadPlanningWorkbench, TMSLoadBuildTemplateApply, WHSLoadTemplate, TMSTransportationStatus, TMSLoadSeal, TMSLoadBuildProposal, TMSLoadBuildWorkbench, TMSLoadBuildStrategy, TMSLoadBuildStrategyAttributeValue
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "30251"
- intro-internal
ms.assetid: d4e3550c-bca8-469c-82df-56ac0083e4ac
ms.search.region: Global
ms.author: weijiesa
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 12f870c95f28e752c3c3b3dd4161d82815b9954a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8897451"
---
# <a name="transportation-management-overview"></a>Přehled správy přepravy

[!include [banner](../includes/banner.md)]

Tento článek poskytuje přehled správy přepravy v aplikaci Supply Chain Management.

Modul Správa přepravy slouží ke správě přepravy ve vaší společnosti a zároveň určování dodavatelů a řešení trasy pro vstupní a výstupní objednávky. Můžete například určit nejrychlejší trasu nebo nejlevnější sazbu pro dodávku. V následující tabulce jsou popsány základní scénáře používání modulu Správa přepravy.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Scénář</th>
<th>Možnosti modulu Správa přepravy</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Použití externích poskytovatelů logistiky pro činností přepravy.</td>
<td>Použití modulu Správa přepravy pro příchozí a/nebo odchozí přepravu.</td>
</tr>
<tr class="even">
<td>Vlastní vozový park společnosti je k dispozici pro doručení/výdej – náklady na dodání se přenáší na odběratele.</td>
<td>Pro výstupní procesy můžete pomocí modulu Správa přepravy určit náklady na dopravu a předat je na odběratele. Nicméně proces vyrovnání faktury s dopravcem není vyžadován.</td>
</tr>
<tr class="odd">
<td>Vozový park společnosti je k dispozici pro doručení/výdej, ale náklady na doručení se nepředávají odběratelům, protože ceny produktu zahrnují přepravu.</td>
<td>Není požadováno velké množství funkcí pro správu přepravy. Nicméně modul Správa přepravy můžete použít a určit s ním sazbu přepravy a odpovídajícím způsobem upravit prodejní ceny.</td>
</tr>
<tr class="even">
<td>Služby z oblasti logistiky jsou poskytovány jinou právnickou osobou ve stejné společnosti.</td>
<td><ul>
<li>Modul Správa přepravy můžete použít pro zacházení s jinými právními subjekty stejně jako s jiným dopravcem. Nelze automaticky provádět ekonomické transakce mezi právnickými osobami. Z tohoto důvodu je nutné zpracovat tyto transakce ručně (například: vytvořením nákupní objednávky).</li>
<li>V právnické osobě, která poskytuje služby z oblasti logistiky, je možné modul Správa přepravy použít k určení sazeb přepravy.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="planning-transportation-in-supply-chain-management"></a>Plánování přepravy v Supply Chain Management
V modulu Správa přepravy lze dopravní plánování založit na objednávkách nebo na dodávkách, které jsou vytvořeny na základě těchto objednávek. Dodávky vždy v každém okamžiku existují, ale nejsou požadovány pro plánování přepravy. Převodní příkazy jsou součástí odchozího scénáře a je možné je plánovat společně s prodejními objednávkami. 

![Načíst výkres.](./media/Load-drawing1-1024x477.jpg)

## <a name="inbound-transportation"></a>Příchozí přeprava
Pokud objednáváte od dodavatele zboží, které je potřeba dodat na sklad, pravděpodobně budete chtít zajistitt přepravu tohoto zboží sami. Pomocí aplikace Supply Chain Management můžete naplánovat přepravu i převzetí příchozího nákladu. Následující obrázek znázorňuje tok obchodního procesu pro plánování přepravy příchozího nákladu. 

![Obchodní proces: průběh přepravy pro vstupní náklady.](./media/Businessprocessflowforinboundloadtransportation.jpg)

## <a name="outbound-transportation"></a>Odchozí přeprava
Můžete naplánovat a zpracovat odchozí náklad a dodat tak konkrétní položky ze skladu společnosti odběrateli. Pomocí aplikace Supply Chain Management můžete naplánovat přepravu i expedici odchozího nákladu. Následující obrázek znázorňuje tok obchodního procesu pro plánování a zpracování odchozích nákladů pro expedici. 

![Plánování a zpracování odchozích nákladů.](./media/Planningandprocessingoutboundloads.jpg)

## <a name="load-building"></a>Sestavení vytížení
Aplikace Supply Chain Management obsahuje strategii sestavení vytížení, která se nazývá Strategie sestavení vytížení založená na objemu. Tato strategie umožňuje použít maximální hodnoty zadané pro výšku a hmotnost v šabloně vytížení nebo přepsat nastavení zadáním nových hodnot. Pokud chcete použít tuto strategii, vyberte ji v poli **Strategie sestavení vytížení** na pevné záložce **Nastavení** na stránce **Pracovní plocha sestavení vytížení**. Kromě toho můžete přidat vlastní strategie sestavení vytížení vytvořením nové třídy ve stromu aplikačních objektů (AOT).





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
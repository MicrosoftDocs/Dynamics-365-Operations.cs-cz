---
title: Mezipodnikové hlavní plánování
description: Tento článek vysvětluje mezipodnikové hlavní plánování
author: Henrikan
ms.date: 09/01/2021
ms.topic: article
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 4993f981b268127af7c9259aa0e73a8e4a75015a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851442"
---
# <a name="intercompany-master-scheduling"></a>Mezipodnikové hlavní plánování

[!include [banner](../../includes/banner.md)]

Mezipodnikové hlavní plánování je prostředkem, který umožňuje vypočítat požadavky a generovat plánované mezipodnikové objednávky pro několik interních společností. Mezipodnikové hlavní plánování se provádí v několika iteracích, které zadáváte. Chcete-li aplikaci Microsoft Dynamics 365 Supply Chain Management umožnit provedení mezipodnikového hlavního plánování, musíte nastavit hlavní plánování v každé z mezipodnikových společností. To znamená několik iterací, při kterých aplikace Microsoft Dynamics 365 Supply Chain Management automaticky vytváří mezipodnikovou nákupní objednávku a to vede k automatickému vytvoření mezipodnikové prodejní objednávky, která znovu znamená vznesení nové poptávky.

Mezipodnikový hlavní plán a pořadí mezipodnikového plánování nastavujete v parametrech **Hlavní plánování** v každé mezipodnikové společnosti.

Abyste mohli šířit poptávku v mezipodnikovém řetězci, musíte nastavit parametry, které zajistí, že se plánované nákupní objednávky automaticky zapevní; to znamená, že objednávky nelze měnit z hlediska času ani množství. Nastavte údaj **Pevná ochranná doba schválení** ve skupině Pokrytí nebo **Pevná ochranná doba schválení** v hlavním plánu. Pokud není **Pevná ochranná doba schválení** nastavena, nevytvářejí se automaticky žádné mezipodnikové nákupní objednávky. Pouze první provedení hlavního plánování skončí vytvořením plánovaných objednávek. Protože se však nevytvoří žádná mezipodniková nákupní objednávka, nevytvoří se žádná mezipodniková prodejní objednávka, a proto se nevytvoří žádné další mezipodnikové nákupní objednávky atd.

Když začnete mezipodnikové hlavní plánování, aplikace Microsoft Dynamics 365 Supply Chain Management provede jedno hlavní plánování v každé mezipodnikové společnosti, pak provede druhou hlavní plánování v každé mezipodnikové společnosti atd., až je dosaženo zadaného počtu iterací. Lze provést maximálně 30 iterací, ale čím více iterací zadáte, tím více času plánování zabere.

Mezipodnikové hlavní plánování můžete začít u kterékoliv mezipodnikové společnosti, protože hlavní plánování ve společnostech je řízeno mezipodnikovou plánovací sekvencí, což je pořadí, ve kterém program přiřazuje prioritu hlavním plánům v každé mezipodnikové společnosti. Protože mezipodniková plánovací sekvence stanoví pořadí, ve kterém se hlavní plánování ve společnostech provede, není důležité, kde mezipodnikové hlavní plánování začne. Při každé iteraci se stávající společnost zpracuje jako poslední.

> [!NOTE]
> Nejlepší je umožnit spuštění mezipodnikového hlavního plánování z jedné společnosti aplikace Microsoft Dynamics 365 Supply Chain Management.

Na stránce **Mezipodnikové hlavní plánování** můžete spustit sekvenci hlavního plánování, která zpracuje hlavní plánování nejprve s principem aktualizovat požadavek výpočtu, který jste vybrali pro první iteraci všech mezipodnikových společností. Následující iterace používají sekundární princip, který vyberete pro následující iteraci a tento princip je aplikován do chvíle, než je dosaženo specifikovaného počtu iterací.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

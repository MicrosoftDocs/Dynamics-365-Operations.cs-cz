---
title: Automatické potvrzení s optimalizací plánování
description: Toto téma vysvětluje, jak používat automatické potvrzování s optimalizací plánování.
author: ChristianRytt
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-11-30
ms.dyn365.ops.version: AX 10.0.7
ms.openlocfilehash: 90319222e7357d7c54243faa8c64575377348467
ms.sourcegitcommit: 0138b6c108a10f2bcb90c91205da8092917160d8
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 11/11/2019
ms.locfileid: "2783146"
---
# <a name="auto-firming-with-planning-optimization"></a>Automatické potvrzení s optimalizací plánování

[!include [banner](../../includes/preview-banner.md)]
[!include [banner](../../includes/banner.md)]

Automatické potvrzení umožňuje potvrdit (tj. vydat) plánované objednávky v rámci procesu hlavního plánování. Při potvrzení jsou plánované objednávky transformovány do skutečných nákupních objednávek, převodních příkazů nebo výrobních zakázek. Je-li použita optimalizace plánování, budou plánované objednávky během hlavního plánování potvrzeny v okamžiku, kdy datum objednávky (tj. datum zahájení) spadá do ochranné doby pro potvrzení.

> [!NOTE]
> K automatickému potvrzení plánované nákupní objednávky může dojít pouze tehdy, pokud je položka přidružena k dodavateli.

## <a name="turn-on-auto-firming"></a>Zapnout automatické potvrzování

Chcete-li zapnout automatické potvrzování, postupujte následujícím způsobem.

1. V pracovním prostoru **Správa funkcí** na kartě **Nová** vyberte v seznamu **automatické potvrzení pro optimalizaci plánování**. Pokud se tato funkce nezobrazí na kartě **Nová**, podívejte se na karty **Není povoleno** a **Vše**.
1. Vyberte **Povolit**. Můžete také vybrat možnost **Plán** a vybrat čas, kdy má být funkce zapnuta.

## <a name="set-up-the-firming-time-fence"></a>Nastavení časového ohraničení potvrzení

Ochranná doba potvrzení se počítá od data spuštění hlavního plánování. Definuje ji počet dní, které zadáte. Ochrannou dobu potvrzování můžete řídit následujícími způsoby:

- Chcete-li definovat výchozí ochrannou dobu potvrzování pro skupinu disponibility, přejděte na **Hlavní plánování** \> **Nastavení** \> **Disponibilita** \> **Skupiny disponibility** a vyberte skupinu disponibility. Pak na pevné záložce **Jiné** zadejte do pole **Ochranná doba automatického potvrzování (ve dnech)** počet dní.
- Pokud chcete přepsat ochrannou dobu potvrzení definovanou pro skupinu pokrytí pro konkrétní položku, přejděte na **Správa informací o produktu** \> **Vydané produkty**, v podokně akcí vyberte **Plán** a pak vyberte **Pokrytí položky**. Potom na kartě **Obecné** vyberte **Přepsat ochrannou lhůtu** a do pole **Automatická ochranná lhůta (dny)** zadejte počet dní.
- Chcete-li přepsat ochrannou dobu potvrzování definovanou pro skupinu disponibility a disponibilitu položky pro určitý hlavní plán, přejděte na **Hlavní plánování** \> **Nastavení** \> **Hlavní plány** a vyberte hlavní plán. Pak na pevné záložce **Ochranná doba ve dnech** nastavte **Zmrazit** na **Ano** a zadejte počet dní.

Je-li pro spuštění hlavního plánování, které používá optimalizaci plánování, zapnuto automatické potvrzování, bude proces automatického potvrzování proveden v souladu s nastavením automatického potvrzování. Pokud není zapnuto automatické potvrzování nebo pokud je plánování zahájeno ze stránky **Požadavky netto**, bude proces automatického potvrzování přeskočen.

## <a name="planning-optimization-vs-the-built-in-supply-chain-management-planning-engine"></a>Optimalizace plánování vs. předdefinovaný modul plánování správy zásobovacího řetězce

Optimalizaci plánování i plánovací modul, který je integrovaný v Microsoft Dynamics 365 Supply Chain Management, lze použít k automatickému potvrzování plánovaných objednávek. Existují však některé důležité rozdíly. Pokud například optimalizace plánování použije datum objednávky (tj. počáteční datum) k určení, které plánované objednávky mají být potvrzeny, použije předdefinovaný modul plánování pro správu zásobovacího řetězce datum požadavku (tj. koncové datum). Zde je souhrn rozdílů.

**Optimalizace plánování**

- Automatické potvrzení je založeno na datu objednávky (počáteční datum).
- Vzhledem k tomu, že datum objednávky (počáteční datum) aktivuje potvrzení, nemusíte považovat dobu realizace za součást ochranné doby potvrzení.
- Chcete-li potvrdit všechny objednávky, které musí být zahájeny v aktuálním týdnu, musí být ochranná doba potvrzování jeden týden.

**Integrovaný modul plánování v Supply Chain Management**

- Automatické potvrzení je založeno na datu požadavku (koncové datum).
- Chcete-li zajistit, aby byly příkazy potvrzeny včas, musí být ochranná doba potvrzení delší než doba realizace.
- Chcete-li potvrdit všechny objednávky, které musí být zahájeny v aktuálním týdnu, musí být ochranná doba potvrzování doba realizace plus jeden týden.

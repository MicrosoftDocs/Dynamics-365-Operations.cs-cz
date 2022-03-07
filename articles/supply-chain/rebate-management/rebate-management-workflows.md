---
title: Pracovní postupy nabídky správy rabatu
description: Toto téma vysvětluje, jak nastavit pracovní postup nabídky správy rabatu, aby bylo možné nabídky schvalovat a aktivovat.
author: sherry-zheng
ms.date: 02/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WorkflowTableListPageRnr
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: ee342de6d069131e230120c5d65aef58da8e632a
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/11/2021
ms.locfileid: "6020376"
---
# <a name="rebate-management-deal-workflows"></a>Pracovní postupy nabídky správy rabatu

[!include [banner](../includes/banner.md)]

Ke schválení nabídek rabatů používá správa rabatů stejnou platformu pracovního postupu jako ostatní aplikace Finance and Operations. Ke každému pracovnímu postupu jsou přidruženy dva procesy úloh:

- Jeden prvek pracovního postupu aktivuje nabídku, aby mohl uživatel nebo proces pracovního postupu schválit transakce.
- Jeden prvek pracovního postupu nabídku schvaluje.

Abyste mohli použít nabídku rabatu, musí být aktivní v modulu **Správa rabatu**. Chcete-li aktivovat nabídku, musíte nejprve vytvořit a nakonfigurovat *Pracovní postup nabídek správy rabatů*.

Po aktivaci pracovního postupu pro správu rabatů nemohou uživatelé ručně schvalovat nabídky. Musí být vždy použit pracovní postup.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Vytvoření a správa pracovních postupů nabídky správy rabatu

Chcete-li pracovat s pracovními postupy nabídek správy rabatů, přejděte na **Správa rabatů \> Nastavit \> Pracovní postupy správy rabatu**. Tam můžete podle potřeby zobrazovat, vytvářet a aktualizovat pracovní postupy. Najednou může být aktivní pouze jeden pracovní postup tohoto typu. Další informace o pracovních postupech, jak pracovat se stránkou **Pracovní postupy správy rabatu** a jak vytvářet pracovní postupy, naleznete v části [Přehled systému pracovních postupů](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) a souvisejících tématech.

## <a name="use-a-workflow-to-activate-a-deal"></a>Použití pracovního postupu k aktivaci nabídky

Chcete-li aktivovat nabídku prostřednictvím pracovního postupu, otevřete nabídku (například na stránce **Všechny nabídky správy rabatů**). Poté v podokně akcí vyberte **Pracovní postup \> Odeslat**. Jakmile bude nová nabídka zpracována a schválena prostřednictvím pracovního postupu, bude aktivní a připravená k použití.

Po aktivaci nabídky nemůžete změnit její nastavení. Pokud musíte změnit aktivní nabídku, deaktivujte ji a poté vytvořte novou nabídku. Pokud se nová nabídka bude podobat staré nabídce, můžete ji vytvořit zkopírováním staré nabídky.

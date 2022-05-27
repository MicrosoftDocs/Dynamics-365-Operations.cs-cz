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
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-02-19
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 0fe5bc5af953ee7cbbda3477d75a38261bb2bb10
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 05/04/2022
ms.locfileid: "8687405"
---
# <a name="rebate-management-deal-workflows"></a>Pracovní postupy nabídky správy rabatu

[!include [banner](../includes/banner.md)]

Ke schválení nabídek rabatů používá správa rabatů stejnou platformu pracovního postupu jako ostatní finanční a provozní aplikace. Ke každému pracovnímu postupu jsou přidruženy dva procesy úloh:

- Jeden prvek pracovního postupu nabídku schvaluje.
- Jeden prvek pracovního postupu aktivuje nabídku, aby mohl uživatel nebo proces pracovního postupu schválit transakce.

Abyste mohli použít nabídku rabatu, musí být aktivní v modulu **Správa rabatu**. Chcete-li aktivovat nabídku, musíte nejprve vytvořit a nakonfigurovat *Pracovní postup nabídek správy rabatů*.

Uživatelé nemohou ručně schvalovat nabídky. Musí být vždy použit pracovní postup.

## <a name="create-and-manage-rebate-management-deal-workflows"></a>Vytvoření a správa pracovních postupů nabídky správy rabatu

Chcete-li pracovat s pracovními postupy nabídek správy rabatů, přejděte na **Správa rabatů \> Nastavit \> Pracovní postupy správy rabatu**. Tam můžete podle potřeby zobrazovat, vytvářet a aktualizovat pracovní postupy. Najednou může být aktivní pouze jeden pracovní postup tohoto typu. Další informace o pracovních postupech, jak pracovat se stránkou **Pracovní postupy správy rabatu** a jak vytvářet pracovní postupy, naleznete v části [Přehled systému pracovních postupů](../../fin-ops-core/fin-ops/organization-administration/overview-workflow-system.md) a souvisejících tématech.

## <a name="use-a-workflow-to-activate-a-deal"></a>Použití pracovního postupu k aktivaci nabídky

Chcete-li aktivovat nabídku prostřednictvím pracovního postupu, otevřete nabídku (například na stránce **Všechny nabídky správy rabatů**). Poté v podokně akcí vyberte **Pracovní postup \> Odeslat**. Jakmile bude nová nabídka zpracována a schválena prostřednictvím pracovního postupu, bude aktivní a připravená k použití.

Po aktivaci nabídky nemůžete změnit většinu nastavení. Pokud musíte změnit aktivní nabídku, nejprve ji deaktivujte a poté vytvořte novou nabídku. Pokud se nová nabídka bude podobat staré nabídce, můžete ji vytvořit zkopírováním staré nabídky.

Po aktivaci nabídky můžete změnit následující nastavení:

- Odsouhlasí
- Kumulativní záruka
- Účetní profil
- Účetní profil pro záruku
- Poznámky k dokumentu
- Měna
- Od data
- Do data

Kromě toho lze odstranit řádky rabatu.

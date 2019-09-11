---
title: Pořadí provádění pro počáteční synchronizaci aplikací Finance and Operations a Common Data Service
description: Toto téma popisuje pořadí synchronizace, které je nutné provést při vytváření počátečních dat.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: 1473c3bad55734d5f83ee3e4c1654921b872f3bb
ms.sourcegitcommit: 3f05ede8b8acdf0550240a83a013e093b4ad043d
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 08/13/2019
ms.locfileid: "1873121"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-and-common-data-service"></a>Pořadí provádění pro počáteční synchronizaci aplikací Finance and Operations a Common Data Service

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

Před použitím integrace dat je nutné vytvořit počáteční data potřebná pro zákazníky, dodavatele a kontakty. Chcete například vytvořit novou položku **Skupina dodavatelů** a nastavit její hodnotu **Platebních podmínek** na **Net30**. V takovém případě se před pokusem o vytvoření položky **Skupiny dodavatelů** ujistěte, že **Net30** existuje v obou aplikacích  Microsoft Dynamics 365 for Finance and Operations a Common Data Service. (V budoucnu vydá Microsoft funkce platformy pro duální zápis nazvanou Počáteční synchronizace. Ta bude provádět jednočasovou synchronizaci dat mezi Finance and Operations a Common Data Service jako součást nastavení pro duální zápis.)

> [!TIP]
> Microsoft vydává mapu dvojího zápisu pro všechna referenční data, včetně **platebních podmínek** (podmínek platby). Pokud již máte počáteční data v jednom systému, může malá operace aktualizace na záznamu spustit pro tento záznam dvojí zápis.

Je nutné postupovat podle následujícího pořadí priorit a zajistit, aby počáteční data byla k dispozici jak pro Finance and Operations, tak pro Common Data Service.

## <a name="vendor"></a>Dodavatel

Zde je pořadí provádění entity **Dodavatel**:

1. Skupina dodavatelů

    1. Platební podmínky

        1. Den a řádky platby
        2. Platební kalendář

2. Platební metoda dodavatele

## <a name="customer-organization"></a>Odběratel (organizace)

Zde je pořadí provádění entity **Odběratel**:

1. Skupina odběratelů

    1. Platební podmínky

        1. Den a řádky platby
        2. Platba 

2. Způsob platby odběratele

## <a name="contact-person"></a>Kontakt (osoba)

Zde je pořadí provádění entity **Kontakt**:

1. Zákazník
2. Dodavatel

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
ms.openlocfilehash: befe4e12a10f4a39b90bcb4faba6431a063a40e2
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019680"
---
# <a name="execution-order-for-initial-synchronization-of-finance-and-operations-apps-and-common-data-service"></a>Pořadí provádění pro počáteční synchronizaci aplikací Finance and Operations a Common Data Service

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

Před použitím integrace dat je nutné vytvořit počáteční data potřebná pro zákazníky, dodavatele a kontakty. Chcete například vytvořit novou položku **Skupina dodavatelů** a nastavit její hodnotu **Platebních podmínek** na **Net30**. V takovém případě se před pokusem o vytvoření položky **Skupiny dodavatelů** ujistěte, že **Net30** existuje v aplikaci a Common Data Service. (V budoucnu vydá Microsoft funkce platformy pro duální zápis nazvanou Počáteční synchronizace. Ta bude provádět jednočasovou synchronizaci dat mezi aplikací a Common Data Service jako součást nastavení pro duální zápis.)

> [!TIP]
> Microsoft vydává mapu dvojího zápisu pro všechna referenční data, včetně **platebních podmínek** (podmínek platby). Pokud již máte počáteční data v jednom systému, může malá operace aktualizace na záznamu spustit pro tento záznam dvojí zápis.

Je nutné postupovat podle následujícího pořadí priorit a zajistit, aby počáteční data byla k dispozici jak pro aplikaci, tak pro Common Data Service.

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

---
title: Typy problémů pro neshody
description: Toto téma popisuje, jak vytvářet a používat typy problémů pro neshody.
author: rachel-profitt
manager: tfehr
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventProblemType, InventProblemTypeSetup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 94003
ms.assetid: a1d9417b-268f-4334-8ab6-8499d6c3acf0
ms.search.region: Global
ms.search.industry: Distribution
ms.author: raprofit
ms.search.validFrom: 2020-06-17
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df509365f5c900898921acfbda380b5e20c7a251
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956584"
---
# <a name="problem-types-for-nonconformances"></a>Typy problémů pro neshody

[!include [banner](../includes/banner.md)]

Toto téma popisuje, jak vytvářet a používat typy problémů pro neshody.

Stránku **Typy problémů** použijte k definování klasifikace problémů s kvalitou, které mohou nastat u různých typů neshod. Pro každý typ problému, který vytvoříte, musíte určit typy neshod, se kterými lze typ problému použít. Můžete nastavit následující typy neshod:

- **Interní** – neshody tohoto typu se vztahují k zásobám na skladě (například k objednávkám kvality nebo karanténním příkazům).
- **Odběratel** – neshody tohoto typu souvisejí s prodejními objednávkami.
- **Dodavatel** – neshody tohoto typu souvisejí s nákupními objednávkami.
- **Požadavek na službu** – neshody tohoto typu souvisejí se servisními zakázkami.
- **Výroba** – neshody tohoto typu souvisejí s dávkovými objednávkami nebo výrobními zakázkami.
- **Výroba vedlejších produktů** – neshody tohoto typu souvisejí s dávkovými objednávkami vedlejších produktů.

Když vytváříte nový typ problému, vyberte v podokně akcí možnost **Typy neshody** k vytvoření seznamu jednoho nebo více typů neshod, které jsou autorizovány pro daný typ problému. Typ problémů, který například souvisí s kódem defektu, je možné použít na všechny typy neshod. Typ problému související se stížnostmi odběratelů se však může vztahovat pouze na typy neshod **Odběratel** a **Požadavek na službu**.

## <a name="examples-of-problem-types"></a>Příklady typů problémů

Tady je několik příkladů scénářů pro typy problémů, které lze použít s různými typy neshod:

- **Odběratel:** Odběratel podal stížnost, provedl vratku nebo nebyly splněny specifikace kvality.
- **Dodavatel:** Produkt byl poškozen, nebyly splněny specifikace kvality nebo byl obdržen nesprávný produkt.
- **Požadavek na službu:** Nebyly splněny specifikace kvality, odběratel podal stížnost nebo je vyžadována údržba stroje.
- **Výroba:** Nebyly splněny specifikace kvality, je vyžadována údržba stroje nebo byl produkt poškozen.
- **Výroba vedlejších produktů:** Nebyly splněny specifikace kvality, je vyžadována údržba stroje nebo byl produkt poškozen.

## <a name="create-a-problem-type-and-assign-it-to-nonconformance-types"></a>Vytvoření typu problému a jeho přiřazení k typům neshod

1. Přejděte k nabídce **Řízení zásob \> Nastavení \> Správa kvality \> Typy problémů**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky. Poté pro nový řádek nastavte následující pole:

    - **Typ problému** – zadejte jedinečné ID nebo název pro typ problému.
    - **Popis** – zadejte podrobný popis typu problému.

1. Zatímco je stále vybrán nový řádek, vyberte v podokně akcí možnost **Typy neshody**.
1. V podokně Akce vyberte možnost **Nový**. Tím se přidá řádek do mřížky. Poté pro nový řádek nastavte pole **Typ neshody** na typ neshody, který chcete povolit pro typ problému.
1. Opakujte předchozí krok pro každý další typ neshody, který chcete autorizovat pro typ problému.
1. Zavřete stránky.

## <a name="additional-resources"></a>Další prostředky

- [Přehled správy kvality](quality-management-processes.md)
- [Povolit správu kvality a neshod](enable-quality-management.md)
- [Zaměstnanci odpovědní za schvalování neshod](quality-responsible-workers.md)
- [Karanténní zóny pro neshody](quality-quarantine-zones.md)
- [Diagnostické typy pro neshody](quality-diagnostic-types.md)
- [Kódy kvality pro náklady.](quality-charges.md)
- [Operace pro neshody](quality-operations.md)
- [Správa kvality pro procesy skladu](quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

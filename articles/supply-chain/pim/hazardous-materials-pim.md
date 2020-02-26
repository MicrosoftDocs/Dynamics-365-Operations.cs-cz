---
title: Nebezpečné materiály
description: Toto téma obsahuje informace o dokumentech s nebezpečnými materiály a informace, které jsou uloženy ve vašem prostředí.
author: lachlancashMS
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76dd6539e39bb77c546e613b290fc5decba9457f
ms.sourcegitcommit: 4c60f5dccdf0b94ed110a657ef331546adc5424a
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/23/2020
ms.locfileid: "2982301"
---
# <a name="hazardous-materials"></a>Nebezpečné materiály

[!include [banner](../includes/banner.md)]

Informace o nebezpečných materiálech se nastavují ve správě informací o produktu. Tento modul také poskytuje dokumenty, které lze vytisknout pomocí řízení skladu.

Při expedici materiálů, které jsou klasifikovány jako nebezpečné, musí být do dodávek zahrnuty další dokumenty. Funkce nebezpečných materiálů umožňuje zákazníkům ukládat informace o klasifikaci a vzájemně je propojit s položkami výdeje. Tyto informace lze poté použít k přípravě dokumentace o dodávce.

> [!IMPORTANT]
> V zájmu usnadnění správy zásilek nebezpečného zboží vám Microsoft Dynamics 365 Supply Chain Management umožňuje nastavit další referenční informace související s produkty. Můžete také nastavit další dokumenty dodávky. Systém však není automaticky kompatibilní s předpisy vaší země nebo oblasti. Namísto toho je to nástroj, který může pomoci celkovému programu.

Před použitím této funkce je nutné provést následující nastavení:

- **Správa informací o produktech**: Nastavte kódy, které lze použít pro uvolněné produkty.
- **Řízení skladu:** Použijte další dokumenty dodávky pro vytisknutí informací o dodávce.

## <a name="product-information-management"></a>Řízení informací o produktech

V modulu Správa informací o produktu existuje řada nastavení tabulek, kde můžete přidat referenční informace, které jsou uvedeny v seznamech nebezpečného zboží pro silniční, leteckou a námořní dopravu.

Zde je přehled některých regulací, na které se často odkazuje:

- **ADR** – Nařízení vztahující se k mezinárodní přepravě nebezpečného zboží po silnici
- **CFR 49** - Nařízení v USA pro přepravu nebezpečného zboží
- **IMDG** – Kód mezinárodní námořní přepravy nebezpečného zboží
- **IATA** – Nařízení mezinárodního sdružení letecké dopravy (IATA) o nebezpečném zboží

Každé z těchto nařízení obsahuje seznam nebezpečného zboží, který obsahuje referenční kódy. Seznamy pro jednotlivé typy přepravy jsou kombinovány se sdílenými mezinárodními klasifikacemi. Supply Chain Management poskytuje referenční tabulku pro sdílené kódy v těchto seznamech. Každý seznam obsahuje také některé jedinečné kódy, které lze definovat.

Chcete-li zahájit konfiguraci těchto informací, vytvořte nařízení, které lze použít ke konfiguraci počátečních parametrů.

## <a name="warehouse-management"></a>Řízení skladu

Při přípravě dodávky lze vytisknout několik nových sestav. Tyto sestavy využívají informace, které nastavíte v modulu Správa informací o produktech.

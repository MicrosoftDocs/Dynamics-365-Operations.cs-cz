---
title: Nebezpečné materiály
description: Toto téma obsahuje informace o dokumentech s nebezpečnými materiály a informace, které jsou uloženy ve vašem prostředí.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: d27ec5b65cc607c22d97c1dc44bb573bc2772611
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243170"
---
# <a name="hazardous-materials"></a>Nebezpečné materiály

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Informace o nebezpečných materiálech se nastavují ve správě informací o produktu. Tento modul také poskytuje dokumenty, které lze vytisknout pomocí řízení skladu.

Při expedici materiálů, které jsou klasifikovány jako nebezpečné, musí být do dodávek zahrnuty další dokumenty. Funkce nebezpečných materiálů umožňuje zákazníkům ukládat informace o klasifikaci a vzájemně je propojit s položkami výdeje. Tyto informace lze poté použít k přípravě dokumentace o dodávce.

> [!IMPORTANT]
> Funkce nebezpečných materiálů v Microsoft Dynamics 365 Supply Chain Management poskytují kolekci užitečných polí s informacemi o produktu a souvisejících funkcích, které vám mohou pomoci zaznamenat a odkazovat na informace související s vašimi nebezpečnými produkty. Tyto funkce vám také mohou pomoci navrhnout a vytisknout dodací doklady, které obsahují některé totožné informace o všech nebezpečných materiálech, které přepravujete. Systém však automaticky nezajistí vaši plnou kompatibilitu se všemi platnými regulacemi vaší země nebo oblasti. Ačkoli jsou tyto nástroje určeny k tomu, aby vám pomohly dodržovat společné předpisy, nejsou samy o sobě dostatečné ani zaručené. Vaše organizace je odpovědná za to, že si je vědoma všech příslušných předpisů a že podniká všechny kroky nezbytné k jejich dodržování.

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
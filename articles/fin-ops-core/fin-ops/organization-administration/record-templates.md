---
title: Přehled šablon záznamu
description: Tento článek představuje koncept šablon záznamů a vysvětluje, jak je lze použít k vytváření záznamů pro sdílení informací.
author: pvillads
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5a8f924a5c2dad45d2006240230b85592d56e676
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 09/27/2019
ms.locfileid: "2176875"
---
# <a name="record-templates-overview"></a>Přehled šablon záznamu

[!include [banner](../includes/banner.md)]

Tento článek představuje koncept šablon záznamů a vysvětluje, jak je lze použít k vytváření záznamů pro sdílení informací.

Šablony záznamů vám mohou pomoci urychlit vytváření záznamů, ale můžete vytvářet pouze šablony záznamů pro některé typy záznamů.

Například si představte že zadáváte informace o půjčovně automobilů, která se nachází v Brně. Vzhledem k tomu, že většina zákazníků bude pravděpodobně z okolí Brna, bylo by výhodné automaticky vyplnit hodnoty pro pole **Stát**, **Země** a **Město** ve formuláři pronájmu.

> [!NOTE]
> Šablony lze použít pouze na ty oblasti, k nimž máte přístup. Všechny názvy šablon však vidíte také při vytvoření nového záznamu a ostatní uživatelé je vidí, když vytváříte šablony dostupné pro všechny uživatele. Při pojmenování šablon je třeba mít tento fakt na paměti. Nepoužívejte například názvy, které zahrnují slovo „provize“, pokud je důvěrnou informací to, že někteří zaměstnanci ve společnosti mají plat založený na provizích.

Pokud v určitém formuláři existuje jedna nebo více šablon, ke kterým máte přístup, a pokusíte se o vytvoření nového záznamu ve formuláři, zobrazí se stránka **Vyberte šablonu pro...**. Pokud vyberete ze seznamu některou šablonu, bude vytvořen nový záznam obsahující výchozí údaje založené na této vybrané šabloně. Pokud nechcete použít šablony při vytváření nových záznamů, zaškrtněte políčko **Tento dotaz příště nezobrazovat** na stránce **Vybrat šablonu pro**. Pokud chcete zobrazit dialogové okno pro výběr šablony znovu, klikněte pravým tlačítkem na jakýkoli záznam, klikněte na **Informace o záznamu** a pak klikněte na **Zobrazit výběr šablony**.
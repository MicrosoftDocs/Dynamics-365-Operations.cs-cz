---
title: "Vytvoření šablon záznamů"
description: "Tento článek představuje koncept šablon záznamů a vysvětluje, jak je lze použít k vytváření záznamů pro sdílení informací."
author: pvillads
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 16101
ms.assetid: 61ada2d8-84c3-44bc-b4c5-516b1aeac3d1
ms.search.region: Global
ms.author: pvillads
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 869151f2486b7a481e4694cfb6992d0ee2cfc008
ms.openlocfilehash: 24643909b0b481d0fe16a5613f28ec6161ef8314
ms.contentlocale: cs-cz
ms.lasthandoff: 06/13/2017

---

# <a name="create-record-templates"></a>Vytvoření šablon záznamů

[!include[banner](../includes/banner.md)]


Tento článek představuje koncept šablon záznamů a vysvětluje, jak je lze použít k vytváření záznamů pro sdílení informací.

Šablony záznamu vám mohou pomoci vytvořit záznamy rychleji v aplikaci Microsoft 365 for Finance and Operations. Šablony záznamu můžete vytvořit pouze pro některé typy záznamů v aplikaci Microsoft Dynamics 365 for Finance and Operations. Například si **** představte že zadáváte informace o půjčovně automobilů, která se nachází v Brně. Vzhledem k tomu, že většina zákazníků bude pravděpodobně z okolí Brna, bylo by výhodné automaticky vyplnit hodnoty pro pole **Stát**, **Země** a **Město** ve formuláři pronájmu. **Poznámka:** Šablony lze použít pouze na ty oblasti aplikace Finance and Operations, k nimž máte přístup. Všechny názvy šablon však vidíte také při vytvoření nového záznamu a ostatní uživatelé je vidí, když vytváříte šablony dostupné pro všechny uživatele. Při pojmenování šablon je třeba mít tento fakt na paměti. Nepoužívejte například názvy, které zahrnují slovo „provize“, pokud je důvěrnou informací to, že někteří zaměstnanci ve společnosti mají plat založený na provizích. Pokud v určitém formuláři existuje jedna nebo více šablon, ke kterým máte přístup, a pokusíte se o vytvoření nového záznamu ve formuláři, zobrazí se stránka **Vyberte šablonu pro...**. Pokud vyberete ze seznamu některou šablonu, bude vytvořen nový záznam obsahující výchozí údaje založené na této vybrané šabloně. Pokud nechcete použít šablony při vytváření nových záznamů, zaškrtněte políčko **Tento dotaz příště nezobrazovat** na stránce **Vybrat šablonu pro**. Pokud chcete zobrazit dialogové okno pro výběr šablony znovu, klikněte pravým tlačítkem na jakýkoli záznam, klikněte na **Informace o záznamu** a pak klikněte na **Zobrazit výběr šablony**.





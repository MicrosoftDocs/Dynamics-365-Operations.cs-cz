---
title: Přesun souborů NF-e XML jako příloh
description: Tento článek vysvětluje, jak přesunout soubory NF-e XML z vaší databáze Microsoft Dynamics 365 Finance nebo Dynamics 365 Supply Chain Management a zpřístupnit je jako přílohy.
author: gionoder
ms.date: 11/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2022-01-27
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: ce9061896759efeb8e8960e84656d5fc1f0616ae
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877890"
---
# <a name="move-nf-e-xml-files-as-attachments"></a>Přesun souborů NF-e XML jako příloh

[!include [banner](../includes/banner.md)] 


Při vydávání elektronických fiskálních dokumentů (NF-e) jsou vytvořeny soubory XML, které jsou uloženy v databázích Microsoft Dynamics 365 Finance a Dynamics 365 Supply Chain Management . V brazilské jazykové verzi můžete použít funkci **Přesun NF-e XML jako přílohy** pro uvolnění databázového prostoru, který tyto soubory XML zabírají.

Tato funkce přesune soubory XML NF-e pro konkrétní časové období a fiskální subjekt z vaší databáze Finance nebo Supply Chain Management do úložiště objektů Blob patřícího do vašeho předplatného Azure. Tento přesun zpřístupní soubory pouze jako přílohy. Po úspěšném přesunutí souborů XML do úložiště objektů Blob jsou původní soubory z databáze Finance nebo Supply Chain Management odstraněny. Proto je uvolněn ten databázový prostor, který tyto soubory používaly.

Chcete-li povolit funkci **Přesun NF-e XML jako přílohy**, postupujte následujícím způsobem.

1. Ve Finance nebo Supply Chain Management otevřete pracovní prostor **Správa funkcí**.
2. Na kartě **Vše** vyhledejte a vyberte funkci **Přesun NF-e XML jako přílohy**.
3. Vyberte **Povolit**.

Chcete-li přesunout soubory NF-e ve formátu XML jako přílohy, postupujte podle těchto kroků.

1. Přejděte do nabídky **Pohledávky** \> **Fiskální dokumenty** \> **Elektronické fiskální dokumenty** \> **Přesun NF-e XML jako přílohy**.
2. V polích **Od data** a **Do data** určete počáteční a koncové datum.
3. V poli **ID fiskálního subjektu** vyberte hodnotu.
4. Vyberte **OK**.

> [!IMPORTANT]
> Tento proces nelze vrátit zpět. Po přesunutí souborů NF-e ve formátu XML je uživatelé mohou zobrazit pouze výběrem položky **Přílohy** na začátku stránky **Fiskální dokument**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

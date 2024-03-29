---
title: Kontrola stavu experimentu
description: Tento článek vysvětluje, jaký stav má experiment v životním cyklu experimentování v Dynamics 365 Commerce.
author: sushma-rao
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 818435a7c901d2a6b876b9c9db27faffc8b322fc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877242"
---
# <a name="review-the-status-of-an-experiment"></a>Kontrola stavu experimentu
Nastavení a spuštění experimentu v Dynamics 365 Commerce zahrnuje mnoho kroků. Informace o životním cyklu experimentování najdete v tématu [Experimentování v Dynamics 365 Commerce](experimentation-overview.md).

Pokud se chcete dozvědět, kde v životním cyklu se experiment nachází, vyberte **Experimenty** v levém navigačním okně konfigurátoru webů Commerce. Zobrazí se seznam experimentů se stavem každého experimentu v Commerce i ve službě třetí strany, která se používá k povolení vytváření experimentů, přiřazování variant a analýze dat.

Ve sloupci **Stav Commerce** se mohou zobrazit následující hodnoty. 
- **Koncept** – Experiment je připojen ke stránce nebo fragmentu v Commerce a je upravován.
- **Publikováno** – Varianty experimentu jsou připraveny k zobrazení na vašem webu. Pokud je experiment spuštěn ve službě třetí strany, uvidí uživatelé webu variantu stránky nebo fragmentu vybranou službou třetí strany.
- **Nepublikováno** – Experiment už na vašem webu není k dispozici. Pokud je experiment spuštěn ve službě třetí strany, uvidí uživatelé webu jen výchozí verzi stránky nebo fragmentu.
- **Dokončeno** – Experiment proběhl a varianta byla povýšena na živě publikovanou pro všechny uživatele webu.

Podobně ve sloupci **Stav třetí strany** mohou být zobrazeny následující hodnoty, které označují, v jakém stavu se nachází experimenty ve službě třetí strany.
- **Koncept** – Experiment je nastaven ve službě třetí strany, ale nebyl spuštěn.
- **Spuštěno** – Experiment byl spuštěn ve službě třetí strany a shromažďuje data.
- **Pozastaveno** – Experiment je pozastaven a neshromažďuje data. Pokud má experiment znovu shromažďovat data, musíte ho znovu spustit.
- **Archivováno** – Experiment proběhl a byl zařazen do katalogu ve službě třetí strany pro budoucí referenci.

Schéma níže znázorňuje obě sady stavů a jejich vzájemný vztah.

[ ![Stavy experimentování.](./media/experimentation_statuses.svg) ](./media/experimentation_statuses.svg#lightbox)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
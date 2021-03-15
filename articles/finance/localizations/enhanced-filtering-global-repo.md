---
title: Rozšířené filtrování RCS v RCS/globálním úložišti
description: V tomto tématu jsou popsány rozšířené možnosti filtrování pro globální úložiště RCS, které bylo vylepšeno za účelem zahrnutí dalších filtrů.
author: JaneA07
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, ERWorkspace
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: a67a4345271cbeffc100fc1d9077cc866846a4d4
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 01/15/2021
ms.locfileid: "5005835"
---
# <a name="rcs-enhanced-filtering-options-for-finding-configurations-in-the-rcsglobal-repository"></a>Rozšířené možnosti filtrování RCS pro vyhledání konfigurací v RCSD/globálním úložišti

[!include [banner](../includes/banner.md)]

V tomto tématu jsou popsány rozšířené možnosti filtrování pro globální úložiště Regulatory Configuration Services (RCS), které bylo vylepšeno za účelem zahrnutí možnosti filtrování s následujícími kritérii: 
- **Země/oblast** - založená na kódech ISO zemí  
- Typy **značek** pro:
  - Funkční oblast
  - Oblast funkce
  - Obor 
  - Obchodní dokument 

Chcete-li snadněji vyhledat konkrétní nebo související konfigurace, můžete použít filtry, a to buď jednotlivě, nebo jako skupinu. Chcete-li například vyhledat jediný typ nastavitelného obchodního dokumentu, který souvisí s fakturami dodavatele, můžete použít filtr **Typ obchodního dokumentu** a vyhledat tento typ dokumentu. 

[![Oddíl filtru pro globální úložiště](media/rcs-enhanced-filter-section.JPG)](./media/rcs-enhanced-filter-section.JPG) 

Hledání lze dále upřesnit výběrem typu dokumentu, například faktury dodavatele a kliknutím na volbu **Použít filtr**. V následujícím příkladu je zobrazen výsledek při filtrování dle **Typu obchodního dokumentu** s přidaným typem dokumentu. 

[![Použitý filtr a import pro typ obchodního dokumentu](media/rcs-enhanced-filtering-applied.JPG)](./media/rcs-enhanced-filtering-applied.JPG) 

Filtrované výsledky mohou být importovány do úložiště RCS uživatelů nebo prostředí Dynamics 365 Finance, a to buď jednotlivě, nebo jako sadu. Chcete-li to provést, vyberte skupinu konfigurací a klikněte na možnost **Importovat**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
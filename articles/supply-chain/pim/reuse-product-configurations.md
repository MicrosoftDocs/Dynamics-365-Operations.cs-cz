---
title: "Opětovně použít konfigurace produktu"
description: "Můžete určit, že chcete automaticky opětovně použít existující konfiguraci produktu. Když potom uživatel dokončí konfigurační relaci, systém ověří, zda již existuje konfigurace, která odpovídá výběru uživatele. Pokud je nalezena odpovídající konfigurace, znovu se použije ID konfigurace, odpovídající kusovníky a postup."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: c447440c33c1f80c6056974086b90d3b43e8499e
ms.contentlocale: cs-cz
ms.lasthandoff: 02/07/2018

---

# <a name="reuse-product-configurations"></a>Opětovně použít konfigurace produktu

[!INCLUDE [banner](../includes/banner.md)]

Můžete určit, že chcete automaticky opětovně použít existující konfiguraci produktu. Když potom uživatel dokončí konfigurační relaci, systém ověří, zda již existuje konfigurace, která odpovídá výběru uživatele. Pokud je nalezena odpovídající konfigurace, znovu se použije ID konfigurace, odpovídající kusovníky a postup.

<a name="requirements-for-reusing-configurations"></a>Požadavky na opětovné použití konfigurací
---------------------------------------

Pokud chcete povolit opětovné použití konfigurací, je nutné zadat pro komponenty a atributy na stránce **Podrobnosti modelu konfigurace produktu**následující informace:

-   **Komponenty a dílčí komponenty** – Na pevné záložce **Obecné** v poli **Znovu použít konfigurace** vyberte **Ano**.
-   **Atributy** – na pevné záložce **Atributy** vyberte možnost **Zahrnout do opakovaného použití**. Tato možnost se zobrazí, pouze pokud je související komponenta povolena pro opakované použití. Jestliže nevyberete žádné atributy pro opakované použití, konfigurace je vždy znovu použita bez ohledu na to, co uživatel vybere během konfigurační relace. Hodnoty atributů v existující konfiguraci musí odpovídat výběrům uživatele. Když například uživatel vybere jako barvu během relace konfigurace **Modrá**, systém ověří, zda existující konfigurace obsahuje komponenty modrou barvu.

## <a name="resetting-configuration-reuse"></a>Resetování opětovného použití konfigurace
Při resetování opětovného použití konfigurací se přestanou brát v úvahu dříve vytvořené konfigurace. Můžete resetovat opětovné použití konfigurací, pokud byl změněn kusovník nebo postup, ale nebyly změněny žádné související atributy. Opětovné použití konfigurací se resetuje na pevné záložce **Obecné** komponenty.





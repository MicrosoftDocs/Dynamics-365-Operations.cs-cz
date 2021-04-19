---
title: Opětovně použít konfigurace produktu
description: Můžete určit, že chcete automaticky opětovně použít existující konfiguraci produktu. Když potom uživatel dokončí konfigurační relaci, systém ověří, zda již existuje konfigurace, která odpovídá výběru uživatele. Pokud je nalezena odpovídající konfigurace, znovu se použije ID konfigurace, odpovídající kusovníky a postup.
author: cvocph
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 201813
ms.assetid: 4985e308-7824-41fc-83fd-fd0bdae888e3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8a3aca07388a440ce5168fa4106d90d931f7f194
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 04/01/2021
ms.locfileid: "5812780"
---
# <a name="reuse-product-configurations"></a>Opětovně použít konfigurace produktu

[!include [banner](../includes/banner.md)]

Můžete určit, že chcete automaticky opětovně použít existující konfiguraci produktu. Když potom uživatel dokončí konfigurační relaci, systém ověří, zda již existuje konfigurace, která odpovídá výběru uživatele. Pokud je nalezena odpovídající konfigurace, znovu se použije ID konfigurace, odpovídající kusovníky a postup.

<a name="requirements-for-reusing-configurations"></a>Požadavky na opětovné použití konfigurací
---------------------------------------

Pokud chcete povolit opětovné použití konfigurací, je nutné zadat pro komponenty a atributy na stránce **Podrobnosti modelu konfigurace produktu** následující informace:

-   **Komponenty a dílčí komponenty** – Na pevné záložce **Obecné** v poli **Znovu použít konfigurace** vyberte **Ano**.
-   **Atributy** – na pevné záložce **Atributy** vyberte možnost **Zahrnout do opakovaného použití**. Tato možnost se zobrazí, pouze pokud je související komponenta povolena pro opakované použití. Jestliže nevyberete žádné atributy pro opakované použití, konfigurace je vždy znovu použita bez ohledu na to, co uživatel vybere během konfigurační relace. Hodnoty atributů v existující konfiguraci musí odpovídat výběrům uživatele. Když například uživatel vybere jako barvu během relace konfigurace **Modrá**, systém ověří, zda existující konfigurace obsahuje komponenty modrou barvu.

## <a name="resetting-configuration-reuse"></a>Resetování opětovného použití konfigurace
Při resetování opětovného použití konfigurací se přestanou brát v úvahu dříve vytvořené konfigurace. Můžete resetovat opětovné použití konfigurací, pokud byl změněn kusovník nebo postup, ale nebyly změněny žádné související atributy. Opětovné použití konfigurací se resetuje na pevné záložce **Obecné** komponenty.





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
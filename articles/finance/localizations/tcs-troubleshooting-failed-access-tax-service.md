---
title: Nepodařilo se získat přístup k daňové službě
description: Toto téma vysvětluje, jak řešit problém s přístupem ke službě výpočtu daně.
author: hangwan
ms.date: 03/04/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxIntegrationTaxServiceParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: hangwan
ms.search.validFrom: 02/16/2022
ms.dyn365.ops.version: Version 10.0.21
ms.openlocfilehash: 48a75cd0c1d91c3b3d9c3fb2e6cab93a76756532
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: HT
ms.contentlocale: cs-CZ
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388547"
---
# <a name="failed-to-access-tax-service"></a>Nepodařilo se získat přístup k daňové službě

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

Toto téma vysvětluje, jak opravit chybu „Nepodařilo se získat přístup k daňové službě“ služby Výpočet daně.

## <a name="symptoms"></a>Příznaky

V Microsoft Dynamics 365 Finance přejděte na **Daň** \> **Nastavení** \> **Konfigurace daně** \> **Parametry daňové služby**. Na kartě **Obecné** aktivujte možnost **Povolit výpočet daně**. Pokud se poté pokusíte vybrat hodnotu v poli **Název nastavení funkce**, dojde k chybě. Chybová zpráva uvádí: „Nepodařilo se získat přístup k daňové službě.“

## <a name="cause"></a>Příčina

K této chybě dochází, protože Finance nemají přístup ke službě Výpočet daně.

## <a name="resolution"></a>Řešení 

1. Přihlaste se do Microsoft Dynamics Lifecycle Services (LCS).
2. Na stránce **Prostředí** na kartě **Doplňky prostředí** najděte položku **Výpočet daně** a zkontrolujte její stav. Stav by měl být **Instaluje se** nebo **Nainstalováno**. Pokud doplněk služby Výpočet daně není nainstalován, zobrazí se chyba.

## <a name="mitigation"></a>Zmírnění dopadů

1. V LCS, na stránce **Finance** v části **Integrace Power platform** vyberte **Nainstalovat nový doplněk**.
2. Přejděte na konec stránky a vyberte doplněk **Výpočet daně** pro jeho instalaci.
3. Vraťte se do svého finančního prostředí a zkuste získat přístup ke službě Výpočet daně.

> [!NOTE]
> Před instalací služby Výpočet daně si přečtěte [Předpoklady služby daňových výpočtů](global-get-started-with-tax-calculation-service.md#prerequisites).
> 
> Pokud nemůžete nainstalovat doplněk, protože část **Integrace Power platform** není dostupná, viz [Přehled doplňků](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md). Pokud k chybě dochází i po instalaci doplňku, obraťte se na správce systému.
